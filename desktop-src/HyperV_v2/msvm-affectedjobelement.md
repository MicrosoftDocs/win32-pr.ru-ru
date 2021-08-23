---
description: Представляет связь между заданием и управляемым элементом, на который может повлиять его выполнение.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Класс Msvm_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f39d800516f96cf602257abc3bd8ed9ed5a8d5561f4b4a5e60f5eb140fc1c308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693544"
---
# <a name="msvm_affectedjobelement-class"></a>\_Класс мсвм аффектеджобелемент

Представляет связь между заданием и управляемым элементом, на который может повлиять его выполнение.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ аффектеджобелемент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ аффектеджобелемент** имеет следующие свойства.

<dl> <dt>

**аффектеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Управляемый элемент, затронутый выполнением задания. Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**аффектинжелемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ конкретежоб**](msvm-concretejob.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Задание, влияющее на управляемый элемент. Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**елементеффектс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Перечисление, описывающее воздействие на управляемый элемент. Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**осерелементеффектсдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет подробные сведения о результате действия в соответствующей позиции массива в **елементеффектс**. Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ аффектеджобелемент мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_АФФЕКТЕДЖОБЕЛЕМЕНТ CIM**](cim-affectedjobelement.md)
</dt> <dt>

[**\_АФФЕКТЕДЖОБЕЛЕМЕНТ CIM**](/previous-versions//cc150663(v=vs.85))
</dt> <dt>

[Классы управления виртуальной системой](virtual-system-management-classes.md)
</dt> </dl>

 

