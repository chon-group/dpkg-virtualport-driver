# Chon Serial Port Emulator
|![](https://github.com/user-attachments/assets/91bbdfee-daaf-4d65-807c-1e654c39c95c)|
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

FREITAS, Bruno Policarpo Toledo; LAZARIN, Nilson Mori; PANTOJA, Carlos Eduardo; VITERBO, José. Integrating Simulated Exogenous Environments to Support the Learning Process of the Embedded MAS Approach. In: WORKSHOP ON COMPUTING EDUCATION (WEI), 33. , 2025, Maceió/AL. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2025 . p. 1195-1206. ISSN 2595-6175. DOI: https://doi.org/10.5753/wei.2025.9115.


<details>
<summary> Cite using Bibtex </summary>


```
@inproceedings{wei,
 author = {Bruno Freitas and Nilson Lazarin and Carlos Pantoja and José Viterbo},
 title = { Integrating Simulated Exogenous Environments to Support the Learning Process of the Embedded MAS Approach},
 booktitle = {Proceedings of the 33rd Workshop on Computing Education},
 location = {Maceió/AL},
 year = {2025},
 keywords = {},
 issn = {2595-6175},
 pages = {1195--1206},
 publisher = {SBC},
 address = {Porto Alegre, RS, Brasil},
 doi = {10.5753/wei.2025.9115},
 url = {https://sol.sbc.org.br/index.php/wei/article/view/36252}
}

```
</details>
