====================================
HOW DO I CREATE A DLL FOR KSP?
====================================

1. Install Visual Studio Community.

2. Start Visual Studio.

3. Click:
   File -> New -> Project

4. Select:
   Class Library (.NET Framework)

5. Give your project a name.
   Example:
   DangerMod

6. Add KSP references:

   Right-click "References"
   -> Add Reference
   -> Browse

   Select:

   KSP_Data\Managed\Assembly-CSharp.dll
   KSP_Data\Managed\UnityEngine.dll

7. Write your code.

   Example:

   using UnityEngine;

   namespace DangerMod
   {
       [KSPAddon(KSPAddon.Startup.Flight, false)]
       public class DangerMod : MonoBehaviour
       {
           void Start()
           {
               Debug.Log("[Danger Mod] Loaded!");
           }
       }
   }

8. Build the DLL.

   Build -> Build Solution

   or

   Ctrl + Shift + B

9. Find the DLL.

   The file will usually be located in:

   bin\Debug\DangerMod.dll

   or

   bin\Release\DangerMod.dll

10. Place the DLL in KSP.

   GameData
   └─ DangerMod
      └─ Plugins
         └─ DangerMod.dll

11. Start KSP.

12. Check KSP.log.

   If everything works, you should see:

   [Danger Mod] Loaded!

====================================
DONE!
You now have a working KSP DLL.
====================================
