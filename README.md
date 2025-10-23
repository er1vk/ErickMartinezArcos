# ErickMartinezArcos
 #!/usr/bin/env python3
"""Simple script to verify your repo was cloned correctly.

Run:
    python hello_github.py [--name YOUR_NAME]

It prints a friendly message and today's date/time.
"""

from __future__ import annotations
import argparse
from datetime import datetime
import platform

def main() -> None:
    parser = argparse.ArgumentParser(description="Say hello from your GitHub repo!")
    parser.add_argument("--name", "-n", default="there", help="Your name (optional)")
    args = parser.parse_args()

    now = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    print(f"👋 Hello, {args.name}!")
    print(f"✅ Your repo is working on Python {platform.python_version()}")
    print(f"🕒 Local time: {now}")
    print("💡 Tip: Try editing this file and pushing a new commit.")

if __name__ == "__main__":
    main()
