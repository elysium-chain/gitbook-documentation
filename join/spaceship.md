# 🚀 太空飞船

## NFT规格

- 实用性：参与Elysium中的竞赛，成为首批验证人之一。
- 供应量：不超过9000枚。
- 铸造：在竞赛开始后，可以使用任何访问密钥NFT免费铸造。
- 购买：只能在竞赛开始后的二级市场购买。
- 出售：在竞赛开始后的二级市场随时出售（但会失去已取得的竞赛成绩）。
- 销毁：在达到Elysium后。

## 飞行物理

我们的造船厂生产的每艘太空飞船都配备了一个在给定方向上创建人工惯性的引擎。能源单位称为Energons将持续消耗以维持人工惯性。没有Energons，人工惯性会逐渐减弱，直至飞船完全失去它。飞船的速度越快，每单位时间消耗的Energons就越多。

飞行员的主要任务是确定每小时消耗的Energons。您可以随时手动更改此参数。设置新的Energons消耗率后，飞船会改变速度。如果新值较高，飞船会线性加速，并在一小时内达到新速度。如果新值较低，飞船将停止引擎，并继续通过惯性移动（失去速度），直到速度达到指定的消耗水平所需的值。

如果未更改消耗率，飞船将保持其速度，直到完全耗尽Energons。

#### 引擎效率

引擎效率参数确定Energons的有效使用程度。参数越高，维持相同速度所需的Energons就越少，或者在相同Energons消耗下飞船的速度越快。

{% tabs %}
{% tab title="图表" %}
<figure><img src="../.gitbook/assets/Energon Consumption.webp" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="详情" %}
每小时Energons消耗取决于速度和引擎效率（EE）参数，按以下公式计算：

$$
Energons=\frac{Speed^{4}}{EE\cdot10^{17}}
$$

您可以在此处进行交互式尝试：[交互式图表](https://www.desmos.com/calculator/20n0oayk1s?lang=en)
{% endtab %}
{% endtabs %}

引擎效率取决于密钥类型，并且可以通过游戏内的增益道具进行临时改善，或通过烧毁额外的密钥进行永久改善。

#### 惯性保持

惯性保持参数影响飞船失去人工惯性的速度。尽管所有飞船都会在25小时内失去人工惯性，但失去速度的速度取决于惯性保持值。参数越高，飞船失去速度的速度越慢。

{% tabs %}
{% tab title="图表" %}
<figure><img src="../.gitbook/assets/Inertia Leakage.webp" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="详情" %}
飞船将在25小时内失去所有人工惯性，无论如何。惯性保持（IR）参数影响泄漏速度。剩余速度的百分比按以下公式计算：

$$
Speed=\frac{100+\left(IR+1\right)}{1+\frac{0.16*hour^{2}}{IR+1}}-\left(IR+1\right)
$$

