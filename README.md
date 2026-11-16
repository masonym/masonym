# masonym

> development, infrastructure, and the occasional homelab rabbit hole

hey, i'm mason. a full-stack developer based in vancouver, bc. i write code, mostly with typescript, next.js, and aws, and i try to make stuff that actual humans use! i spent a while learning the "safe" stuff like react, and lately i've been stepping outside the box: c# data tooling, self-hosting on my own hardware, and everything inbetween with agents.

## what i'm building

### [maplestory tools](https://masonym.dev/)
a platform of tools for the MMORPG *MapleStory*, used by 50k+ players a month. built with next.js and fed by a custom ETL pipeline (c# + python) that pulls equipment, maps, familiars, damage skins and more straight out of the raw game client files, then diffs them between patches. it's the project i enjoy most, so it's also the one i spend the most time on. there's always another tool to add.

### [american defense alliance](https://www.americandefensealliance.org)
event platform for a company that runs defense industry conferences. i'm the sole engineer: i replaced a stalled no-code build with a next.js site in about two weeks, and it's since grown into a small internal platform:
- paid registration with stripe checkout (multiple ticket types, add-ons, early-bird pricing, promo codes), with webhooks that validate orders, write attendees to google sheets, and send confirmation emails
- an admin portal staff use directly to manage speakers, sponsors, schedules and promo codes, with direct-to-s3 uploads
- a playwright suite that runs every ticket type against real stripe test charges before an event goes live
- sanity cms + dynamodb for content, s3 + cloudfront for media, and a move to cloudflare workers via opennext in progress

### [med spa booking + ecommerce platform](https://www.phace.ca/)
custom booking, cart and checkout for a small medical aesthetics business. it talks to square's appointments and web payments apis directly to get around the default jank, so clients can book services with add-ons and buy products in one flow. it also has an admin side for the calendar and client consent forms, backed by aws (dynamodb, cognito, ses) and deployed with cdk.

## on the side

- **self-hosted fitness hub**: a personal fork of [liftosaur](https://github.com/astashov/liftosaur) running on a thin client at home. i swapped the aws backend for dynamodb local + docker, and added food logging, adaptive tdee, nutrition graphs, and an MCP server so claude can analyze my training and diet
- **homelab**: the same box runs home assistant and a matrix/synapse server behind caddy. it has 3gb of ram, so every service has to earn its spot

## what i know

- **languages**: typescript / javascript, python, c#, php
- **frontend**: react, next.js, tailwind
- **backend**: node.js, django, stripe, square
- **infra**: aws (lambda, dynamodb, s3, cloudfront, api gateway, cdk), vercel, cloudflare (workers, dns), docker, linux / self-hosting, nix / nixos
- **tools**: neovim (btw 🤓), git (hopefully a given), playwright

## reach me

- **site**: [masonleitch.dev](https://masonleitch.dev)
- **github**: [github.com/masonym](https://github.com/masonym) (you're already here!)
- **email**: [nosamleitch@gmail.com](mailto:nosamleitch@gmail.com)
