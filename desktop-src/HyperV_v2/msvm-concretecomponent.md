---
description: Универсальная ассоциация, используемая для установления части отношений между управляемыми элементами.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Класс Msvm_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663733"
---
# <a name="msvm_concretecomponent-class"></a>\_Класс мсвм конкретекомпонент

Универсальная ассоциация, используемая для установления отношений "часть" между управляемыми элементами. [**Модель CIM \_ Конкретекомпонент**](/previous-versions//cc150665(v=vs.85)) определяется как конкретный подкласс абстрактного класса [**\_ компонента CIM**](/windows/desktop/CIMWin32Prov/cim-component) , который используется вместо множества конкретных подклассов компонента, которые не добавляют семантику (то есть подклассы, которые не уточняют тип композиции, обновляют кратность или добавляют или удаляют квалификаторы).

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ конкретекомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ конкретекомпонент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Родительский элемент в ассоциации. Это свойство наследуется от [**CIM \_ конкретекомпонент**](/previous-versions//cc150665(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дочерний элемент в ассоциации. Это свойство наследуется от [**CIM \_ конкретекомпонент**](/previous-versions//cc150665(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ конкретекомпонент мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КОНКРЕТЕКОМПОНЕНТ CIM**](cim-concretecomponent.md)
</dt> <dt>

[**\_КОНКРЕТЕКОМПОНЕНТ CIM**](/previous-versions//cc150665(v=vs.85))
</dt> <dt>

[Классы виртуальных систем](virtual-system-classes.md)
</dt> </dl>

 

