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
ms.openlocfilehash: 55ed0dc2cfdaa3f351537e18994a0b45c8490097f93c2cfaddbdf575d07e03c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790304"
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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




