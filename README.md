# CTFd-Waves

A CTFd plugin to schedule the release of challenges in waves.

## Installation

1. Clone this repository into the `CTFd/plugins` folder of your CTFd deployment:
   ```bash
   cd CTFd/plugins
   git clone https://github.com/Osama-Yusouf/CTFd-Waves.git ctfd-waves
   ```
2. Restart your CTFd application.

## Usage

This plugin allows administrators to create "Waves" that specify a particular date and time to release a group of challenges. 

- Challenges assigned to a wave will be made visible automatically at the scheduled release time.
- Managed entirely via the CTFd Admin API.

## Requirements

- CTFd
- Flask
