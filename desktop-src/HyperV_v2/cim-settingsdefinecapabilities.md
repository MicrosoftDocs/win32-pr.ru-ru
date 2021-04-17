---
description: Представляет ассоциацию между свойствами \_ экземпляра CIM и \_ экземпляра возможностей CIM.
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: Класс CIM_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineCapabilities
- CIM_SettingsDefineCapabilities.GroupComponent
- CIM_SettingsDefineCapabilities.PartComponent
- CIM_SettingsDefineCapabilities.PropertyPolicy
- CIM_SettingsDefineCapabilities.ValueRole
- CIM_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3c36e7c24702578704e849820abf2b1769c91c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663857"
---
# <a name="cim_settingsdefinecapabilities-class"></a>\_Класс CIM сеттингсдефинекапабилитиес

Представляет ассоциацию между свойствами экземпляра [**CIM и \_**](cim-settingdata.md) экземпляра [**\_ возможностей CIM**](cim-capabilities.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Abstract, Version("2.22.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingsDefineCapabilities : CIM_Component
{
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ сеттингсдефинекапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ сеттингсдефинекапабилитиес** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **\_ возможности CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка на экземпляр [**\_ возможностей CIM**](cim-capabilities.md) .

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **\_ SettingData CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ссылка на экземпляр [**CIM \_ SettingData**](cim-settingdata.md) , используемый для определения экземпляра [**\_ возможностей CIM**](cim-capabilities.md) .

</dd> <dt>

**пропертиполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сеттингсдефинекапабилитиес**.**Валуероле**","**CIM \_ сеттингсдефинекапабилитиес**.**Валуеранже**")
</dt> </dl>

Указывает, обрабатываются ли непустые, ненулевые свойства связанного экземпляра [**CIM \_ -класса**](cim-settingdata.md) , независимо друг от друга или как коррелированный набор. Например, независимый набор максимальных свойств может быть определен при отсутствии связи между каждым свойством. Напротив, может потребоваться определить несколько коррелированных наборов максимальных свойств, если максимальное значение каждого из них зависит от некоторых других.

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**Независимое** (0)


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

**Коррелировано** (1)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**валуеранже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сеттингсдефинекапабилитиес**.**Пропертиполици**","**CIM \_ сеттингсдефинекапабилитиес**.**Валуероле**")
</dt> </dl>

Указывает тип диапазона значений, используемый свойствами ненулевых неключевых свойств экземпляра типа данных [**CIM \_**](cim-settingdata.md) .

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

**Точка** (0)


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

**Минимум** (1)


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

**Максимум** (2)


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

**Приращения** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**валуероле**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сеттингсдефинекапабилитиес**.**Пропертиполици**","**CIM \_ сеттингсдефинекапабилитиес**.**Валуеранже**")
</dt> </dl>

Дополнительная семантика для интерпретации ненулевых неключевых свойств экземпляра типа данных [**CIM \_**](cim-settingdata.md) .

"Default" указывает, что значения свойств экземпляра SettingData компонента будут использоваться в качестве значений по умолчанию при создании нового экземпляра SettingData для элементов, возможности которых определяются связанным экземпляром возможностей.

В экземплярах SettingData для определенных свойств, имеющих одинаковое семантическое назначение, в качестве значения по умолчанию должно быть указано не более одного экземпляра SettingData.

"Оптимальный" указывает, что экземпляр SettingData представляет оптимальные значения параметров для элементов, связанных с экземпляром связанных возможностей. Экземпляры SettingData нескольких компонентов могут быть объявлены как оптимальные. " Среднее значение указывает, что числовые свойства, отличные от NULL, неключевые, не являющиеся перечислениями, не являющиеся логическими, а не перечислимые, не являющиеся значениями типа Boolean, представляют собой среднюю точку для некоторого измерения. Для различных сочетаний свойств SettingData экземпляры SettingData с несколькими компонентами могут быть объявлены как "среднее". "Supported" указывает, что ненулевые неключевые свойства экземпляра SettingData компонента представляют набор поддерживаемых значений свойств, которые в противном случае не являются полными.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**По умолчанию** (0)


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

**Оптимальный** (1)


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

**Среднее значение** (2)


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

**Поддерживается** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Компонент CIM**](cim-component.md)
</dt> </dl>

 

