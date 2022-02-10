# Beerlicht

matelight + pixelflut = beerlicht

Visualize the [ghosts in the machines](https://en.wikipedia.org/wiki/Ghost_in_the_machine) as if they're [will-o'-the-wisps](https://en.wikipedia.org/wiki/Will-o%27-the-wisp).


## Goals

The goals for this project are to create a fun little way to visualize network traffic in a way that feels like having a lavalamp in your room.

How it works:
Currently I have a rough idea of how I want this to work using both IPv6 and IPv4.

IPv4:
Each pixel gets a unique IP address, and each each address has a daemon listening on all 65,535 ports.
Each port number corresponds to a 16-bit color when the port recieves a tcp/udp packet, it lights up to the color (and slowly fades back to dark)

IPv6 would work similarly to the above, but forego ports and just give everything a link-local ipv6 addr (so as to simplify it down to colors and pixels lighting up via icmpv6)
IPv6 will be able to do higher color fidelity, but these are LEDs on dirty beer bottles, so probably not a major driver.
It would be interesting to see if a raspberry pi can support a program that listens for pings on millions of ipv6 addresses. I do not know enough about networking to fully comprehend the implications here.

## Installation

At this time, it is only possible to install from source by cloning this repo.

```bash
git clone https://github.com/facklambda/beerlicht
```

## Usage

```bash
cargo run beerlicht
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

I'm new at this. :)

## License
[MIT](https://choosealicense.com/licenses/mit/)
