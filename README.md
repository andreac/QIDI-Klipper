# Table of Contents  
- [Table of Contents](#table-of-contents)
- [QIDI-Klipper](#qidi-klipper)
  - [BOM](#bom)
  - [Install ST Link v2 and upgrade](#install-st-link-v2-and-upgrade)


# QIDI-Klipper
Here i collect all my expertise on how to install klipper on our QIDI X-Plus. X-Max.

Starting from the work of Funkton and ecsv (thanks to them) i'm trying to collect every info on this page

## BOM

First of all you neead an ST-link v2 to dump and flash klipper.bin
you can buy from [amazon](https://www.amazon.it/gp/product/B07YX83NSL/ref=ppx_yo_dt_b_asin_title_o05_s00?ie=UTF8&psc=1) or [aliexpress](https://it.aliexpress.com/item/32887597480.html?spm=a2g0o.productlist.0.0.35235251njfsds&algo_pvid=8298341a-c818-41ff-bc0b-aa8cfb25572f&algo_exp_id=8298341a-c818-41ff-bc0b-aa8cfb25572f-3&pdp_ext_f=%7B%22sku_id%22%3A%2265696129095%22%7D&pdp_npi=2%40dis%21EUR%212.94%212.59%21%21%211.42%21%21%402100bdd816642914796751384e409f%2165696129095%21sea&curPageLogUid=54v8GDPXkiuv)

You need a raspberry. Starting from model 3b+ everythings works. If you don't want to use raspberry you can also use a minipc but you need ad [usb-ttl cable](https://www.amazon.it/gp/product/B083HVM7VZ/ref=ppx_yo_dt_b_asin_title_o00_s01?ie=UTF8&psc=1)

[Dupont cables](https://www.amazon.it/HeyNana-Dupont-Multicolore-maschio-femmina/dp/B0965R9J21/ref=sr_1_5?__mk_it_IT=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=AG7PRWLL9GE3&keywords=dupont&qid=1664291717&qu=eyJxc2MiOiI1LjM5IiwicXNhIjoiNC41MiIsInFzcCI6IjMuODgifQ%3D%3D&s=electronics&sprefix=dupont%2Celectronics%2C108&sr=1-5), to connect raspberry to mainboard or as said before usb-ttl cable


## Install ST Link v2 and upgrade

Following steps are for Ubuntu. I did some test with windows but i wasn't able to get stlink working correctly.

First of all download STM32cubeProg 2.7. Follow [this link](https://www.st.com/en/development-tools/stm32cubeprog.html#get-software)
on right select 2.7 version and download. When you press to download it ask you to register, follow registration steps and after you get STM32cubeProg.

Double click on SetupSTM32CubeProgrammer-2.7.0.linux and follow steps for installation.

Launch STM32cubeProg and plug STLink, click on refresh icon (top right) and you'll see a long number on Serial number. If you see it everything it's working.

![refresh and serial number](images/stlink_serial.png)

Close STM32CubeProg. Now you need to download STLINK007 to upgrade your ST-Link. Go to [Download page](https://www.st.com/content/my_st_com/en/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-programmers/stsw-link007.license=1664260122653.product=STSW-LINK007.version=3.10.3.html) and download latest version. Extract, inside AllPlatform you find STLinkUpgrade.jar, double click and it will open.

Unplug STLink and re-plug it, now click on refresh Device list and after click on Open in update mode.

Check if a new version of firmware are ready and in case press Upgrade

![stlink upgrade](images/stlinkupgrade.png)

In below image **Version** and **Update to Firmware** are the same so i don't need to upgrade.

let's go to next chapter, Dump current Firmware






