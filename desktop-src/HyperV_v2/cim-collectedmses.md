---
description: Представляет универсальную связь между коллекцией управляемых системных элементов и элементами коллекции.
ms.assetid: c9e2bbca-67be-41f2-a94c-cf4eaf5f4694
title: Класс CIM_CollectedMSEs (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 74486e12eb4b4ee155554db8ba9f6f8774728217ca6d0ac70b5faac11958726a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790534"
---
# <a name="cim_collectedmses-class-hyper-v-management"></a>Класс CIM_CollectedMSEs (Управление Hyper-V)

Представляет универсальную связь между коллекцией управляемых системных элементов и элементами коллекции.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectedMSEs : CIM_MemberOfCollection
{
  CIM_CollectionOfMSEs     REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ коллектедмсес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ коллектедмсес** имеет следующие свойства.

<dl> <dt>

**Коллекция**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ коллектионофмсес**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Коллекция.

</dd> <dt>

**Член**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажедсистемелемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("член")
</dt> </dl>

Элементы коллекции.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_МЕМБЕРОФКОЛЛЕКТИОН CIM**](cim-memberofcollection.md)
</dt> </dl>

 

