---
title: Включение проектируемой файловой системы Windows
description: Описание включения Прожфс в Windows
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: f903192190877631084e366bcaeafd8b5b0e7e72
ms.sourcegitcommit: 42cdae4d2eca84713ab3f7a5c88f583a352991a8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/23/2019
ms.locfileid: "105671992"
---
# <a name="enabling-windows-projected-file-system"></a>Включение проектируемой файловой системы Windows

Прожфс поставляется с Windows в качестве дополнительного компонента.  Чтобы поставщик мог использовать его, он должен быть включен.  Вы можете использовать <!--the GUI or--> Использование PowerShell для включения Прожфс.

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a>Как включить Прожфс с помощью PowerShell

Чтобы использовать PowerShell для включения Прожфс, используйте `Enable-WindowsOptionalFeature` командлет в окне PowerShell с повышенными привилегиями:

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

Перезагрузите компьютер, если Enable-WindowsOptionalFeature отчеты `RestartNeeded: True` .
