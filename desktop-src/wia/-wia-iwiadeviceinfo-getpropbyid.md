---
description: Метод Жетпропбид объекта DeviceInfo использует идентификатор свойства устройства для возвращения его значения.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: DeviceInfo. Жетпропбид, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719517"
---
# <a name="deviceinfogetpropbyid-method"></a>DeviceInfo. Жетпропбид, метод

Метод **жетпропбид** объекта [**DeviceInfo**](-wia-deviceinfo.md) использует идентификатор свойства устройства для возвращения его значения.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Идентификатор* \[ в\]
</dt> <dd>

Тип: **[виадевицеинфопропертид](-wia-wiadeviceinfopropertyid.md)**

Указывает идентификатор свойства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **Variant**

Этот метод возвращает значение свойства, заданного *идентификатором*.

## <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы найти значение свойства устройства по его ИДЕНТИФИКАТОРу. Список идентификаторов свойств см. в разделе [определения констант свойств WIA](-wia-wia-property-constant-definitions.md). Сведения о свойствах получения образа Windows (WIA) см. в разделе [константы свойства WIA](-wia-wia-property-constants.md).

Для приложений Microsoft Visual Basic добавьте ссылку на "Библиотека типов приобретения образа Windows 1,01". Следующие константы, определенные в этом файле, допустимы для этого метода:

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a>Примеры

В следующем примере демонстрируется использование метода **жетпропбид** для получения значения свойства.


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




