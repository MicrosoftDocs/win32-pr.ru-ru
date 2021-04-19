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
# <a name="using-wia-collection-objects"></a>Использование объектов коллекции WIA

Коллекция — это объект, содержащий один или несколько объектов. Коллекции обеспечивают эффективный способ группирования схожих объектов. Получение образа Windows (WIA) предоставляет коллекции для объектов [**DeviceInfo**](-wia-deviceinfo.md) и [**Item**](-wia-item.md) .

Коллекции используются для перечисления содержащихся в них объектов. Например, следующий пример на языке VBScript получает коллекцию объектов [**DeviceInfo**](-wia-deviceinfo.md) из метода [**Devices**](-wia-iwia-devices.md) , а затем использует **для... Каждый** цикл для итерации по коллекции:


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
> Объекты коллекции WIA основаны на 0.

 

 

 



