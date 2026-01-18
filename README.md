# T.I.C.K
A standalone tool to generate launchers (.desktop, Steam shortcuts) for Bottles-based Windows games.

# T.I.C.K

**Target Input Compatible Kickoff**

T.I.C.K is a standalone tool to generate clean Linux launchers  
(`.desktop`, Steam shortcuts) for Windows games installed via **Bottles**.

It is designed to be used **independently**, or integrated as a building block
inside other frontends (such as BeHolder).

---

## What T.I.C.K does

- Detects Windows games installed inside Bottles
- Generates reliable launch scripts
- Creates `.desktop` launchers for Linux desktops
- Optionally adds non-Steam games to Steam
- Keeps a local database of created launchers (state, Steam status, stats)
- Can regenerate broken or outdated launchers

T.I.C.K focuses on **turning a Bottles game into a clean, launchable Linux entry**.

---

## What T.I.C.K does NOT do

- It is **not** a game library frontend
- It is **not** a launcher UI replacement
- It does **not** manage game installations
- It does **not** handle networking, LAN, or online features
- It does **not** try to abstract Proton/Wine internals beyond what is needed

Those responsibilities belong to higher-level tools.

---

## Standalone usage

T.I.C.K can be used on its own to:

- Create launchers for Bottles-based games
- Repair or regenerate existing launchers
- Add or remove games from Steam
- Manage `.desktop` entries without any external frontend

A graphical interface exists, but the project is designed so that
its core logic can be driven without depending on a specific UI.

---

## Integration philosophy

T.I.C.K is designed as a **reusable building block**.

Other applications can integrate it by:
- Calling its CLI
- Reusing its internal logic
- Treating it as a “launcher generator service”

T.I.C.K does not depend on BeHolder.  
BeHolder does not depend strictly on T.I.C.K.

They are designed to work **together**, but also to exist **independently**.

---

## License

T.I.C.K is licensed under the **GNU General Public License v3.0**.

See the `LICENSE` file for details.
