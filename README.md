
## About LiveLab | https://livelab.app
LiveLab is a browser-based media routing software designed for collaborative performance by [CultureHub](https://culturehub.org), a global art & technology community founded by SeoulArts & La MaMa.

It is a new tool that empowers artists  and arts presenters to meet, create, collaborate, rehearse, and ultimately produce multi-location performances from virtually anywhere in the world. This innovative video collaboration software expands the current field of offerings by allowing users to customize media in ways that best suit their needs.

**Feature highlights:**
- add multiple cameras, audio streams, and screen shares to the same session from one laptop
- dynamically add and remove audio and video feeds
- send video feeds to separate windows
- use audio mixer to control the master volume as well as the output volume of individual feeds
- video switcher to switch between video feeds
- chat, who doesn't like?



More info about LiveLab and how it is used in performance production by CultureHub, its creating organization: https://www.culturehub.org/livelab

## 🎉🎉 LiveLab 1.3.9 beta LAUNCHED!
LiveLab is open-source and free to use. To access:

1. go to https://livelab.app using Chrome Browser or Android tablet devices
2. Ensure the appropriate video and audio sources are selected
3. Click 'start' to join a room with a randomly generated room name
4. Share the URL with other people in order to add them to the session

## LiveLab Resources
### Tutorials
- [First Things to Know about LiveLab](https://github.com/CultureHub/LiveLab/issues/6)

### Signalling server
   To build and modify your own LiveLab signalling server that runs locally, check out our Github repo about [LiveLab Signalling Server](https://github.com/CultureHub/LiveLab_server)

To develop either version, type
```
npm run dev
```

# Changelog
## [1.3.10] - 2020-06-18
### Changed
 - switched to nanoid and randomIds rather than sequential
 - absolute path for preview images

## [1.3.9] - 2020-06-05
### Changed
 - added linter
 - cleaned up code
 - different range slider styling
 - added screen share icon

## [1.3.8] - 2020-06-03
### Added
 - toggle between floating layout and column layout in settings
 - colors as variables in layout
 - icons on landing page
 - font rektorant
 - button class
 - info to login page
 - buttons to login page
 - chat pops out when closed

### Changed
 - label removed from initial 'add media' page
 - accent color

## [1.3.6] - 2020-05-28
### Added
 - dev and production builds to specify different server address
 - version number included as environmental variable
 - settings panel
 - setting to configure number of switchers
 - column layout
 - overlay showing switcher value
 - x to end stream

### Changed
 - switcher can be toggled directly

## [1.3.4] - 2020-05-26
### Added
 - New layout for login
 - user info in 'peer list'
 - video grid adjusts to mobile layout
 - dedicated column for menu

### Changed
 - updated media settings
 - moved unused files to 'older'
 - media info removed from grid and added to peerslist

## [1.3.3] - 2020-05-22
### Changed
 - Add Media instead of addAudio()

## [1.3.2] - 2020-05-17
### Added
  - Global hangup
  - Switcher A and B
  - buttons for share, add video, add audio, help/info (non-functional)
  - Chat opens when a chat is received and window is closed
  - collapsible menu
  - 'advanced' and 'basic' menu
  - add audio with mic visualization

### Changed
  - Icons for bounding box, end call, share window
  - Audio mixer uses HTML elements rather than web audio ()

## [1.3.1] - 2020-05-12
### Added
  - hangup buttons for individual streams
  - indicator of number of users in room

## [1.3.0] - 2020-05-03
  Major refactor
### Changed
  - All state related to media streams contained in MultiPeer.js
  - choo stores only used for ui state
  - login, media settings, chat are all stateful components that only rerender when needed

### Fixed
  - bug on page load in safari

### Added
  - Audio mixer
  - popout window button
  - video mute
  - adaptive layout + layout controls
  - all users can see muted streams

## [1.2.5] - 2020-03-31
### Changed
 - scrollable track info
 - removed bandwidth info
 - no volume control for own audio
 - colors for muting and volume control

## [1.2.4] - 2020-03-31
### Added
 - controls for echoCancellation, autoGainControl, and noiseSuppressiong

## [1.2.3] - 2020-03-28
### Fixed
 - building and running the desktop on multiple platforms and without requiring nw.js to be installed globally

## [1.2.2] - 2020-03-28
### Added
 - screensharing

## [1.2.1] - 2020-03-27
### Added
 - room and nickname info saved to local storage
 - Room added to URL query params: '?room=roomName'. When using with sendOnly, follow format 'https://livelab.app?room=roomName#sendOnly'
 - Room name auto-populated on login page when specified in query

## [1.2.0] - 2020-03-26
### Added
 - client rejoins room when server is reconnected
 - [server update] added 'getPeers' function so that client can query for existing peers in room
 - client reconnects to peers when internet connection is rest

### Changed
 - Logs using built in Choo logging function, so that later it will be easier to show logs to user

### Fixed
  - Catch 'Ice Connection Failed' error -- removes ghost black screens

## [1.1.1] - 2020-02-12
### Fixed
 - Updated route for gh-pages

## [1.1.0] - 2020-02-12
### Added
- Interface for sending media without receiving, with separate route at #sendonly
- Flag for each peer 'requestMedia', indicating whether that peer should receive media
- Peers no longer send media by default, only when requested. (breaking change / not compatible with earlier versions)

## [1.0.2] - 2020-02-11
### Changed
- Updated choo devtools

## [1.0.1] - 2020-02-11
### Added
- Version number on login page
- Changelog

### Fixed
- Audio turning off when show control open
