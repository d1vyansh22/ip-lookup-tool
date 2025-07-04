# Redis Setup and Management on Ubuntu/WSL2

## 1. Install Redis
```sh
sudo apt update
sudo apt install redis-server
```

## 2. Start the Redis Service
```sh
sudo service redis-server start
# or
sudo systemctl start redis-server
```

## 3. Enable Redis to Start on Boot (Optional)
```sh
sudo systemctl enable redis-server
```

## 4. Check Redis Status
```sh
sudo systemctl status redis-server
# or
redis-cli ping
# Should return: PONG
```

## 5. (Optional) Configure Redis
- Config file: `/etc/redis/redis.conf`
- For development, you may want to set `supervised systemd` in the config.

## 6. Stop/Restart Redis
```sh
sudo systemctl stop redis-server
sudo systemctl restart redis-server
```

## Notes
- All commands should be run **inside the Ubuntu WSL2 terminal**.
- For most development, Redis will be accessible at `localhost` inside WSL2.
- If you need to access Redis from Windows, adjust the `bind` and `protected-mode` settings in the config file and check your firewall.

---
*This file is for developer reference only. Do not commit sensitive information.* 