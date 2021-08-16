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
ms.openlocfilehash: b6cf843d92b5ce2260578b653a1163526b22fb735c01542d772b2687ca890dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208927"
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
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




