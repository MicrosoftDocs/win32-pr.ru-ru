---
description: Управляет назначаемыми устройствами на компьютере узла.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Класс Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684633"
---
# <a name="msvm_assignabledeviceservice-class"></a>\_Класс мсвм ассигнабледевицесервице

Управляет назначаемыми устройствами на компьютере узла.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ ассигнабледевицесервице** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **мсвм \_ ассигнабледевицесервице** содержит следующие методы.



| Метод                                                                                    | Описание                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**дисмаунтассигнабледевице**](msvm-assignabledeviceservice-dismountassignabledevice.md) | Отключает указанное устройство PCI, чтобы его можно было назначить.<br/>                      |
| [**маунтассигнабледевице**](msvm-assignabledeviceservice-mountassignabledevice.md)       | Подключает указанное устройство PCI, чтобы его можно было использовать в системе главного компьютера.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




