---
description: Коллекция — это объект, содержащий один или несколько объектов. Коллекции обеспечивают эффективный способ группирования схожих объектов. Получение образа Windows (WIA) предоставляет коллекции для объектов DeviceInfo и Item.
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: Использование объектов коллекции WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22aa959547647070c733b8c3f81dd1181243bcb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692409"
---
# <a name="using-wia-collection-objects"></a><span data-ttu-id="5f56d-105">Использование объектов коллекции WIA</span><span class="sxs-lookup"><span data-stu-id="5f56d-105">Using WIA Collection Objects</span></span>

<span data-ttu-id="5f56d-106">Коллекция — это объект, содержащий один или несколько объектов.</span><span class="sxs-lookup"><span data-stu-id="5f56d-106">A collection is an object that contains one or more objects.</span></span> <span data-ttu-id="5f56d-107">Коллекции обеспечивают эффективный способ группирования схожих объектов.</span><span class="sxs-lookup"><span data-stu-id="5f56d-107">Collections provide an efficient way of grouping similar objects.</span></span> <span data-ttu-id="5f56d-108">Получение образа Windows (WIA) предоставляет коллекции для объектов [**DeviceInfo**](-wia-deviceinfo.md) и [**Item**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="5f56d-108">Windows Image Acquisition (WIA) provides collections for the [**DeviceInfo**](-wia-deviceinfo.md) and [**Item**](-wia-item.md) objects.</span></span>

<span data-ttu-id="5f56d-109">Коллекции используются для перечисления содержащихся в них объектов.</span><span class="sxs-lookup"><span data-stu-id="5f56d-109">Use collections to enumerate the objects they contain.</span></span> <span data-ttu-id="5f56d-110">Например, следующий пример на языке VBScript получает коллекцию объектов [**DeviceInfo**](-wia-deviceinfo.md) из метода [**Devices**](-wia-iwia-devices.md) , а затем использует **для... Каждый** цикл для итерации по коллекции:</span><span class="sxs-lookup"><span data-stu-id="5f56d-110">For example, the following VBScript example obtains a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects from the [**Devices**](-wia-iwia-devices.md) method and then uses a **For...Each** loop to iterate through the collection:</span></span>


```
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ' Do something with the DeviceInfo object.
Next
</SCRIPT>
```



> [!Note]  
> <span data-ttu-id="5f56d-111">Объекты коллекции WIA основаны на 0.</span><span class="sxs-lookup"><span data-stu-id="5f56d-111">WIA collection objects are 0-based.</span></span>

 

 

 