您可以在此处进行交互式尝试：[交互式图表](https://www.desmos.com/calculator/0mvkcqrmjx?lang=en)
{% endtab %}
{% endtabs %}

可以通过游戏内的增益道具临时获得惯性保持点，并通过烧毁额外的密钥（之前质押的密钥）或在比赛开始之前获取飞船来永久获得。

{% hint style="info" %}
在预发行阶段，飞船的惯性保持参数将以比质押的密钥更快的速度增长。烧毁更多的密钥（不论类型）将会增加这种差异。每个烧毁的密钥都会相对于质押减少15%的时间，以获得新的惯性保持点。

{% tabs %}
{% tab title="图表" %}
<figure><img src="../.gitbook/assets/Inertia Rewards.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="详情" %}
在预发行阶段，为了获得飞船的新惯性保持点，需要经过的天数取决于烧毁的密钥数量，按以下公式计算：

$$
DAYS=\frac{30}{KEYs}\cdot0.85^{KEYs}
$$

<table><thead><tr><th width="305.5">烧毁的密钥数</th><th>获得新IR点的天数</th></tr></thead><tbody><tr><td>1（适用于每艘飞船）</td><td>25.5</td></tr><tr><td>2</td><td>10.838</td></tr><tr><td>3</td><td>6.141</td></tr><tr><td>4</td><td>3.915</td></tr></tbody></table>
{% endtab %}
{% endtabs %}
{% endhint %}

#### 太空飞船发射

每艘飞船都是

通过电磁弹射器发射的，获得基础速度，或者换句话说是真实的惯性。飞船失去人工惯性时不会完全停止，而是继续以主要加速度获得的速度移动。这意味着即使在比赛过程中耗尽Energons，您仍然会以相对较低的速度继续向终点前进。

每次发射后，电磁弹射器都会失去能量，每次发射都会使飞船的加速度减小。因此，首先发射的人将占据优势。

{% tabs %}
{% tab title="图表" %}
<figure><img src="../.gitbook/assets/Catapult Power.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="详情" %}
第一次发射将使飞船的速度达到每小时15,000公里。每次后续发射效果都会减弱。特定发射的弹射器能量可以通过以下公式计算：

$$
Speed=\frac{1500000}{N+100}
$$
{% endtab %}
{% endtabs %}

{% hint style="info" %}
在预发行阶段，已加入的先驱者将等待正式比赛开始。由于他们将同时发射，所以会有一个弹射器队列。每个先驱者在预发行期间都将有一个特定的分数，确定了他们在弹射器队列中的位置。有三种方式可以提高分数。

1. 烧毁更好的密钥：\
   &#x20;\- 密钥D得到+10分\
   &#x20;\- 密钥C得到+30分\
   &#x20;\- 密钥B得到+90分\
   &#x20;\- 密钥A得到+270分
2. 尽早烧毁密钥。在开放铸造后的第一天烧毁的密钥（不论类型）将获得+90分。第二天的密钥烧毁将获得+89分。每天这个奖励将减少一分。
3. Elysium团队将使用积分作为不同社区活动的奖励。
{% endhint %}

## 太空飞船升级

通过烧毁额外的密钥，您可以在预发行阶段和比赛开始后的任何时刻改善飞船的参数。密钥的参数将添加到飞船的参数中。

<figure><img src="../.gitbook/assets/Spaceship Upgrade.png" alt=""><figcaption></figcaption></figure>

烧毁四种不同类型的密钥（A、B、C、D）来改善一艘飞船将获得特殊奖励。当一艘飞船使用了这四种密钥进行升级时，将为两个参数添加20分。

{% hint style="info" %}
完整套装奖励只能应用于一艘飞船。
{% endhint %}

<figure><img src="../.gitbook/assets/Prelaunch Special Offer.png" alt=""><figcaption></figcaption></figure>

## 飞行经济

在先驱者计划中，我们决定在真实环境中重新创建Elysium的通证经济模型，以测试其在实际条件下的可行性，然后再启动区块链。在太空竞赛中，我们仅仅将代币数量减少到100,000，并略微加快发行时间。

因此，Astonite -> Cosmogrinder -> Energon之间的关系与Elysium的通证经济模型中的SKY -> Grinder -> RAY完全对应。

#### Astonite挖掘

获得Energons所需的独特矿物质称为Astonite。您可以在每日矿游戏锦标赛中获得它。不幸的是，Astonite的数量不仅在宇宙中有限，而且不断减少。

可以在名为“Astonite Mining”的每日锦标赛中获得Astonite。该活动同时面向所有参与者进行。Astonite根据锦标赛得分进行分发。每天，锦标赛启动时间将推迟一小时，以确保所有先驱者处于相同的条件下。

这些锦标赛是防止多账户的关键机制。由于比赛时间不长（约5-10分钟），并且需要玩家的全部注意力，因此几乎没有可能同时从多个账户进行游戏。当然，我们将确保无法创建可以替代人类进行游戏的机器人。

#### 获得Energons

通过在名为“cosmogrinder”的独特设备中回收Astonite来获得Energons。转换率越高，cosmogrinder的处理越困难。因此，如果每单位Astonite提供的Energon较少，则cosmogrinder的工作速度会更快。
