---
description: Представляет связь между точкой доступа к службе (SAP) и логическим устройством, которое ее реализует.
ms.assetid: 40c8111a-d439-4c0f-805e-9c10d7182eb4
title: Класс CIM_DeviceSAPImplementation (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Antecedent
- CIM_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d801f0ce1ecc6b30ff9ae5481047cbacf9fa3e20f2713a4cf39b723c5fa904ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812821"
---
# <a name="cim_devicesapimplementation-class-hyper-v-management"></a>Класс CIM_DeviceSAPImplementation (Управление Hyper-V)

Представляет связь между точкой доступа к службе (SAP) и логическим устройством, которое ее реализует.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ девицесапимплементатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ девицесапимплементатион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Логическое устройство.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сервицеакцесспоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Протокол SAP, реализованный логическим устройством.

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

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

