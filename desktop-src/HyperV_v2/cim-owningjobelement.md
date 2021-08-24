---
description: Представляет связь между заданием и управляемым элементом, создавшим задание.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: Класс CIM_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8ea0e4371246f71d125295730c19de75c59eafb08a4c081699b6b40575f27a99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694664"
---
# <a name="cim_owningjobelement-class"></a>\_Класс CIM овнингжобелемент

Представляет связь между заданием и управляемым элементом, создавшим задание. Так как задание может перемещаться между системами, а управляемый элемент может не существовать в течение всего задания, в некоторых случаях такая ассоциация может быть невозможной или может существовать только для части существования задания.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ овнингжобелемент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ овнингжобелемент** имеет следующие свойства.

<dl> <dt>

**овнеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Задание CIM** .
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ссылка на задание, созданное управляемым элементом.

</dd> <dt>

**овнинжелемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка на управляемый элемент, создавший задание.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

