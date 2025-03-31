# ha-ump-fix

There is no `Announcement`, `Enqueue` and `Extra` exposed for the `play_media` command in the original [Universal Media Player](https://www.home-assistant.io/integrations/universal/) component, this tries to fix that.

```yaml
media_player:
  - platform: ha_ump_fix
    unique_id: testmediaplayer
    name: TestMediaPlayer
    device_class: speaker
    commands:
      play_media:
        action: system_log.write
        data:
          level: critical
          message: "Announce={{announce}} Enqueue={{enqueue}} Extra={{extra}}"
```

![image](https://github.com/user-attachments/assets/4a82d7f1-8791-45c8-a024-f2c4f04fdde4)
