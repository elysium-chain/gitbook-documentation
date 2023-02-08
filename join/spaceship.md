---
description: A vehicle needed to participate in the race
---

# 🚀 Spaceship

<figure><img src="../.gitbook/assets/Spaceship NFT.webp" alt=""><figcaption></figcaption></figure>

## NFTs Specification

| **Utility** | Participating in the race to become one of the first validators in the Elysium.                              |
| ----------- | ------------------------------------------------------------------------------------------------------------ |
| **Supply**  | Not greater than 9000                                                                                        |
| **Minting** | Free mint with any Access Key NFT after the start of the race.                                               |
| **Buying**  | On the secondary market only, after the start of the race.                                                   |
| **Selling** | At any time after the start of the race on the secondary market (with the loss of the achieved race result). |
| **Burning** | When finishing at Elysium.                                                                                   |

## Flight Physics

Each spaceship produced in our shipyard is equipped with an engine that creates artificial inertia in a given direction. Units of energy called Energons are constantly spent to keep it. Without it, the artificial inertia will decrease until the ship loses it entirely. The greater the speed of the spaceship, the more Energons will be spent per unit of time to keep it.

The main task of the pilot is to determine the hourly consumption of Energons. You can manually change this parameter at any time. When a new Energon consumption rate is set, the spaceship changes its speed. If the new value is higher, the ship linearly accelerates and achieves a new speed in one hour. If the new value is lower, the vessel stops the engine and continues moving by inertia (losing it) until the speed reaches the value required for the specified consumption level.

If the consumption rate is not changed, the spaceship will maintain its speed until it entirely runs out of Energons.

#### Engine Efficiency

The Engine Efficiency parameter determines how productively the Energons are used. The higher the parameter, the fewer Energons are needed to maintain the same speed, or the faster the ship can fly with the same consumption of Energons.&#x20;

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/Energon Consumption.webp" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The hourly consumption of Energons depends on the speed and the _**Engine Efficiency**_ (EE) parameter, and is calculated by the formula:

$$
Energons=\frac{Speed^{4}}{EE\cdot10^{17}}
$$

