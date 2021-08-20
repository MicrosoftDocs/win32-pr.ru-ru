---
description: Представляет ассоциацию, когда \_ объект CIM сервицеакцесспоинт запрашивает службы протокола из \_ объекта протоколендпоинт CIM.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: Класс CIM_BindsTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b0b2dc2f767ad409cece300fc33ecde0e6a0d2f55ce659ea9d77fe332f3529a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813425"
---
# <a name="cim_bindsto-class"></a>\_Класс CIM биндсто

Представляет ассоциацию, когда объект [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md) запрашивает службы протокола из [**объекта \_ протоколендпоинт CIM**](cim-protocolendpoint.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ биндсто** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ биндсто** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ протоколендпоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Конечная точка нижнего уровня, к которой обращается точка доступа службы.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сервицеакцесспоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Точка доступа или конечная точка протокола, зависящая от конечной точки нижнего уровня.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_САПСАПДЕПЕНДЕНЦИ CIM**](cim-sapsapdependency.md)
</dt> </dl>

 

