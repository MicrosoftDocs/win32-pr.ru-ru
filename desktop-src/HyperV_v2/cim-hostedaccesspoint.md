---
description: Представляет связь между точкой доступа службы (SAP) и системой, в которой она размещается.
ms.assetid: 82db71d6-6d14-408e-87e0-fe869e454d4d
title: Класс CIM_HostedAccessPoint (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Antecedent
- CIM_HostedAccessPoint.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2079d34af64b7819f7c7dc4991a00a9a01b350ee45c54b910a35f1008d45e510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014632"
---
# <a name="cim_hostedaccesspoint-class-hyper-v-management"></a>Класс CIM_HostedAccessPoint (Управление Hyper-V)

Представляет связь между точкой доступа службы (SAP) и системой, в которой она размещается. В системе может размещаться несколько точек доступа. Если реализация SAP моделируется, она должна быть реализована устройством или программным обеспечением, которое является частью системы, в которой размещается SAP.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_HostedAccessPoint : CIM_HostedDependency
{
  CIM_System             REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ хостедакцесспоинт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ хостедакцесспоинт** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **\_ система CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Система размещения.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сервицеакцесспоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимый), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

SAPs, размещенные в системе.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ХОСТЕДДЕПЕНДЕНЦИ CIM**](cim-hosteddependency.md)
</dt> </dl>

 

