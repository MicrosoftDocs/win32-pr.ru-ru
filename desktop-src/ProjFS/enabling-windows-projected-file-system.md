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
# <a name="enabling-windows-projected-file-system"></a><span data-ttu-id="34938-103">Включение проектируемой файловой системы Windows</span><span class="sxs-lookup"><span data-stu-id="34938-103">Enabling Windows Projected File System</span></span>

<span data-ttu-id="34938-104">Прожфс поставляется с Windows в качестве дополнительного компонента.</span><span class="sxs-lookup"><span data-stu-id="34938-104">ProjFS ships with Windows as an Optional Component.</span></span>  <span data-ttu-id="34938-105">Чтобы поставщик мог использовать его, он должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="34938-105">Before a provider can use it, it must be enabled.</span></span>  <span data-ttu-id="34938-106">Вы можете использовать</span><span class="sxs-lookup"><span data-stu-id="34938-106">You can use</span></span> <!--the GUI or--> <span data-ttu-id="34938-107">Использование PowerShell для включения Прожфс.</span><span class="sxs-lookup"><span data-stu-id="34938-107">PowerShell to enable ProjFS.</span></span>

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a><span data-ttu-id="34938-108">Как включить Прожфс с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="34938-108">How to enable ProjFS using PowerShell</span></span>

<span data-ttu-id="34938-109">Чтобы использовать PowerShell для включения Прожфс, используйте `Enable-WindowsOptionalFeature` командлет в окне PowerShell с повышенными привилегиями:</span><span class="sxs-lookup"><span data-stu-id="34938-109">To use PowerShell to enable ProjFS use the `Enable-WindowsOptionalFeature` cmdlet in an elevated PowerShell window:</span></span>

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

<span data-ttu-id="34938-110">Перезагрузите компьютер, если Enable-WindowsOptionalFeature отчеты `RestartNeeded: True` .</span><span class="sxs-lookup"><span data-stu-id="34938-110">Reboot the computer if the Enable-WindowsOptionalFeature reports `RestartNeeded: True`.</span></span>
