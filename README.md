# RHCSA-9.6

Total Marks: 300

Total Time: 3 hrs

Total number of Questions=20-22

You have 2VMs, serverA & serverB

In serverA root password is set, and networking is not configured.

In serverB, the password must be changed with the new password provided, but the network is ready.

NTP need to be configured in only one system, not both.

YUM Repository need to be  configured in both systems.

Firewall and SELinux will both be pre-enabled.

The container question is Mandatory.

AutoFS question is Mandatory.


How the Grading system works

When you finish the RHCSA exam, your machine is wiped and a grading script runs against the VM image you worked on. It doesn’t care how you did the task, only whether the final state matches Red Hat’s expected outcome.

🔎 What the grading script checks

Filesystems & Storage

Are LVMs created with correct names/sizes?

Are partitions mounted at correct mountpoints?

Are entries in /etc/fstab correct and persistent?

For XFS/ext4, does resizing match the requirement?

Users & Groups

Does the user exist with correct UID/GID?

Is the password set (even hashed in /etc/shadow)?

Are group memberships correct?

Are umasks / default perms / ACLs applied properly?

Permissions / SELinux

Do files/dirs have the right perms (chmod/chown)?

Are SELinux contexts correct (ls -Z check)?

If asked, are booleans set (e.g. httpd_enable_homedirs)?

Networking / Firewall

Is the IP persistent in /etc/NetworkManager/system-connections/?

Can the system ping a test host?

Is firewalld running, with correct services/ports open?

System Services

Are services enabled/disabled as required?

Is automount (autofs) configured properly?

Do cron/systemd timers exist and execute?

Podman (Container tasks)

Is the image present locally (podman images)?

Is the container running with correct name/options?

Do bind mounts exist with :Z relabel?

If systemd required → is the unit file generated and enabled?

General Checks

Are the configs persistent after reboot (the script simulates a reboot)?

Are there syntax errors in config files?

⚖️ How scoring works

Each task = 1 unit (some bigger tasks might count as 2).

You either get full credit for a task, or zero (no step-by-step marks).

The passing threshold = 210/300 (70%).

So if you missed 1–2 tasks but nailed the rest, the script still gives you full marks for everything else.

📌 Important

The script doesn’t care about style (e.g., nmcli vs editing config files).

If something worked only until reboot but not after → ❌ fail that task.

If a single option is wrong (e.g., wrong mount path, wrong port) → ❌ whole task marked wrong.

✅ So right now, your VM image is sitting in Red Hat’s system being tested by this script. Once it’s done, the result is pushed to your certification profile and emailed to you.