You can play with it here: [interactive chart](https://www.desmos.com/calculator/20n0oayk1s?lang=en)
{% endtab %}
{% endtabs %}

The Engine Efficiency depends on the key type and can be improved temporarily with the in-game boosters or permanently with additional keys burning.

#### Inertia Retention

The Inertia Retention parameter affects how fast your spaceship will lose its artificial inertia. Though all the ships will lose it in 25 hours, the speed of losing it differs depending on the Inertia Retention value. The higher the parameter is, the slower your ship will drop its speed.&#x20;

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/Inertia Leakage.webp" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The spaceship will lose all artificial inertia if there are no Energons left in 25 hours no matter what. The _**Inertia Retention**_ (IR) parameter affects the speed of the leakage. The percent of the speed remaining is calculated by the formula:

$$
Speed=\frac{100+\left(IR+1\right)}{1+\frac{0.16*hour^{2}}{IR+1}}-\left(IR+1\right)
$$

You can play with it here: [interactive chart](https://www.desmos.com/calculator/0mvkcqrmjx?lang=en)
{% endtab %}
{% endtabs %}

The Inertia Retention points can be obtained temporarily via the in-game boosters and permanently by burning additional keys (that were staked before) or acquiring a ship before a race starts.

{% hint style="info" %}
During the prelaunch phase, the Inertia Retention parameter of the ship will grow faster compared to the key staking. And the more keys are burned for the spaceship - the more the difference is. Each burned key reduces the period of getting a new Inertia Retention point by 15% relative to the staking.

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/Inertia Rewards.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The number of days that should pass to obtain a new Inertia Retention point for the ship during the prelaunch phase depends on the number of keys burned for the ship, and is calculated by the formula:

$$
DAYs=\frac{30}{KEYs}\cdot0.85^{KEYs}
$$

| Keys burned                     | Days till the new IR point |
| ------------------------------- | -------------------------- |
| 1 (applied for every spaceship) | 25.5                       |
| 2                               | 10.838                     |
| 3                               | 6.141                      |
| 4                               | 3.915                      |
{% endtab %}
{% endtabs %}
{% endhint %}

#### Spaceship Launch

Every ship is launched by the electromagnetic catapult obtaining the base speed, or in other words real inertia. The spaceship cannot lose this real, not artificial, inertia. So the ship does not fully stop when it loses its artificial inertia but continues to move with speed acquired by the primary acceleration. That means that even if you run out of Energons during the race, you will still continue to move towards the finish, though at a relatively low speed.

After each launch, the electromagnetic catapult loses its power, and each subsequent launch will accelerate the ships less. So it gives an advantage to those who will be the first.&#x20;

{% tabs %}
{% tab title="Chart" %}
<figure><img src="../.gitbook/assets/Catapult Power.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Details" %}
The first launch will give the spaceship a speed of 15 000 km/hour. Every next launch will be less effective. The catapult power for a particular launch can be calculated by the formula:

$$
Speed=\frac{1500000}{N+100}
$$
{% endtab %}
{% endtabs %}

{% hint style="info" %}
During the prelaunch phase, already joined pioneers will be waiting for the official race to start. Since they will launch at once, there will be a queue for the catapult. Every pioneer will have a particular score during prelaunch that will determine the place in the catapult queue. There are three ways to raise the score.

1. Burn better keys:\
   &#x20;\- key D gives +10 points\
   &#x20;\- key C gives +30 points \
   &#x20;\- key B gives +90 points \
   &#x20;\- key A gives +270 points
2. Burn keys as soon as possible. Those who burn keys (independent of the type) during the first day after opening the minting will receive +90 points. The next day key burn will give +89 points. Every day this reward will be reduced by one point.
3. &#x20;Elysium Team will use points as rewards for different community events.
{% endhint %}

## Spaceship Upgrade

By burning additional keys, you can improve the ship's parameters at any moment - during the prelaunch stage and after the race has already started. The parameters of the keys are added to the ship's parameters.

<figure><img src="../.gitbook/assets/Spaceship Upgrade.png" alt=""><figcaption></figcaption></figure>

There is a special bonus for burning 4 different types of keys (A, B, C, D) to improve one ship. When a spaceship is upgraded with all four types of keys, 20 points will be added to both parameters.

{% hint style="info" %}
Full Set Bonus can be applied for the ship only once.
{% endhint %}

<figure><img src="../.gitbook/assets/Prelaunch Special Offer.png" alt=""><figcaption></figcaption></figure>

## Flight Economics

In the Pioneer Program, we decided to recreate the Elysium tokenomics without simplifications to test it in real-life conditions before launching the blockchain. The only things we changed for the space race were to reduce the number of tokens to 100 000 and slightly accelerate the timing of the issuance.

Therefore, the relationship of Astonite -> Cosmogrinder -> Energon fully corresponds to the SKY -> Grinder -> RAY in Elysium tokenomics.

#### Astonite Mining

A unique mineral called Astonite is needed to obtain Energons. You can receive it during daily minigame tournaments. Unfortunately, the amount of Astonite is not only limited in the Universe but also constantly decreasing.

Astonite can be obtained in daily tournaments on the game "Astonite Mining." The event is held simultaneously for all participants. Astonite is distributed according to the tournament score. The tournament launch time will be shifted each day by one hour so that all pioneers will be in identical conditions.

These tournaments are the crucial mechanism to protect against multi-accounts. Since the competition will not last long (about 5-10 minutes) and will require all the player's attention, there will be no practical possibility of playing simultaneously from multiple accounts. And, of course, we will make it impossible to create a bot that can play instead of a human.

#### Obtaining Energons

Energons are obtained by recycling Astonite in a unique device called a "cosmogrinder." The higher the conversion rate - the harder it is for the cosmogrinder to proceed. That is why cosmogrinder will work faster if you offer less Energon for one Astonite.
