---
description: Представляет ассоциацию, в которой конечные точки протокола зависят от службы пересылки для пересылки данных.
ms.assetid: b63dbd2c-2842-498a-a352-b7ab7f7c841a
title: Класс CIM_ForwardsAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardsAmong
- CIM_ForwardsAmong.Antecedent
- CIM_ForwardsAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: aa6f3782407f57f999117b83918460adae307c962336386301592d3408e6490d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014652"
---
# <a name="cim_forwardsamong-class"></a>\_Класс CIM форвардсамонг

Представляет ассоциацию, в которой конечные точки протокола зависят от службы пересылки для пересылки данных.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::RoutingForwarding")]
class CIM_ForwardsAmong : CIM_ServiceSAPDependency
{
  CIM_ProtocolEndpoint  REF Antecedent;
  CIM_ForwardingService REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ форвардсамонг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ форвардсамонг** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ протоколендпоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Конечные точки протокола отправляют и получают перенаправленные данные.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ форвардингсервице**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Служба пересылки, которая перенаправляет данные.

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

[**\_СЕРВИЦЕСАПДЕПЕНДЕНЦИ CIM**](cim-servicesapdependency.md)
</dt> </dl>

 

