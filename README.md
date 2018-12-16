# homebridge-securitysystem
Homebridge plugin that creates a security system accessory that can be triggered by HomeKit accessories.

## Installation
If you already have Homebridge installed, skip to step two!

1. Install homebridge using `npm install -g homebridge`.
2. Install the plugin using `npm install -g homebridge-securitysystem`.
3. Update your configuration file (see `sample-config.json`).

## Automations
Use Eve or a similar app to create automations like this:

| Trigger            | Condition                         | Action                        |
|--------------------|-----------------------------------|-------------------------------|
| Motion is detected | Security system is set to `Night` | Turn on `Siren`               |
| Door is opened     | Security system is set to `Away`  | Turn on `Siren`               |
| Button is pressed  | Security system is set to `Away`  | Set security system to `Home` |

## Additional information
An accessory called `Siren` that appears as a switch is used to trigger the security system. Changing modes while the security system is about to be triggered or already triggered will stop the alarm and continue its normal behaviour.
