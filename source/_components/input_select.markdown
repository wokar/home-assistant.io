---
layout: page
title: "Input Select"
description: "Instructions how to integrate the Input Select component into Home Assistant."
date: 2016-02-02 17:00
sidebar: true
comments: false
sharing: true
footer: true
logo: home-assistant.png
ha_category: Automation
ha_release: 0.13
---

The `input_select` component allows the user to define a list of values that can be selected via the frontend and can be used within conditions of automation. When a user selectes a new item, a state transition event is generated. This state event can be used in an `automation` trigger. 

To enable this platform, add the following lines to your `configuration.yaml`:

```yaml
# Example configuration.yaml entry
input_select:
  who_cooks:
    name: Who cooks today
    options:
     - Paulus
     - Anne Therese
    initial: Anne Therese
    icon: mdi:panda
  living_room_preset:
    options:
      - Visitors
      - Visitors with kids
      - Home Alone
```

Configuration variables:

- **[alias]** (*Required*): Alias for the input.
- **name** (*Optional*): Friendly name of the input.
- **options** array: List of options to choose from
- **initial** (*Optional*): Initial value when Home Assistant starts.
- **icon** (*Optional*): Icon for entry.

Pick an icon that you can find on [materialdesignicons.com](https://materialdesignicons.com/) to use for your input and prefix the name with `mdi:`. For example `mdi:car`, `mdi:ambulance`, or  `mdi:motorbike`.

