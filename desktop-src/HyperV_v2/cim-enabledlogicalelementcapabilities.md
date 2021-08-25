---
description: Описывает ограничения свойств связанного \_ объекта CIM енабледлогикалелемент.
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: Класс CIM_EnabledLogicalElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbec7b52d735b6dcff4da4c211da1db8b36d18adf20798fdcaa3932e1761119a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695914"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a>\_Класс CIM енабледлогикалелементкапабилитиес

Описывает ограничения свойств связанного объекта [**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ енабледлогикалелементкапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ енабледлогикалелементкапабилитиес** имеет следующие свойства.

<dl> <dt>

**елементнамидитсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-свапи. ИНЦИТС-T11 \| свапи \_ Unit \_ config \_ Cap \_ T \| едитнаме "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ манажеделемент**](cim-managedelement.md).**ElementName**")
</dt> </dl>

**значение true** , если свойство **ElementName** включенного логического элемента может быть изменено; в противном случае — **значение false**.

</dd> <dt>

**елементнамемаск**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ енабледлогикалелементкапабилитиес**.**Макселементнамелен**")
</dt> </dl>

Регулярное выражение, которое указывает на ограничения для свойства **ElementName** логического элемента Enable. Допустимый синтаксис см. в разделе *DMTF Standard ABNF с руководством по использованию спецификации профиля управления*. приложение в.

> [!Note]  
> Если это свойство и свойство **елементнамемаск** логического элемента включения содержат максимальную длину **ElementName**, используется меньшее значение.

 

</dd> <dt>

**макселементнамелен**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-свапи. ИНЦИТС-T11 \| свапи \_ Unit \_ config \_ Cap \_ T \| макснамечарс "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ фксвитчкапабилитиес. елементнамидитсуппортед ","**CIM \_ EnabledLogicalElementCapabilities**.**Елементнамемаск**")
</dt> </dl>

Максимальная поддерживаемая длина свойства **ElementName** для включенного логического элемента.

</dd> <dt>

**рекуестедстатессуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).**RequestStateChange**")
</dt> </dl>

Возможные состояния, которые могут запрашиваться для включенного логического элемента методом [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Завершение работы** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Вне сети** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Тест** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Отложить** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Замораживание** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Перезагрузка** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Сброс** (11)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Возможности CIM**](cim-capabilities.md)
</dt> </dl>

 

