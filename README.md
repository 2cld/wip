wip.2cld.net
[edit](https://github.com/2cld/wip/edit/main/README.md)

# Today
- ~~Identify critial nodes verity documents~~
  - [https://cf.2cld.net/docs/wf](https://cf.2cld.net/docs/wf)
  - [https://cf.2cld.net/docs/ng2](https://cf.2cld.net/docs/ng2)
  - [https://sl.2cld.net/docs/devices](https://sl.2cld.net/docs/devices) issue with direct access
- WAN ~~map networks~~
  - gh [https://my.zerotier.com/](https://my.zerotier.com/)
  - ct [https://dash.cloudflare.com/](https://dash.cloudflare.com/)
- sl ~~Verify manual monitor access~~
  - [https://traefik.2cld.com/](https://traefik.2cld.com/)
  - [https://gitea.2cld.com/](https://gitea.2cld.com/)
  - [https://portainer.2cld.com/](https://portainer.2cld.com/)
  - slcp - sl cockpit [https://slcp.2cld.com/](https://slcp.2cld.com/)
- wf ~~Verify manual monitor access~~
  - [https://gitea.klopfenstein.org/](https://gitea.klopfenstein.org/)
  - [https://sg.klopfenstein.org/](https://sg.klopfenstein.org/)
  - [https://metube.klopfenstein.org/](https://metube.klopfenstein.org/)
  - joplin wd [https://jp.klopfenstein.org/](https://jp.klopfenstein.org/)
- plex [https://tv.2cld.net/](https://tv.2cld.net/) ~~Verify manual monitor access~~
  - [https://www.plex.tv/](https://www.plex.tv/)
    - cfTV
    - slPlex
    - wfTube
- ~~get doorbells back online~~
- build monitor ??
- wireguard to trink vps ?
- tbd
## sl stuff [sl.2cld.net](https://sl.2cld.net/)
- having issues with sl network  ssl to wsl ssh -p 2222 ghadmin@10.147.17.94
- ~~currently [portainer](https://portainer.2cld.com/), [gitea](https://gitea.2cld.com/) [slcp - sl cockpit](https://slcp.2cld.com/) ha and traefik are running under wsl on slwin11ops~~
- [slcp - sl cockpit](https://slcp.2cld.com/) is having issues with javascript over cf [googleai - fix](https://www.google.com/search?udm=50&aep=11&atvm=1&q=I%27m+a+network+admin+working+on+using+cockpit+to+access+a+vm+through+Traeffik+and+I%27m+getting+the+following+error%3A%0A%0APlease+enable+JavaScript+to+use+the+Web+Console.&mtid=GfetaNjwDv6qw8cP08fb0QE&mstk=AUtExfBwEopM_vL7eTWigtYwJCSYxBiWuHHqTiVd1K3eajOB7cTax4odN2D5-hsCtyv2HCVmY-9fbbUib3MryGieiQTKBQr_M_KnCGRLuArcBhR9M4d4JcgHQqhmmIt0IU-kNm8-JFUvK8CHo1ExS_iO_3hpLInkhpUoXQE6xCpJtA7BdT12ETfKm3o05B-p-1sBJW5Nlfw4Av5KOXKcAN6lPBta3eGjqafQSUP9O0Wx0j-N2OQYMu48D3CmG-TtUz3I1EV5v0VvpDbgBqIwrc7efymwOwK_kIW52CY&csuir=1)
- I have *.2cld.com [sl-2cld cftunnel](https://one.dash.cloudflare.com/830c41d5976453f0c03f34d4f765b229/networks/tunnels) running on slwinllops
- gitea.2cld.com (slops) does seem to work but I don't remember how I sync test works
- need to spin gus up on backups
- Need cleanup docs on [sl.2cld.net](https://sl.2cld.net/)
  - [https://sl.2cld.net/docs/devices](https://sl.2cld.net/docs/devices)
  - [https://sl.2cld.net/docs/services](https://sl.2cld.net/docs/services)
  - [https://sl.2cld.net/docs/storage](https://sl.2cld.net/docs/storage)
- Neet to cleanup [tv.2cld.net](https://tv.2cld.net)
- tbd
## wf stuff [cf.2cld.net/docs/wf](https://cf.2cld.net/docs/wf)
- Fired up wf-proxmox - power fail restart failure... need to figure out
- need to put security crap back online in wf
- thinking I should nuke wsl and go with docker on ubuntu vm with cockpit (that's what I had started on wf-proxmox)
- [https://192.168.9.3:8006/](https://192.168.9.3:8006/) proxmox-wf
- [https://192.168.9.102:9090/](https://192.168.9.102:9090/) cockpit 11scat-102-proxmox
- Network cleanup
    - ~~Update network docs~~ [https://netstack.org/docs/portals/netbox/](https://netstack.org/docs/portals/netbox/)
    - ssh setups
      - cfub2204vm on CyberTruck Hyper-V vm cfub2204vm 10.147.17.126
      - ssh ghadmin@10.147.17.126 -> ghadmin@cfub2204vm:~$ pwd /home/ghadmin
      - ssh ghadmin@10.147.17.223 -> ghadmin@mg2:~$ pwd /home/ghadmin
      - mg2 nsUb2404 on SLWIN11OPS Hyper-V vm 10.147.17.135
      - ssh -p 2222 ghadmin@10.147.17.94 -> 
    - sl site [https://sl.2cld.net/](https://sl.2cld.net/)
      - ssh -p 2222 ghadmin@10.147.17.94 -> cf-wfw-proxy-wsl2 SLWIN11OPS into wsl
      - ssh ghadmin@10.147.17.135 -> mg2 nsUb2404 on SLWIN11OPS Hyper-V vm
      - [https://portainer.2cld.com/](https://portainer.2cld.com/) via [sl-2cld cloudflare](https://one.dash.cloudflare.com/830c41d5976453f0c03f34d4f765b229/networks/tunnels)
      - access sl docker via remotedesktop.g in wsl
        ```
        ghadmin@slwin11ops:~/docker/docker-compose$ pwd
        /home/ghadmin/docker/docker-compose
        ghadmin@slwin11ops:~/docker/docker-compose$
        ```
    - cf site [https://cf.2cld.net/](https://cf.2cld.net/)
      - 10.147.17.219 CyberTruck
    - wf site [https://cf.2cld.net/docs/wf](https://cf.2cld.net/docs/wf)
      - 10.147.17.165 devwin10
      - ?? proxmox
      - ?? cfDVR
      - ?? storage
    - Install netbox in sl
    - sort out [cf tunnels](https://one.dash.cloudflare.com/830c41d5976453f0c03f34d4f765b229/networks/tunnels)
    - stand up netbox
    - fix plex and sort out storage and backup
    - sort out docs with gus
- Setup local n8n 
  - ~~View tutorial~~
  - ~~Create n8n service project~~ on [netstack.com edit portals n8n](https://github.com/2cld/netstack/tree/master/docs/portals)
  - ~~Create n8n install~~ [https://netstack.org/docs/portals/n8n/](https://netstack.org/docs/portals/n8n/)
  - get a test docker node running in cf and sl
    - [https://sl.2cld.net/](https://sl.2cld.net/)
    - [https://cf.2cld.net/](https://cf.2cld.net/)
    - Update network docs [https://netstack.org/docs/portals/netbox/](https://netstack.org/docs/portals/netbox/)
    - Document [zt cat-ghadmin-grid](https://my.zerotier.com/network/d5e5fb65371eb4a4)
  - update n8n deployment document and service maps
    - [https://sl.2cld.net/docs/services](https://sl.2cld.net/docs/services)
    - [https://cf.2cld.net/docs/services](https://cf.2cld.net/docs/services)
  - Setup in sl and cf use and update [2cld.net](https://2cld.net/)
  - create plex monitoring [netstack plex edit](https://github.com/2cld/netstack/tree/master/docs/portals/plex)
- Figure out hwpc old db data
  - review old code on [https://hwpc.2cld.net/](https://hwpc.2cld.net/)
  - look for old dev vm ?
  - setup google sheet like old db and get import / export working
  - use n8n to export old hwpc data to google sheets ??
- Cleanup Keep notes ghadmin
- wip for me, steve, candy, brian, kenton
- Setup Steve Testing
- Setup Candy Testing
- [hwpc-bug](https://github.com/grasshorse/hwpc-bug)
- [hwpc-gs](https://github.com/grasshorse/hwpc-gs)

# SOON que
- Land Tax
- LLC Accounting

# Active
- [https://github.com/grasshorse/hwpc-gs](https://github.com/grasshorse/hwpc-gs) Pest Control Service Management
  - [https://hwpc.2cld.net/](https://hwpc.2cld.net/) 
- [https://github.com/grasshorse/hwpc-bug](https://github.com/grasshorse/hwpc-bug) cuke testing for hwpc-gs
- [https://drive.google.com/drive/home](https://drive.google.com/drive/home) start clearing

# Testing
- [kiro.dev download](https://kiro.dev/downloads/) ai chat
  - [docs](https://kiro.dev/docs/getting-started/)
  - [.kiro/steering/*.md](https://kiro.dev/docs/steering/) steering docs <-- **trink note**
- Warp [https://www.warp.dev/](https://www.warp.dev/)
- Replit [https://replit.com/](https://replit.com/)
- autonomai (like replit) [https://autonomyai.io/](https://autonomyai.io/)
- claude code [https://claude.ai/](https://claude.ai/)
- Google stuff
  - [http://google.com/aimode](http://google.com/aimode)
  - [https://notebooklm.google.com/](https://notebooklm.google.com/)
  - [https://keep.google.com/](https://keep.google.com/)
  - [https://script.google.com/home](https://script.google.com/home)
  - [https://colab.research.google.com/](https://colab.research.google.com/)
  - [https://console.cloud.google.com/](https://console.cloud.google.com/)
  - [https://code.google.com/](https://code.google.com/)
- [https://symless.com/synergy/account](https://symless.com/synergy/account)
- [https://cursor.com/en](https://cursor.com/en)

# paused
- [USD](./usd/)

# wip doc
- [docs](./docs/)

# Done delete soon
- ~~Cleanup [hwpc-bug](https://github.com/grasshorse/hwpc-bug) api test~~
  - ~~backup working test db~~ C:\Users\ghadmin\code\hwpc-gs\backend\database\zdbbackup\20250815-hwpc-bug-pass
  - ~~rebuild db seed and check db structure~~
  - ~~looneyTunesTest C:\Users\ghadmin\code\hwpc-gs\backend\database\zdbbackup\looneyTunesTest~~
    - ~~customers.json~~
    - ~~routes.json~~
    - ~~tickets.json~~
    - ~~users.json~~ 
  - ~~manual looneyTunesTest update~~
  - ~~set api test data to special looneyTunesTest customers, tickets and routes~~
  - ~~make api feature test work with new seed~~
  - ~~retest db resets and db migration~~
- ~~Cleanup Keep notes christrees~~
- ~~Cleanup hwpc-gs and hwpc-bug looneyTunesTest-v1~~
  - ~~hwpc-bug~~ [hwpc-bug main looneyTunesTest-vi commit f622](https://github.com/grasshorse/hwpc-bug/commit/a66fa91af593ce26cbf2c24f03f8c7fea5aff622)
  - ~~hwpc-gs~~ [hwpc-gs hwpc-site-test-target looneyTunesTest-v1 commit 00f0b77](https://github.com/grasshorse/hwpc-gs/commit/00f0b773a25ea9a3684eac65b368bb0b27b8f614)
  - out of kiro credits for the month

