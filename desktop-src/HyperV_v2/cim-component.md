---
description: Представляет универсальную связь между родительским управляемым элементом и дочерним управляемым элементом, в котором дочерний элемент представляет компонент или часть родительского элемента.
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: Класс CIM_Component (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683619"
---
# <a name="cim_component-class-hyper-v-management"></a>Класс CIM_Component (Управление Hyper-V)

Представляет универсальную связь между родительским управляемым элементом и дочерним управляемым элементом, в котором дочерний элемент представляет компонент или часть родительского элемента.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **\_ компонента CIM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ компонента CIM** имеет эти свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Родительский элемент в ассоциации.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Дочерний элемент в ассоциации.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

