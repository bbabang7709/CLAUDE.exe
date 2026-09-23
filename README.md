# CLAUDE.exe

> 클로드가 토큰을 잡아먹을 뿐인 시뮬레이션 게임.

---

## 🎮 Game Overview

**CLAUDE.exe**는 평범한 사무직 직장인의 일상을 배경으로 한  
**가상 OS 기반 사무 업무 시뮬레이션 게임**입니다.

플레이어는 회사에서 각종 서류 정리와 사무 업무를 수행하며 **Token**을 획득합니다.

그리고 이 Token을 사용해 AI 프로그램 **Claude.exe**에게 업무를 맡길 수 있습니다.

하지만 Claude에게 일을 시키는 것 역시 공짜가 아닙니다.

> **Claude는 일을 대신해주지만, Token을 소비합니다.**

Claude가 업무를 완료하면 **Credit**을 획득할 수 있으며,  
Credit을 사용하여 Claude의 능력을 강화할 수 있습니다.

---

## 💡 Core Gameplay Loop

~~~text
┌──────────────────┐
│   Office Work    │
│   직접 업무 수행   │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│      Token       │
│      획득         │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│    Claude.exe    │
│    업무 위임       │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│   Token 소비      │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│   Task Complete  │
│   업무 완료        │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│     Credit       │
│      획득          │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ Claude Upgrade   │
│ 효율 / 능력 강화   │
└────────┬─────────┘
         │
         └───────────────┐
                         │
                         ▼
                   더 어려운 업무
~~~

---

# 🖥️ Virtual OS

게임 전체는 가상의 컴퓨터 화면을 통해 진행됩니다.

플레이어는 실제 운영체제를 사용하는 것처럼 다양한 프로그램을 사용할 수 있습니다.

예정된 프로그램:

- 📁 File Explorer
- 📝 Notepad
- 📊 Spreadsheet
- 📧 Mail
- 🖥️ Terminal
- 🤖 Claude.exe
- ⚙️ Settings

게임 내부의 파일과 폴더는 실제 OS의 파일 시스템이 아닌  
**Virtual File System**을 통해 관리됩니다.

예:

~~~text
C:\
│
├── Documents
│   ├── Report.txt
│   └── Meeting.docx
│
├── Downloads
│   ├── Invoice_01.xlsx
│   └── Invoice_02.xlsx
│
└── Company
    │
    ├── HR
    ├── Finance
    ├── Sales
    └── Projects
~~~

---

# 🤖 Claude.exe

Claude.exe는 플레이어의 업무를 대신 처리하는 게임 내 AI 프로그램입니다.

처음부터 모든 업무를 수행할 수 있는 것은 아닙니다.

Claude의 능력과 효율을 성장시키면서 점점 더 복잡한 업무를 처리할 수 있게 됩니다.

### 초기 능력

- 파일 이동
- 파일 이름 변경
- 폴더 생성
- 간단한 문서 정리

### 성장 후

- 대량 파일 처리
- 문서 분석
- 여러 문서 간 정보 비교
- 스프레드시트 처리
- 이메일 정리
- 복합 업무
- 반복 업무 자동화

---

# 🧠 Claude Growth System

Claude는 업무를 완료하면 **Credit**을 획득합니다.

Credit을 사용하여 Claude의 능력을 강화할 수 있습니다.

~~~text
                    CLAUDE CORE
                         │
             ┌───────────┼───────────┐
             │           │           │
             ▼           ▼           ▼
          Efficiency   Intelligence  Access
             │           │           │
             ▼           ▼           ▼
         Token Cost    Task Level   File Access
           감소          증가          증가
             │           │           │
             ▼           ▼           ▼
          Automation   Complex      System
                       Tasks        Permission
~~~

## Upgrade Examples

### Efficiency

- Token Compression
- Batch Processing
- Parallel Processing
- Autonomous Workflow

### Intelligence

- Basic Analysis
- Document Understanding
- Cross Reference
- Complex Reasoning

### Access

- Documents Access
- Company Folder Access
- Spreadsheet Access
- Mail Access
- Database Access
- Administrator Access

---

# 💰 Economy

게임에는 두 가지 주요 자원이 존재합니다.

## Token

Claude가 업무를 수행하기 위해 사용하는 자원입니다.

플레이어가 직접 업무를 수행하면 Token을 획득할 수 있습니다.

~~~text
Player Work
     │
     ▼
   Token
     │
     ▼
Claude Task
     │
     ▼
Token 소비
~~~

---

## Credit

Claude가 업무를 성공적으로 완료하면 획득할 수 있습니다.

Credit은 Claude의 능력을 강화하는 데 사용됩니다.

