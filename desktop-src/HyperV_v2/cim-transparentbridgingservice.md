---
description: Представляет прозрачный аспект моста для \_ объекта СВИТЧСЕРВИЦЕ CIM.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: Класс CIM_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908731"
---
# <a name="cim_transparentbridgingservice-class"></a>\_Класс CIM транспарентбридгингсервице

Представляет прозрачный аспект моста для объекта [**\_ свитчсервице CIM**](cim-switchservice.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ транспарентбридгингсервице** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ транспарентбридгингсервице** имеет следующие свойства.

<dl> <dt>

**агингтиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Мост IETF — MIB. dot1dTpAgingTime ")
</dt> </dl>

Период времени ожидания (в секундах), в течение которого динамически изучена информация о пересылке. Стандарт 802.1 D-1990 рекомендует значение по умолчанию, равное 300 секундам.

</dd> <dt>

**FID**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Фильтрация идентификатора базы данных, используемого коммутаторами с поддержкой VLAN, которые имеют более одной фильтрации базы данных.

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

[**\_ФОРВАРДИНГСЕРВИЦЕ CIM**](cim-forwardingservice.md)
</dt> </dl>

 

