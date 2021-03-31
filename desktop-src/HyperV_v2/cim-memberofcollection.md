---
description: Представляет связь, в которой управляемый элемент является членом и обрабатывается коллекцией.
ms.assetid: 324284fa-ece6-41df-9891-040a7561dce4
title: Класс CIM_MemberOfCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemberOfCollection
- CIM_MemberOfCollection.Collection
- CIM_MemberOfCollection.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9bcebfb08cbbc0cb18e00f1b0e5e2646ca086faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081079"
---
# <a name="cim_memberofcollection-class"></a>\_Класс CIM мемберофколлектион

Представляет связь, в которой управляемый элемент является членом и обрабатывается коллекцией.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_MemberOfCollection
{
  CIM_Collection     REF Collection;
  CIM_ManagedElement REF Member;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ мемберофколлектион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ мемберофколлектион** имеет следующие свойства.

<dl> <dt>

**Коллекция**
</dt> <dd> <dl> <dt>

Тип данных: **\_ коллекция CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Коллекция, которая выполняет статистическую обработку элементов.

</dd> <dt>

**Член**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Элемент коллекции.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