~~~text
Claude Task
     │
     ▼
Task Complete
     │
     ▼
 Credit
     │
     ▼
Claude Upgrade
~~~

---

# 📋 Task System

업무는 `TaskDefinition`을 기반으로 관리합니다.

Unity의 `ScriptableObject`를 사용하여 업무 데이터를 관리할 예정입니다.

예:

~~~text
Task Definition

Name:
거래처 문서 정리

Difficulty:
2

Token Cost:
15

Credit Reward:
4

Duration:
12 sec
~~~

업무 난이도가 높아질수록 필요한 Claude 능력도 증가합니다.

---

# 📂 Virtual File System

실제 OS의 파일 시스템과 분리된 게임 전용 파일 시스템을 사용합니다.

핵심 클래스:

~~~text
VirtualFileSystem
│
├── VirtualFolder
│   ├── VirtualFolder
│   └── VirtualFile
│
└── VirtualFile
~~~

### 주요 클래스

~~~text
VirtualFile
VirtualFolder
VirtualFileSystem
FileSystemPath
FileType
~~~

파일 시스템의 변경사항은 게임 세이브 데이터에 포함됩니다.

---

# 🪟 Window System

게임의 모든 애플리케이션은 Window System을 통해 관리됩니다.

~~~text
WindowManager
│
├── FileExplorer
├── Notepad
├── Spreadsheet
├── Mail
├── Terminal
└── Claude
~~~

각 프로그램은 `GameWindow`를 상속합니다.

~~~text
GameWindow
    │
    ├── FileExplorerWindow
    ├── NotepadWindow
    ├── SpreadsheetWindow
    ├── MailWindow
    ├── TerminalWindow
    └── ClaudeWindow
~~~

WindowManager는 다음 기능을 담당합니다.

- Window Open
- Window Close
- Window Focus
- Window Z-Order
- Window Registration

---

# 🏗️ Architecture

프로젝트는 다음과 같은 계층 구조를 사용합니다.

~~~text
Presentation
     │
     ▼
Application
     │
     ▼
Domain
     │
     ▼
Infrastructure
~~~

## Presentation

Unity UI와 직접 연결되는 영역입니다.

~~~text
Presentation/
├── Desktop/
├── WindowSystem/
├── FileExplorer/
├── Claude/
└── HUD/
~~~

---

## Application

게임의 주요 Use Case를 처리합니다.

~~~text
Application/
├── FileSystem/
├── Economy/
├── Claude/
└── Tasks/
~~~

예:

~~~text
ClaudeWindow
      │
      ▼
ClaudeService
      │
      ▼
EconomyService
      │
      ▼
TokenWallet
~~~

UI가 직접 게임 데이터를 변경하지 않도록 구성합니다.

---

## Domain

게임의 핵심 규칙과 데이터를 담당합니다.

~~~text
Domain/
├── FileSystem/
├── Economy/
├── Claude/
└── Tasks/
~~~

Unity에 대한 의존성을 최대한 줄이는 것을 목표로 합니다.

---

## Infrastructure

게임 외부와 연결되는 시스템입니다.

~~~text
Infrastructure/
├── SaveSystem/
└── Persistence/
~~~

예:

- Save / Load
- JSON Serialization
- File Persistence

---

# 📁 Project Structure

