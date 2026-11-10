# Lab 1 setup notes (rough)

## Session 1 — Tue 10 Nov 2026: Domain controller
- VirtualBox NAT Network SOCLAB 10.10.10.0/24, DHCP off
- DC01: Server 2022 Standard Eval (Core), 2 vCPU, 2 GB, 40 GB fixed disk
- sconfig: name DC01, static 10.10.10.10/24, GW 10.10.10.1, DNS 127.0.0.1, updates manual, TZ UTC+1
- AD DS + DNS: forest soclab.local (NetBIOS SOCLAB), DNS forwarders 1.1.1.1 / 8.8.8.8
- OU LabUsers: jdoe, asmith, svc_sql (svc_sql reserved for Kerberoasting in Lab 4)
- Lab-only test password; admin + DSRM passwords kept private

## Issues hit
- Re-booted from the ISO after install → Windows Boot Manager showed setup again. Fix: eject ISO, reset VM.
- Typo `netlogin` in Get-Service → corrected to `netlogon`.

## Time
- ~2 h total (install ~25 min on HDD)
