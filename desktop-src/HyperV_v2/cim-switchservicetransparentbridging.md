---
description: Представляет ассоциацию, в которой служба моста является компонентом службы коммутатора.
ms.assetid: 737d5ba1-0759-40cf-bc46-a059d19902c8
title: Класс CIM_SwitchServiceTransparentBridging
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchServiceTransparentBridging
- CIM_SwitchServiceTransparentBridging.GroupComponent
- CIM_SwitchServiceTransparentBridging.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e3f56f565286358f5d55ee47ccb102a4ecbf35e89fcd207c67518fc1fb42627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899484"
---
# <a name="cim_switchservicetransparentbridging-class"></a>\_Класс CIM свитчсервицетранспарентбридгинг

Представляет ассоциацию, в которой служба моста является компонентом службы коммутатора.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchServiceTransparentBridging : CIM_ServiceComponent
{
  CIM_SwitchService              REF GroupComponent;
  CIM_TransparentBridgingService REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ свитчсервицетранспарентбридгинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ свитчсервицетранспарентбридгинг** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ свитчсервице**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка [**CIM \_ свитчсервице**](cim-switchservice.md) на службу коммутатора.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ транспарентбридгингсервице**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ссылка [**CIM \_ транспарентбридгингсервице**](cim-transparentbridgingservice.md) на службу моста компонентов.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_SERVICECOMPONENT CIM**](cim-servicecomponent.md)
</dt> </dl>

 

