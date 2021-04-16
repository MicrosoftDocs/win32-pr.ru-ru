---
description: Представляет связь между службой и управляемым элементом, на которые может повлиять выполнение.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: Класс CIM_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662471"
---
# <a name="cim_serviceaffectselement-class"></a>\_Класс CIM сервицеаффектселемент

Представляет связь между службой и управляемым элементом, на которые может повлиять выполнение.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Члены

Класс **CIM \_ сервицеаффектселемент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ сервицеаффектселемент** имеет следующие свойства.

<dl> <dt>

**аффектеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Управляемый элемент, затронутый службой.

</dd> <dt>

**аффектинжелемент**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Служба CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Служба, влияющая на управляемый элемент.

</dd> <dt>

**елементеффектс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сервицеаффектселемент**.**Осерелементеффектсдескриптионс**")
</dt> </dl>

Воздействие на управляемый элемент. Этот массив соответствует массиву **осерелементеффектсдескриптионс** .

\- Монопольное использование (2): ни одна другая служба не может использовать эту связь с элементом.

\- Влияние на производительность (3): не рекомендуется в пользу "потребляет", "повышает производительность" или "снижение производительности". Выполнение службы может повысить или снизить производительность элемента. Это может быть побочным действием выполнения или, как следствие, от методов, предоставляемых службой.

\- Целостность элементов (4): не рекомендуется в пользу "потребляет", "повышает целостность" или "снижение целостности". Выполнение службы может повысить или снизить целостность элемента. Это может быть побочным действием выполнения или, как следствие, от методов, предоставляемых службой.

\- Управляет (5). служба управляет элементом.

\- Потребление (6): выполнение службы потребляет некоторые или все связанные элементы как следствие выполнения службы. Например, служба может использовать циклы ЦП, что может повлиять на производительность или хранение, что может повлиять на производительность и целостность. (Например, отсутствие свободного хранилища может привести к снижению целостности, уменьшая возможность сохранения состояния. ) "Использование" может использоваться отдельно или в сочетании с другими значениями (в частности, "снижение производительности" и "снижение целостности").

Для отражения служб распределения, которые могут предоставляться службой, следует использовать "Управление", а не "использование".

\- Расширяет целостность (7): служба может улучшить целостность связанного элемента.

\- Деградация целостности (8): служба может снизить целостность связанного элемента.

\- Повышение производительности (9): служба может повысить производительность связанного элемента.

\- Снижение производительности (10): служба может снизить производительность связанного элемента.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

**Эксклюзивное использование** (2)


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

**Влияние на производительность** (3)


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

**Целостность элементов** (4)


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

**Управляет** (5)


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

**Потреблено** (6)


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

**Улучшенная целостность** (7)


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

**Целостность деградаций** (8)


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

**Повышает производительность** (9)


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

Снижение **производительности** (10)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (0x8000.. 0XFFFF


</dt> <dd></dd> </dl>

</dd> <dt>

**осерелементеффектсдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сервицеаффектселемент**.**Елементеффектс**")
</dt> </dl>

Каждый элемент в массиве предоставляет дополнительные сведения для соответствующего элемента в массиве **елементеффектс** . Для любого элемента в массиве **елементеффектс** , для которого задано значение **other** ("1"), требуется описание.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

