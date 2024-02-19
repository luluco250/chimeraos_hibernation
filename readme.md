# ChimeraOS Hibernation

This is an experimental script to setup hibernation in ChimeraOS.

## Usage

Simply download `setup_hibernation` somewhere in your filesystem, open a
console window, navigate to the folder where the file was downloaded with `cd`
and execute it with `bash setup_hibernation`.

You will be asked for your user password, which is `gamer` by default on
ChimeraOS. Simply type it and press enter when prompted (there won't be visual
feedback in the terminal).

## Features

Currently it sets up a swap file equal to the size of the Linux kernel's
default `image_size` (`cat /sys/power/image_size`) + 1mb for rounding.

This works when using `sudo systemctl hibernation`, though work is being done
to get it to work with the power button.

It may take a while for the device to actually hibernate, specially with higher
capacity RAM. Just be patient.

There are plans to investigate using larger image sizes, the trade-off would be
between losing more storage space due to the required swap file vs having
longer hibernation/resuming times.

## Warning

You are on your own if you choose to run this script, neither me nor the
ChimeraOS team is liable if it leads to data loss or hardware failure.
Do it at your own risk.
