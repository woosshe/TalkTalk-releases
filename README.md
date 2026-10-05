# TalkTalk

[English](#english)

같은 네트워크에 있는 사람끼리 **중앙 서버 없이** 대화하고 파일을 주고받는 데스크톱 메신저입니다.

대화는 서버를 거치지 않고 두 PC 사이에서 직접 오갑니다.<br>
계정도 가입도 없습니다. 같은 네트워크 망에 붙어 있으면 자동으로 목록에 서로가 나타납니다.

## 받기

오른쪽 **Releases** 에서 설치본을 받습니다.<br>
서명하지 않은 설치본이라 Windows SmartScreen 경고가 뜹니다.<br>
'추가 정보' > '실행' 을 누르세요.

## 0.4.0 - 2026-10-05

채팅 목록을 분류해서 보는 **태그**와, 실수하면 안 되는 대화방을 지키는 **입력창 잠금** 기능이 추가되었습니다.

### 추가

- **대화 태그** - 채팅 목록 위에 전체 · 안읽음 · 내 태그가 탭으로 놓입니다
  - 대화를 오른쪽 클릭해 '태그'에서 붙이고 뗍니다. 한 대화에 태그를 여러 개 붙일 수 있습니다
  - 탭 줄 끝의 + 로 태그를 만들고, 태그 탭을 오른쪽 클릭해 이름 바꾸기 · 차례 바꾸기 · 삭제가 가능합니다
  - 태그를 삭제해도 대화는 유지됩니다.
  - 안읽음과 태그 탭에 안 읽은 메시지 수가 뜹니다
  - 탭이 많으면 드래그나 휠로 스크롤 됩니다.
- **입력창 잠금** - 실수하면 안 되는 대화방에 켜 두면 자물쇠를 한 번 눌러야 입력할 수 있습니다
  - 대화창 메뉴나 채팅 목록의 오른쪽 클릭에서 '입력창 잠금'으로 켜고 끕니다
  - 한 번 보내면 다시 잠깁니다. 다른 대화에 다녀오면 쓰던 글이 지워진 채 잠겨 있습니다
  - 잠긴 대화는 채팅 목록과 대화창 제목 옆에 자물쇠가 보입니다
- **대화창 메뉴의 '알림 설정'에서도 알림을 켜고 끕니다**

### 바뀜

- **대화창 메뉴를 정리했습니다** - 자주 쓰는 것만 두고, 알림 설정과 나머지(더 보기)는 하위 메뉴로 옮겼습니다
- **메뉴의 켜기 · 끄기 항목은 눌러도 메뉴가 닫히지 않습니다** - 알림, 입력창 잠금, 태그를 연달아 바꿀 수 있습니다
- **'안 읽은 대화만 보기' 단추가 '안읽음' 탭으로 바뀌었습니다**
- **일체형 창에서 친구 탭으로 대화를 열면 왼쪽이 채팅 목록으로 넘어갑니다**

### 수정

- **일부 스티커가 수정되었습니다**
- **대화창 이름 수정 버튼 위치가 어긋나던 것을 조정했습니다**
- **상대가 꺼져 있을 때 입력칸 아래 안내가 단어 중간에서 줄이 바뀌지 않습니다**

지난 버전은 [변경 이력](CHANGELOG.md)에 있습니다.

---

<a id="english"></a>

# TalkTalk

[한국어](#talktalk)

A desktop messenger for people on the same network to chat and share files **without a central server**.

Messages go straight between two PCs without passing through a server.<br>
No accounts, no sign-up. Anyone on the same network shows up in your list automatically.

## Download

Get the installer from **Releases** on the right.<br>
The installer is not signed, so Windows SmartScreen shows a warning.<br>
Click 'More info' > 'Run anyway'.

## 0.4.0 - 2026-10-05

**Tags** to filter the chat list, and an **input lock** that guards chats where you can't afford a mistake.

### Added

- **Chat tags** - All, Unread and your own tags sit as tabs above the chat list
  - Right-click a chat and use 'Tags' to add or remove them. A chat can have several tags
  - Create a tag with the + at the end of the tab bar. Right-click a tag tab to rename, reorder or delete it
  - Deleting a tag keeps its chats.
  - The Unread tab and tag tabs show how many messages are unread
  - With many tabs, drag or use the mouse wheel to scroll.
- **Input lock** - turn it on for chats where you can't afford a mistake, and you click the lock once before typing
  - Turn it on or off with 'Lock input' in the chat menu or by right-clicking the chat in the list
  - It locks again after each message you send. Leave for another chat and come back, and your draft is cleared and locked
  - Locked chats show a lock in the chat list and next to the chat title
- **Mute and unmute from 'Notifications' in the chat menu too**

### Changed

- **The chat menu is tidier** - only the everyday items stay, and Notifications and the rest (More) moved into submenus
- **On/off items no longer close the menu** - flip notifications, input lock and tags one after another
- **The 'Show unread only' button became the Unread tab**
- **In the single window, opening a chat from the Friends tab switches the list to Chats**

### Fixed

- **Some stickers were touched up**
- **Fixed the misaligned rename button next to the chat name**
- **The note under the input box when the other person is offline no longer breaks a word across lines**

Earlier versions are in the [changelog](CHANGELOG.en.md).
