---
title: Универсальное приложение пользовательской точки управления
description: Приложение универсальной точки управления пользователя (UCP) позволяет обнаруживать устройства, управлять обнаруженными устройствами и просматривать связанные сведения о событиях, используя графический интерфейс.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104557666"
---
# <a name="generic-user-control-point-application"></a><span data-ttu-id="eb743-103">Универсальное приложение пользовательской точки управления</span><span class="sxs-lookup"><span data-stu-id="eb743-103">Generic User Control Point Application</span></span>

<span data-ttu-id="eb743-104">Приложение универсальной точки управления пользователя (UCP) позволяет обнаруживать устройства, управлять обнаруженными устройствами и просматривать связанные сведения о событиях, используя графический интерфейс.</span><span class="sxs-lookup"><span data-stu-id="eb743-104">The generic user control point (UCP) application allows you to discover devices, control those discovered devices, and view the related eventing information, all using a graphical interface.</span></span>

<span data-ttu-id="eb743-105">**Запуск универсального приложения управления служебной программой**</span><span class="sxs-lookup"><span data-stu-id="eb743-105">**To start the generic UCP application**</span></span>

1.  <span data-ttu-id="eb743-106">Создайте и настройте образцы \\ нетдс \\ UPnP \\ женерикукп \\ cpp \\devtype.txt файл (или \\ \\ файлdevtype.txt VisualBasic) со сведениями об устройстве.</span><span class="sxs-lookup"><span data-stu-id="eb743-106">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\devtype.txt file (or the \\VisualBasic\\devtype.txt file) with device information.</span></span> <span data-ttu-id="eb743-107">Этот файл позволяет настроить общую точку управления служебной программой для поиска "найти по типу" и "Async Find".</span><span class="sxs-lookup"><span data-stu-id="eb743-107">This file allows you to configure the generic UCP for the "find by type" and "async find" searches.</span></span> <span data-ttu-id="eb743-108">Каждая строка файла должна содержать тип устройства и связанное с ним описание.</span><span class="sxs-lookup"><span data-stu-id="eb743-108">Each line of the file must contain a device type and the related description.</span></span> <span data-ttu-id="eb743-109">Пример:</span><span class="sxs-lookup"><span data-stu-id="eb743-109">For example:</span></span>

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    <span data-ttu-id="eb743-110">Этот пример предназначен для вымышленного устройства проигрывателя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="eb743-110">This example is for a fictitious media player device.</span></span> <span data-ttu-id="eb743-111">"Проигрыватель мультимедиа" в конце второй строки не является частью типа устройства, он предназначен для информационных целей в универсальном приложении управления служебной программой (UCP).</span><span class="sxs-lookup"><span data-stu-id="eb743-111">The "Media Player" at the end of the second line is not a part of the device type, it is for informational purposes in the Generic UCP application.</span></span> <span data-ttu-id="eb743-112">То же относится и к "всем корневым устройствам" в первой строке.</span><span class="sxs-lookup"><span data-stu-id="eb743-112">The same applies to "All Root Devices" in the first line.</span></span>

    <span data-ttu-id="eb743-113">Добавьте строку, содержащую сведения о конкретном типе устройства и его описание для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="eb743-113">Add a line that contains your specific device type and description for each device.</span></span>

2.  <span data-ttu-id="eb743-114">Создайте и настройте образцы \\ нетдс \\ UPnP \\ женерикукп \\ cpp \\udn.txt файл (или \\ \\ файлudn.txt VisualBasic) с информацией УДН для своих устройств.</span><span class="sxs-lookup"><span data-stu-id="eb743-114">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\udn.txt file (or the \\VisualBasic\\udn.txt file) with UDN information for your devices.</span></span> <span data-ttu-id="eb743-115">Этот файл позволяет настроить общую точку управления служебной программой для поиска "найти по УДН".</span><span class="sxs-lookup"><span data-stu-id="eb743-115">This file allows you to configure the generic UCP for the "find by UDN" search.</span></span> <span data-ttu-id="eb743-116">Каждая строка использует следующую форму:</span><span class="sxs-lookup"><span data-stu-id="eb743-116">Each line uses the following form:</span></span>

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    <span data-ttu-id="eb743-117">Добавьте строку, которая содержит определенные УДН для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="eb743-117">Add a line that contains your specific UDN for each device.</span></span>

3.  <span data-ttu-id="eb743-118">Запустите GenericUCP.exe.</span><span class="sxs-lookup"><span data-stu-id="eb743-118">Run GenericUCP.exe.</span></span> <span data-ttu-id="eb743-119">Появится **универсальное окно управления служебной программой (UCP** ).</span><span class="sxs-lookup"><span data-stu-id="eb743-119">The **Generic UCP** window appears.</span></span>

    ![универсальное окно управления служебной программой](images/generic-ucp.png)

> [!Note]  
> <span data-ttu-id="eb743-121">В примере кода C++ не реализована функция **View Presentation** и **View Service DESC.**</span><span class="sxs-lookup"><span data-stu-id="eb743-121">The **View Presentation** and **View Service Desc.** functionality is not implemented in the C++ sample code.</span></span>

 

 

 




