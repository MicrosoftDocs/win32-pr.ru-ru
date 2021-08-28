---
description: Представляет связь между заданием и управляемыми элементами, на которые может повлиять его выполнение.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Класс Msvm_AffectedStorageJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9eed09eab5a2bbb6985d1dc230d12a4f60fe5834b3fce1927036b560adc5d7e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693524"
---
# <a name="msvm_affectedstoragejobelement-class"></a>\_Класс мсвм аффектедсторажежобелемент

Представляет связь между заданием и управляемыми элементами, на которые может повлиять его выполнение.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ аффектедсторажежобелемент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ аффектедсторажежобелемент** имеет следующие свойства.

<dl> <dt>

**аффектеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Управляемый элемент, затронутый выполнением задания. Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**аффектинжелемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ сторажежоб**](msvm-storagejob.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ аффектеджобелемент. аффектинжелемент")
</dt> </dl>

Задание, влияющее на затронутый элемент. Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**елементеффектс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Перечисление, описывающее воздействие на управляемый элемент. Этот массив соответствует массиву свойств **осерелементеффектсдескриптионс** , где второй предоставляет подробные сведения, относящиеся к эффектам высокого уровня, перечисленным этим свойством. Дополнительные сведения требуются, если массив свойств **елементеффектс** содержит значение 1, (другое). Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Эксклюзивное использование** (2)
</dt> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Влияние на производительность** (3)
</dt> <dt>

<span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Целостность элементов** (4)
</dt> </dl>

</dd> <dt>

**осерелементеффектсдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет подробные сведения о результате действия на соответствующей позиции массива в массиве свойств **елементеффектс** . Эта информация необходима, когда соответствующий элемент в массиве свойств **елементеффектс** содержит значение 1 (другое). Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ аффектедсторажежобелемент мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[служба хранилища Класса](storage-classes.md)
</dt> </dl>

 

