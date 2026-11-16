# CTF-Waves 🌊

**CTF challenge scheduling through timed release waves.**

CTF-Waves is a Python plugin for [CTFd](https://github.com/CTFd/CTFd) that enables competition administrators to organize challenges into scheduled release waves.

Instead of making every challenge available at the beginning of a competition, administrators can control when specific groups of challenges become visible to participants.

## ✨ Features

- **Scheduled Challenge Releases** – Configure specific dates and times for challenge releases.
- **Wave Management** – Organize multiple challenges into independent release waves.
- **Automatic Visibility** – Assigned challenges automatically become visible when their scheduled release time arrives.
- **Admin API** – Create, retrieve, delete, and manage waves through administrative API endpoints.
- **Background Scheduler** – Automatically checks for pending releases and processes scheduled waves.
- **Cache Invalidation** – Clears the CTFd cache after releases to reflect updated challenge visibility.

## ⚙️ How It Works

1. An administrator creates a wave with a name and release date/time.
2. Challenges are assigned to that wave.
3. The background scheduler monitors scheduled waves.
4. When the release time arrives, the assigned challenges become visible.
5. The wave is marked as released.

## 📦 Installation

Clone the repository into your CTFd plugins directory:

```bash
cd CTFd/plugins
git clone https://github.com/0xWh173/CTF-Waves.git ctfd-waves
```

Restart your CTFd application to load the plugin.

## 🔌 API Endpoints

All endpoints require administrator access.

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/v1/waves` | Retrieve all waves |
| POST | `/api/v1/waves` | Create a new wave |
| DELETE | `/api/v1/waves/{wave_id}` | Delete a wave |
| POST | `/api/v1/waves/{wave_id}/challenges` | Assign challenges to a wave |

### Create a Wave

```json
{
  "name": "Wave 1",
  "release_time": "2026-12-01T12:00:00Z"
}
```

### Assign Challenges

```json
{
  "challenge_ids": [1, 2, 3]
}
```

## 🛠️ Technology Stack

- Python
- Flask
- CTFd
- SQLAlchemy

## 📁 Project Structure

```text
CTF-Waves/
├── __init__.py
├── models.py
└── README.md
```

## 🎯 Use Cases

- Progressive challenge releases during CTF competitions.
- Time-based competition progression.
- Scheduled difficulty progression.
- Controlled challenge availability for participants.

## 📄 License

No license has been specified yet.

---

**CTF-Waves** – Bringing structure and timing to CTF challenge releases. 🌊
