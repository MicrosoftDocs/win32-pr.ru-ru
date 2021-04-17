---
description: Коллекция объектов DeviceInfo, представляющих все устройства, установленные на компьютере.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Свойство WIA. Devices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d03aa0b7e73d5dfbc6449816f3b64147e51db882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711253"
---
# <a name="wiadevices-property"></a>Свойство WIA. Devices

Коллекция объектов [**DeviceInfo**](-wia-deviceinfo.md) , представляющих все устройства, установленные на компьютере. Только для чтения.

> [!Note]  
> Эта коллекция основана на 0.

 

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a>Значение свойства

## <a name="examples"></a>Примеры

В следующем примере показано использование коллекции **устройств** для перечисления устройств в системе.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




