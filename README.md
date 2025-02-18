# Chon Serial Port Emulator
|![](.imgs/cover.png)|
|:-:|
|It is a serial port emulator for communication between Multi-agent Systems and a Exogenous Environment in Simulated World.|

## Installation
1) Install the dependencies. On your Debian-like Linux machine, run:

```console
echo "deb [trusted=yes] http://packages.chon.group/ chonos main" | sudo tee /etc/apt/sources.list.d/chonos.list
sudo apt update
sudo apt install linux-headers-`uname -r`
sudo apt install chonos-serial-port-emulator
```

After the installation, by default, it will be instatiated on /dev 4 pairs of devices:

- /dev/ttyEmulatedPort0 <---> /dev/ttyExogenous0
- /dev/ttyEmulatedPort1 <---> /dev/ttyExogenous1
- /dev/ttyEmulatedPort2 <---> /dev/ttyExogenous2
- /dev/ttyEmulatedPort3 <---> /dev/ttyExogenous3

And so on. Writing on one device will make its content to be read on the other pair, and vice-versa

## Example
In a terminal window, execute the command below to put the emulated port waiting for incoming data

Open another terminal window and run the below command. On the first terminal Window. It should appear the message.

![Screenshot_20240117_201825](https://github.com/chon-group/dpkg-virtualport-driver/assets/32855001/3aefe904-f3cd-49a9-a6e8-91eeb423b245)

## Copyright
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />It is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>. The licensor cannot revoke these freedoms as long as you follow the license terms:

* __Attribution__ — You must give __appropriate credit__ like below:

FREITAS, Bruno Policarpo Toledo; LAZARIN, Nilson Mori; PANTOJA, Carlos Eduardo. Uma Proposta de Emulador de Portas Seriais para Sistemas Multiagentes Embarcados. In: WORKSHOP-SCHOOL ON AGENTS, ENVIRONMENTS, AND APPLICATIONS (WESAAC), 17. , 2023, Pelotas/RS. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2023 . p. 55-66. ISSN 2326-5434. URL: https://sol.sbc.org.br/index.php/wesaac/article/view/33437


<details>
<summary> Cite using Bibtex </summary>


```
@inproceedings{wesaac,
 author = {Bruno Freitas and Nilson Lazarin and Carlos Pantoja},
 title = {Uma Proposta de Emulador de Portas Seriais para Sistemas Multiagentes Embarcados},
 booktitle = {Proceedings of the 17th Workshop-School on Agents, Environments, and Applications},
 location = {Pelotas/RS},
 year = {2023},
 keywords = {},
 issn = {2326-5434},
 pages = {55--66},
 publisher = {SBC},
 address = {Porto Alegre, RS, Brasil},
 url = {https://sol.sbc.org.br/index.php/wesaac/article/view/33437}
}

```
</details>