~~~text
Assets/
│
├── _Game/
│   │
│   ├── Core/
│   │   ├── Bootstrap/
│   │   ├── Events/
│   │   ├── Save/
│   │   └── Time/
│   │
│   ├── Domain/
│   │   │
│   │   ├── FileSystem/
│   │   │   ├── VirtualFile.cs
│   │   │   ├── VirtualFolder.cs
│   │   │   ├── VirtualFileSystem.cs
│   │   │   ├── FileType.cs
│   │   │   └── FileSystemPath.cs
│   │   │
│   │   ├── Economy/
│   │   │   ├── TokenWallet.cs
│   │   │   ├── CreditWallet.cs
│   │   │   └── CurrencyType.cs
│   │   │
│   │   ├── Claude/
│   │   │   ├── ClaudeState.cs
│   │   │   ├── ClaudeStats.cs
│   │   │   ├── ClaudeTask.cs
│   │   │   └── ClaudeUpgrade.cs
│   │   │
│   │   └── Tasks/
│   │       ├── OfficeTask.cs
│   │       ├── TaskDefinition.cs
│   │       └── TaskResult.cs
│   │
│   ├── Application/
│   │   │
│   │   ├── FileSystem/
│   │   │   └── FileSystemService.cs
│   │   │
│   │   ├── Economy/
│   │   │   └── EconomyService.cs
│   │   │
│   │   ├── Claude/
│   │   │   ├── ClaudeService.cs
│   │   │   ├── ClaudeTaskExecutor.cs
│   │   │   └── ClaudeUpgradeService.cs
│   │   │
│   │   └── Tasks/
│   │       └── TaskService.cs
│   │
│   ├── Presentation/
│   │   │
│   │   ├── Desktop/
│   │   │
│   │   ├── WindowSystem/
│   │   │   ├── WindowManager.cs
│   │   │   ├── GameWindow.cs
│   │   │   └── WindowType.cs
│   │   │
│   │   ├── FileExplorer/
│   │   │   ├── FileExplorerWindow.cs
│   │   │   ├── FileIconView.cs
│   │   │   └── FileContextMenu.cs
│   │   │
│   │   ├── Claude/
│   │   │   ├── ClaudeWindow.cs
│   │   │   ├── ClaudeMessageView.cs
│   │   │   ├── ClaudeTaskView.cs
│   │   │   └── ClaudeStatusView.cs
│   │   │
│   │   └── HUD/
│   │       ├── TokenView.cs
│   │       └── CreditView.cs
│   │
│   ├── Infrastructure/
│   │   ├── SaveSystem/
│   │   └── Persistence/
│   │
│   └── Data/
│       ├── Files/
│       ├── Tasks/
│       ├── Claude/
│       └── Upgrades/
│
└── Scenes/
    ├── Boot.unity
    └── Main.unity
~~~

---

# 🧩 Core Classes

## VirtualFile

~~~csharp
public sealed class VirtualFile
{
    public string Id { get; }
    public string Name { get; private set; }
    public FileType Type { get; }

    public VirtualFolder Parent { get; private set; }

    public string Content { get; private set; }

    public void Rename(string newName)
    {
        Name = newName;
    }

    public void MoveTo(VirtualFolder target)
    {
        Parent?.RemoveFile(this);

        Parent = target;
        target.AddFile(this);
    }
}
~~~

---

## VirtualFolder

~~~csharp
public sealed class VirtualFolder
{
    public string Id { get; }
    public string Name { get; private set; }

    public VirtualFolder Parent { get; private set; }

    public IReadOnlyList<VirtualFile> Files { get; }
    public IReadOnlyList<VirtualFolder> Folders { get; }

    public void AddFile(VirtualFile file)
    {
        // ...
    }

    public void AddFolder(VirtualFolder folder)
    {
        // ...
    }
}
~~~

---

## ClaudeService

~~~csharp
public sealed class ClaudeService
{
    public ClaudeState State { get; private set; }

    public ClaudeStats Stats { get; }

    public bool TryExecute(TaskDefinition task)
    {
        // 1. 작업 가능 여부 확인
        // 2. Token 비용 계산
        // 3. Token 차감
        // 4. Task 실행
        // 5. 완료 후 Credit 지급

        return true;
    }
}
~~~

---

# 🔄 Claude Task Flow

~~~text
Player
  │
  │ "거래처 파일 정리"
  ▼
ClaudeWindow
  │
  ▼
ClaudeService
  │
  ├── Check Difficulty
  │
  ├── Calculate Token Cost
  │
  ▼
EconomyService
  │
  └── Spend Token
  │
  ▼
ClaudeTaskExecutor
  │
  ├── Execute Task
  │
  ├── Modify Virtual File System
  │
  └── Create TaskResult
  │
  ▼
ClaudeService
  │
  └── Reward Credit
  │
  ▼
ClaudeWindow
  │
  └── Update UI
~~~

---

# 💾 Save System

게임 진행 상황은 저장되어야 합니다.

저장 대상:

~~~text
GameSaveData
│
├── Virtual File System
│   ├── Files
│   └── Folders
│
├── Economy
│   ├── Token
│   └── Credit
│
├── Claude
│   ├── Level
│   ├── Efficiency
│   ├── MaxTaskDifficulty
│   └── Upgrades
│
└── Tasks
    ├── Completed Tasks
    └── Active Tasks
~~~

Virtual File System은 실제 C# 객체를 그대로 저장하지 않고  
Save DTO로 변환하여 JSON으로 저장하는 것을 목표로 합니다.

예:

~~~csharp
[Serializable]
public class FileSaveData
{
    public string id;
    public string name;
    public FileType type;
    public string parentId;
    public string content;
}
~~~

---

# 🛠️ Tech Stack

| Category | Technology |
|---|---|
| Engine | Unity 6 |
| Language | C# |
| UI | Unity UI / TextMeshPro |
| Data | ScriptableObject |
| Save | JSON |
| Version Control | Git / GitHub |
| Architecture | Domain / Application / Presentation / Infrastructure |

