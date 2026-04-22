<p align="center">
  <img src="https://i.ibb.co.com/XZgQvY8/free-fire-logo.png" width="180" alt="Free Fire Squad Logo" />
</p>

<h1 align="center" style="font-family: 'Courier New', monospace; font-weight: 900;">
  🔥 IMAGINE.CORE // VISUAL SUITE 2026 🔥
</h1>

<p align="center">
  <img src="https://img.shields.io/badge/STATUS-UNDETECTED-success?style=for-the-badge&logo=accenture" />
  <img src="https://img.shields.io/badge/BOOYAH!-99%25-red?style=for-the-badge&logo=riotgames" />
  <img src="https://img.shields.io/badge/ImGui.Net-1.89.9-blueviolet?style=for-the-badge&logo=dotnet" />
  <img src="https://img.shields.io/badge/.NET-8.0-purple?style=for-the-badge&logo=dotnet" />
</p>

---

### 📊 STATISTIK SQUAD (RUNTIME ANALYTICS)

<table align="center">
  <tr>
    <td align="center" width="200">
      <h3 style="margin:0; color: #FFD700;">▐▐ 12.4k</h3>
      <small style="color:gray;">Total Render Calls</small>
    </td>
    <td align="center" width="200">
      <h3 style="margin:0; color: #00FF7F;">▐▐ 0.02ms</h3>
      <small style="color:gray;">Frame Time (Avg)</small>
    </td>
    <td align="center" width="200">
      <h3 style="margin:0; color: #FF4500;">▐▐ 144 FPS</h3>
      <small style="color:gray;">Locked</small>
    </td>
  </tr>
</table>

---

### 🧠 INTEGRASI IMGUI.NET / C# (STYLE XIOWU)

Buat lu yang nyari library visual tapi males pake *HTML murni* buat overlay cheat atau tools internal. Ini modul-modulnya di-*porting* langsung ke **ImGui.NET** style. Bisa lu embed di project C# WinForms atau WPF lu.

| Modul | Status ImGui | Deskripsi Singkat (Bahasa Tongkrongan) |
| :--- | :---: | :--- |
| `Diagram` | ✅ | Bikin flowchart buat alur **Aimbot** atau **Wallhack**. Pake `AddRectFilled`, `AddBezierCurve`, beres. |
| `Mockup` | ✅ | Bikin UI Form Login palsu buat **Phishing Panel** pake C#. Design clean, gak norak. |
| `Interactive`| 🔄 | Slider buat atur **Smooth Aim**, **FOV Circle**, langsung update di overlay. |
| `Chart` | ✅ | Visualisasi damage dealt pake **PlotLines** atau **PlotHistogram** di dalam game. |
| `Art` | ❌ | (Skip dulu, fokus ke fungsional cheat dulu) |

---

### 🛠️ SNIPPET KODE C# (IMPLEMENTASI OVERLAY)

```csharp
// XIOWU DEVELOPER - IMGUI.NET RENDER LOOP
// JANGAN LUPA SET 'IsOverlay = true' di WndProc

using ImGuiNET;

public unsafe void RenderVisuals()
{
    // Render Box ESP ala Diagram
    ImGui.GetForegroundDrawList().AddRect(
        new System.Numerics.Vector2(100, 100), 
        new System.Numerics.Vector2(200, 200), 
        ImGui.ColorConvertFloat4ToU32(new System.Numerics.Vector4(0.2f, 0.8f, 0.4f, 1.0f)), 
        0.0f, 
        ImDrawFlags.RoundCornersAll, 
        2.0f
    );

    // Render Statistik Kesehatan (Progress Bar)
    ImGui.GetForegroundDrawList().AddRectFilled(
        new System.Numerics.Vector2(80, 210), 
        new System.Numerics.Vector2(80 + (120 * 0.75f), 220), 
        ImGui.ColorConvertFloat4ToU32(new System.Numerics.Vector4(0.9f, 0.2f, 0.2f, 1.0f))
    );
    
    // Render Nama Player (Text)
    ImGui.GetForegroundDrawList().AddText(
        new System.Numerics.Vector2(100, 90), 
        ImGui.ColorConvertFloat4ToU32(new System.Numerics.Vector4(1f, 1f, 1f, 1f)), 
        "XIOWU_BOT [HEADSHOT]"
    );
}