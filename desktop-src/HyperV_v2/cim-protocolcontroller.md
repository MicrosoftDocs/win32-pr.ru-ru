---
description: Представляет группу контроллеров, управляющих работой и функцией устройств, инициирующих протоколы.
ms.assetid: fb6b65d4-3a1a-47b1-afc7-9b10e8eeaa32
title: Класс CIM_ProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolController
- CIM_ProtocolController.MaxUnitsControlled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7dcd0f0ca1891914e2c4fc3fedbc0012d930dbaec99926f9db8e013435367f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148516"
---
# <a name="cim_protocolcontroller-class"></a>\_Класс CIM протоколконтроллер

Представляет группу контроллеров, управляющих работой и функцией устройств, инициирующих протоколы.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolController : CIM_LogicalDevice
{
  uint32 MaxUnitsControlled;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ протоколконтроллер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ протоколконтроллер** имеет следующие свойства.

<dl> <dt>

**максунитсконтроллед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное число единиц, которое может управляться или доступно через контроллер протокола.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Модель \_ CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




