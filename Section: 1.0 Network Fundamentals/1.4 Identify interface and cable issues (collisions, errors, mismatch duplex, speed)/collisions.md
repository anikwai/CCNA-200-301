
# Carrier Sense Multiple Access - Collision Detection (CSMA/CD)
In order to prevent collisions as much as possible, Ethernet uses a set of rules known as Carrier Sense Multiple Access - Collision Detection (which is abbreviated as CSMA/CD). These rules are critical to half-duplex Ethernet communications.

## What is the order of operations for an Ethernet transmission using CSMA/CD?
  1. Listen to the medium to ensure it is clear
  2. Start transmitting
  3. Listen for a collision
  4. Send a jamming signal if needed


# Late Collisions
If a collision comes after the initial 64B are transmitted, this is known as a late collision, and it indicates that there is a major problem with the network.

The expectation is that an Ethernet transmitter is fully occupying the medium after 64B of transmission. Normal collisions cannot occur at this point because all devices should be able to see the incoming transmission. If another device starts transmitting this late, something has gone terribly wrong! And this creates the late collision.

## What is the Byte threshold for a collision vs late collision?
  - 64B

# Collision Domains
As we just saw, collisions occur when multiple devices attempt to send on a shared medium at the same time. A location on the network where collisions can occur is known as a collision domain.

A network hub operates at L1 and replicates any signal received on any port to all other ports. Connecting dozens of hosts through hubs creates a shared medium and therefore increases the likelihood of collisions being present.

A hub lacks intelligence.

  ## At what layer does a network hub operate?
    - L1

# Ethernet Switches
Ethernet switches change how traffic is propagated by operating at L2. This results in creating more collision domains and drastically reducing the likelihood of collisions occurring. In this video we are still presuming the use of half-duplex, as we introduce the use of the L2 switch.

- Collision domains reduced to two(2) i.e between host and switch

## Using a network switch eliminates the possibility of collisions. True or false?
  - False because we still have 2 collision domains

# Half-duplex and Full-duplex Operations
Half-duplex operation is critical for when a medium is being shared. However, what happens when there is no shared medium in use? This creates an opportunity to run in full-duplex!


<img width="682" alt="1" src="https://github.com/anikwai/CCNA-200-301/assets/15828026/a0dd9710-1431-4f89-b1a5-344ee00daa54">

To summarize the Ethernet spec support for half/full duplex:

 - 10Mbps requires half-duplex

 - 100Mbps can run in either half-duplex or full-duplex (full-duplex requires point-to-point switch connections with no hubs)

 - 1000Mbps allows for supporting both (per the spec), but Cisco devices only support full-duplex

 - Anything above 1000Mbps will not support half-duplex operation


# Ethernet Broadcasts
Switches create collision domain boundaries, but they allow for the propagation of broadcasts. Routers and L3 interfaces create broadcast domain boundaries, thus allowing us to properly scale networks and prevent 1000s of hosts from existing within a single broadcast domain.

<img width="682" alt="2" src="https://github.com/anikwai/CCNA-200-301/assets/15828026/1683dc51-2366-400b-bb34-f3964bb1f428">

## What is the L2 broadcast address for Ethernet frames?
Ans: FF:FF:FF:FF:FF:FF

## If a network consists of a single 48-port switch, how many broadcast domains are present by default?
Ans: 1



