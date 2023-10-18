# README

## TrueNAS Info

TrueCharts can be installed as both *normal* Helm Charts or as Apps on TrueNAS SCALE.
However only installations using the TrueNAS SCALE Apps system are supported.
For more information about running this app on TrueNAS, please check the docs on the TrueCharts [website](https://truecharts.org/charts/stable/)

## General Threadfin Info

- Threadfin is a M3U proxy server for Plex, Emby, Jellyfin and other clients and providers, which support the .TS and .M3U8 (HLS) streaming formats.
- Threadfin emulates a SiliconDust HDHomeRun OTA tuner, which allows it to expose IPTV style channels to software, which would not normally support it.

## Features

### Recent Additions
- New Bootstrap based UI
- RAM based buffer instead of File based for enhanced performance 

### Filter Group
- Can now add a starting channel number for the filter group

### Map Editor
- Can now multi select Bulk Edit by holding shift
- Now has a separate table for inactive channels
- Can add 3 backup channels for an active channel (backup channels do NOT have to be active)
- Alpha Numeric sorting now sorts correctly
- Can now add a starting channel number for Bulk Edit to renumber multiple channels at a time
- PPV channels can now map the channel name to an EPG
- Removed old Threadfin buffer option, since FFMPEG/VLC will always be a better solution
## xTeVe Features
### Files
- Merge external M3U files
- Merge external XMLTV files
- Automatic M3U and XMLTV update
- M3U and XMLTV export
### Channel management
- Filtering streams
- Channel mapping
- Channel order
- Channel logos
- Channel categories
### Streaming
- Buffer with HLS / M3U8 support
- Re-streaming
- Number of tuners adjustable
- Compatible with Plex / Emby / Jellyfin EPG

see https://github.com/Threadfin/Threadfin for additional details

## Notes
- Threadfin (Linux - x86 64 bit ffmpeg) Support Runs as unprivileged user

## Default container paths
The default container from https://hub.docker.com/r/fyb3roptik/threadfin is configured with the following default environmental variables, for reference, here are the paths of the Threadfin installation:

| Variable               | Path                 |
|------------------------|----------------------|
| $THREADFIN_HOME        | /home/threadfin      |
| $THREADFIN_BIN         | /home/threadfin/bin  |
| $THREADFIN_CONF        | /home/threadfin/conf |
| $THREADFIN_CONF/data   | /home/threadfin/conf/data |
| $THREADFIN_CONF/backup | /home/threadfin/conf/backup |

## Parameters

| Parameter          | Description               | Valid Options                                                                                            | Default | Example                  |
|--------------------|---------------------------|----------------------------------------------------------------------------------------------------------|---------|--------------------------|
| THREADFIN_BRANCH   | Set Threadfin git branch  | [main or beta etc]  tags on <br/><a href="https://hub.docker.com/r/fyb3roptik/threadfin/tags">docker page</a> | main    | -e THREADFIN_BRANCH=beta |
| THREADFIN_DEBUG    | Set Threadfin debug level | [0-3] <br>0=off <br>3=most                                                                               | 0       | -e THREADFIN_DEBUG=0     |
| THREADFIN_PORT     | Set Threadfin port        | 1-30000                                                                                                  | 34400   | -e THREADFIN_PORT=34400  |



## Support

For Threadfin support join the discord discussion with the tean on
- https://github.com/Threadfin/Threadfin/discussions
<br>or
- https://hub.docker.com/r/fyb3roptik/threadfin 

For TreuNAS support
- Please check our [quick-start guides for TrueNAS SCALE](https://truecharts.org/manual/SCALE/guides/scale-intro).
- See the [Website](https://truecharts.org)
- Check our [Discord](https://discord.gg/tVsPTHWTtr)
- Open a [issue](https://github.com/truecharts/charts/issues/new/choose)

---

## Sponsor TrueCharts

TrueCharts can only exist due to the incredible effort of our staff.
Please consider making a [donation](https://truecharts.org/sponsor) or contributing back to the project any way you can!

*All Rights Reserved - The TrueCharts Project*
