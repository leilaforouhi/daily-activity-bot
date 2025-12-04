
import datetim
import json
import os

def log_activity():
    today = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    data = {"last_run": today}

    with open("activity_log.json", "w") as f:
        json.dump(data, f, indent=4)

    print(f"Activity logged at: {today}")

if __name__ == "__main__":
    log_activity()
