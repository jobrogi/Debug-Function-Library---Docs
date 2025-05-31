# Debug Function Library – by Ghillie Studios

A powerful set of 15+ advanced Blueprint debugging tools designed to speed up development, improve visualization, and keep your workflow clean. From categorized logging to directional arrows, this is your new go-to utility for runtime debugging in UE5.4+.

> 🔧 Built for **Unreal Engine 5.3+**  
> 🧠 Ideal for solo devs, tool creators, or teams needing runtime insight  
> 💻 All nodes live in `Debug → Advanced` under Blueprint editor

---

## 🔧 Setup Instructions
Follow these steps to install and begin using the Debug Function Library in your Unreal Engine 5.3+ project.

1. Enable the Plugin
To activate the plugin in your project:

Open Edit → Plugins from the top menu bar.

In the Plugins window, search for Debug Function Library.

Enable the plugin by checking the box.

Restart the Unreal Editor (required the first time you enable the plugin).

✅ Once restarted, the plugin is fully loaded and ready for use.

2. Using the Debug Nodes in Blueprint
You can now begin integrating the debug tools into any Blueprint in your project:

Open or create a Blueprint Actor, Function Library, or any Blueprint class where you want to use debug tools.

In the Event Graph, Right-Click to open the Blueprint node context menu.

Navigate to Debug → Advanced to find all available debug nodes provided by the plugin.

Select and place the desired debug node into your graph.

💡 All nodes are organized under a single category for quick access.

3. (Optional) Visual Guide
To make setup even easier, here are step-by-step images showing the process:

✅ [Insert Image: Plugin Enabled in Plugin Browser]

✅ [Insert Image: Right-Click in Graph → Debug → Advanced]

✅ [Insert Image: Node placed and ready for use]

## 🧩 Function Overview

Below is a full list of Blueprint nodes included in the library:

| Function | Purpose |
|---------|---------|
| `PrintDebug` | Prints a category-tagged message to screen/log based on dev settings. |
| `PrintDebugAutoCategory` | Automatically tags messages with the calling object's name. |
| `DrawDebugTextAtActor` | Draws floating text at an actor’s location with custom offset. |
| `DebugTraceResult` | Performs a trace and logs the result onscreen and in the log. |
| `PrintActorInfo` | Outputs actor name and location to the screen. |
| `DrawDebugCapsuleSimple` | Draws a single capsule with color, size, and orientation. |
| `DrawDebugArrowFromActor` | Draws directional arrow (Forward, Backward, Up, Down, etc.) from actor. |
| `DrawDebugPath` | Connects an array of points with debug lines (great for pathfinding). |
| `DrawDebugSphereArray` | Draws a series of debug spheres for visualizing many points. |
| `HighlightActorOnce` | Draws a debug box around an actor’s bounds. |
| `LogActorComponentHierarchy` | Logs the actor's component tree to console/log. |
| `RunDebugConsoleCommand` | Executes a console command and stores it in the debug log. |
| `GetRecentDebugMessages` | Returns the full runtime history of recent debug messages. |
| `ClearAllDebugLines` | Clears all persistent debug visuals from the current world. |
| `SetDebugCategoryEnabled` | Enables/disables individual categories for runtime control. |
| `IsDebugCategoryEnabled` | Checks if a specific debug category is currently active. |

---

## 🗃️ File Logging Location

Using the `LogDebugToFile()` function? Here's where your saved logs end up:

- **Folder Path:** `[YourProject]/Saved/[FolderName]/[FileName].txt`
- For example: `Saved/Logs/GameplayDebug.txt`

You can specify both the folder and file name via Blueprint when calling the function.

✅ Log messages are timestamped and appended to the file.  
✅ The log folder will auto-create if it doesn’t exist.

This is useful for saving runtime debug sessions for review after a crash, playtest, or session reset.

## 📂 How Debug Categories Work

You can use `SetDebugCategoryEnabled("MyCategory", false)` to toggle off a category and mute all associated messages or visuals. Every log respects its category status before displaying.

---

## 🗂️ Debug Message History

Every function in this library automatically logs its activity to a **runtime-accessible message history**, retrievable via `GetRecentDebugMessages`.

The system stores up to 50 recent messages.

---

## ❓ Frequently Asked Questions

**Q: Where do I find Debug Function Library nodes in Blueprint?**  
**A:** All nodes are under the `Debug → Advanced` category in the Blueprint context menu.

**Q: Will these functions work in packaged builds?**  
**A:** No. All debug logic is excluded from shipping builds via `#if !UE_BUILD_SHIPPING`.

**Q: Can I filter or disable debug messages during runtime?**  
**A:** Yes! Use `SetDebugCategoryEnabled(CategoryName, false)` to toggle any category on/off dynamically.

**Q: Is this safe to use in multiplayer or networked projects?**  
**A:** Yes. These nodes are strictly visual/debug-only and have no gameplay side effects.

---

## 📞 Support

Need help or want to request a feature?

Email: `Jobrogi@gmail.com`

---

## 🔐 License

This plugin is sold for commercial and personal use. Redistribution or resale of source code is prohibited.

---

Made by Ghillie Studios