---

# 🚧 Development Roadmap

## Phase 1 — Core Prototype

- [ ] Unity 6 Project Setup
- [ ] GameBootstrap
- [ ] VirtualFile
- [ ] VirtualFolder
- [ ] VirtualFileSystem
- [ ] WindowManager
- [ ] Basic Desktop UI
- [ ] File Explorer
- [ ] Token System
- [ ] Credit System
- [ ] Claude.exe
- [ ] Basic Claude Task

### 목표

> 플레이어가 파일을 직접 정리해서 Token을 얻고,  
> Claude에게 Token을 지불하여 파일 정리를 맡길 수 있다.

---

## Phase 2 — Task System

- [ ] TaskDefinition
- [ ] TaskResult
- [ ] Task Difficulty
- [ ] Task Reward
- [ ] Task Duration
- [ ] Task Failure
- [ ] Task Progress UI
- [ ] Task History

---

## Phase 3 — Claude Growth

- [ ] Claude Level
- [ ] Efficiency Upgrade
- [ ] Task Difficulty Upgrade
- [ ] File Access Upgrade
- [ ] Batch Processing
- [ ] Parallel Processing
- [ ] Automation

---

## Phase 4 — Office OS

- [ ] Notepad
- [ ] Spreadsheet
- [ ] Mail
- [ ] Terminal
- [ ] Search
- [ ] Notifications
- [ ] Clipboard
- [ ] Multiple Windows
- [ ] Context Menu

---

## Phase 5 — Advanced Tasks

- [ ] Document Analysis
- [ ] Spreadsheet Tasks
- [ ] Email Tasks
- [ ] Cross-Document Tasks
- [ ] Complex Office Tasks
- [ ] Automated Workflows

---

## Phase 6 — Game Content

- [ ] Daily Workload
- [ ] Random Tasks
- [ ] Company Events
- [ ] Coworkers
- [ ] Boss Requests
- [ ] Performance Evaluation
- [ ] Story Events
- [ ] Claude Personality
- [ ] Claude Dialogue

---

# 🎯 First Playable Goal

프로젝트의 첫 번째 목표는 거대한 시스템을 완성하는 것이 아닙니다.

다음 하나의 루프를 실제로 플레이할 수 있게 만드는 것입니다.

~~~text
┌─────────────────────────────┐
│                             │
│       Player Desktop        │
│                             │
│   📁 Downloads              │
│   📁 Company                │
│   🤖 Claude.exe             │
│                             │
└──────────────┬──────────────┘
               │
               ▼
       직접 파일 정리
               │
               ▼
          + TOKEN
               │
               ▼
          Claude.exe
               │
               ▼
       업무 선택 / 실행
               │
               ▼
          - TOKEN
               │
               ▼
      Claude 작업 진행
               │
               ▼
       실제 파일 변경
               │
               ▼
          + CREDIT
               │
               ▼
       Claude Upgrade
               │
               └───────────────►
~~~

이 루프가 완성되면 이후의 모든 시스템은  
이 기반 위에 확장합니다.

---

# 📌 Design Principles

### 1. Fake OS, Real Game State

겉으로는 운영체제처럼 보이지만,  
내부적으로는 게임이 모든 데이터를 통제합니다.

### 2. UI와 Game Logic 분리

UI는 게임 규칙을 직접 처리하지 않습니다.

~~~text
UI
 ↓
Service
 ↓
Domain
~~~

### 3. Virtual File System First

실제 파일 시스템에 의존하지 않습니다.

모든 파일 조작은 게임 내부의 Virtual File System을 통해 이루어집니다.

### 4. Data Driven

업무와 업그레이드는 가능한 한 ScriptableObject 기반으로 관리하여  
코드 수정 없이 새로운 콘텐츠를 추가할 수 있도록 합니다.

### 5. Expandable Architecture

초기에는 간단한 파일 정리 게임으로 시작하지만,  
향후 다음 시스템을 추가할 수 있도록 설계합니다.

~~~text
File System
     +
Applications
     +
Tasks
     +
Claude
     +
Economy
     +
Automation
     +
Story
~~~

---

# 📜 License

TBD

---

# 🚀 Project Status

**Early Development**

현재 프로젝트는 핵심 시스템 및 아키텍처 설계 단계입니다.

첫 번째 목표는 다음 기능을 포함하는  
**Playable Core Prototype**입니다.

- Virtual File System
- File Explorer
- Window Manager
- Token / Credit Economy
- Claude.exe
- Basic Task System
- Claude Upgrade

---

> **CLAUDE.exe**
>
> 당신의 업무를 대신해드립니다.
>
> 물론, 무료는 아닙니다.
