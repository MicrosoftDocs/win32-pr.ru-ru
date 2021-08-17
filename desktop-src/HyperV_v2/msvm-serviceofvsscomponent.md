---
description: Ассоциация между экземпляром Мсвм \_ всскомпонент и экземпляром мсвм \_ всссервице, который представляет службу для выполнения операций с компонентом VSS.
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Класс Msvm_ServiceOfVssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a96c59a2e483080293ece2281ddb64fc9a7b43b425e5b508fe7ec209d1144dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950544"
---
# <a name="msvm_serviceofvsscomponent-class"></a>\_Класс мсвм сервицеофвсскомпонент

Ассоциация между экземпляром [**мсвм \_ всскомпонент**](msvm-vsscomponent.md) и экземпляром [**мсвм \_ всссервице**](msvm-vssservice.md) , который представляет службу для выполнения операций с компонентом VSS.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ сервицеофвсскомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ сервицеофвсскомпонент** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ всскомпонент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")
</dt> </dl>

A, [**мсвм \_ всскомпонент**](msvm-vsscomponent.md) , представляющий компонент VSS.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ всссервице**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ зависимость CIM. Dependent")
</dt> </dl>

[**Мсвм \_ всссервице**](msvm-vssservice.md) , представляющий службу VSS IC.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

