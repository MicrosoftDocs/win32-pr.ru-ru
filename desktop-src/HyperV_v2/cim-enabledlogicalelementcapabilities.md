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
ms.openlocfilehash: 35f400643e01821667c999342603fd402a3ae419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663476"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a><span data-ttu-id="9e659-103">\_Класс CIM енабледлогикалелементкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="9e659-103">CIM\_EnabledLogicalElementCapabilities class</span></span>

<span data-ttu-id="9e659-104">Описывает ограничения свойств связанного объекта [**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md) .</span><span class="sxs-lookup"><span data-stu-id="9e659-104">Describes the restrictions on the properties of an associated [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e659-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e659-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="9e659-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9e659-106">Members</span></span>

<span data-ttu-id="9e659-107">Класс **CIM \_ енабледлогикалелементкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9e659-107">The **CIM\_EnabledLogicalElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="9e659-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="9e659-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e659-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="9e659-109">Properties</span></span>

<span data-ttu-id="9e659-110">Класс **CIM \_ енабледлогикалелементкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9e659-110">The **CIM\_EnabledLogicalElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e659-111">**елементнамидитсуппортед**</span><span class="sxs-lookup"><span data-stu-id="9e659-111">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e659-112">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9e659-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e659-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9e659-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e659-114">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-свапи. ИНЦИТС-T11 \| свапи \_ Unit \_ config \_ Cap \_ T \| едитнаме "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ манажеделемент**](cim-managedelement.md).**ElementName**")</span><span class="sxs-lookup"><span data-stu-id="9e659-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|EditName"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedElement**](cim-managedelement.md).**ElementName**")</span></span>
</dt> </dl>

<span data-ttu-id="9e659-115">**значение true** , если свойство **ElementName** включенного логического элемента может быть изменено; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9e659-115">**true** if the **ElementName** property of the enabled logical element can be modified; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="9e659-116">**елементнамемаск**</span><span class="sxs-lookup"><span data-stu-id="9e659-116">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e659-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e659-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e659-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9e659-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e659-119">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ енабледлогикалелементкапабилитиес**.**Макселементнамелен**")</span><span class="sxs-lookup"><span data-stu-id="9e659-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span></span>
</dt> </dl>

<span data-ttu-id="9e659-120">Регулярное выражение, которое указывает на ограничения для свойства **ElementName** логического элемента Enable.</span><span class="sxs-lookup"><span data-stu-id="9e659-120">A regular expression that indicates the restrictions on the **ElementName** property of the enable logical element.</span></span> <span data-ttu-id="9e659-121">Допустимый синтаксис см. в разделе *DMTF Standard ABNF с руководством по использованию спецификации профиля управления*. приложение в.</span><span class="sxs-lookup"><span data-stu-id="9e659-121">See *DMTF standard ABNF with the Management Profile Specification Usage Guide*, appendix C for the permitted syntax.</span></span>

> [!Note]  
> <span data-ttu-id="9e659-122">Если это свойство и свойство **елементнамемаск** логического элемента включения содержат максимальную длину **ElementName**, используется меньшее значение.</span><span class="sxs-lookup"><span data-stu-id="9e659-122">If this property and the **ElementNameMask** property of the enable logical element describe the maximum length of **ElementName**, the smaller value is used.</span></span>

 

</dd> <dt>

<span data-ttu-id="9e659-123">**макселементнамелен**</span><span class="sxs-lookup"><span data-stu-id="9e659-123">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e659-124">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e659-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e659-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9e659-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e659-126">Квалификаторы: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-свапи. ИНЦИТС-T11 \| свапи \_ Unit \_ config \_ Cap \_ T \| макснамечарс "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ фксвитчкапабилитиес. елементнамидитсуппортед ","**CIM \_ EnabledLogicalElementCapabilities**.**Елементнамемаск**")</span><span class="sxs-lookup"><span data-stu-id="9e659-126">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|MaxNameChars"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_FCSwitchCapabilities.ElementNameEditSupported", "**CIM\_EnabledLogicalElementCapabilities**.**ElementNameMask**")</span></span>
</dt> </dl>

<span data-ttu-id="9e659-127">Максимальная поддерживаемая длина свойства **ElementName** для включенного логического элемента.</span><span class="sxs-lookup"><span data-stu-id="9e659-127">The maximum supported length of the **ElementName** property of the enabled logical element.</span></span>

</dd> <dt>

<span data-ttu-id="9e659-128">**рекуестедстатессуппортед**</span><span class="sxs-lookup"><span data-stu-id="9e659-128">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e659-129">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9e659-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9e659-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9e659-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e659-131">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).**RequestStateChange**")</span><span class="sxs-lookup"><span data-stu-id="9e659-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")</span></span>
</dt> </dl>

<span data-ttu-id="9e659-132">Возможные состояния, которые могут запрашиваться для включенного логического элемента методом [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="9e659-132">The possible states that can be requested on the enabled logical element by the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9e659-133">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="9e659-133">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9e659-134">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="9e659-134">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="9e659-135">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="9e659-135">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="9e659-136">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="9e659-136">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="9e659-137">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="9e659-137">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="9e659-138">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="9e659-138">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="9e659-139">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="9e659-139">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="9e659-140">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="9e659-140">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="9e659-141">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="9e659-141">**Reset** (11)</span></span>


<span data-ttu-id="9e659-142"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9e659-142"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9e659-143">Требования</span><span class="sxs-lookup"><span data-stu-id="9e659-143">Requirements</span></span>



| <span data-ttu-id="9e659-144">Требование</span><span class="sxs-lookup"><span data-stu-id="9e659-144">Requirement</span></span> | <span data-ttu-id="9e659-145">Значение</span><span class="sxs-lookup"><span data-stu-id="9e659-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e659-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e659-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9e659-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9e659-147">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9e659-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e659-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9e659-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e659-149">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9e659-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9e659-150">Namespace</span></span><br/>                | <span data-ttu-id="9e659-151">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9e659-151">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9e659-152">MOF</span><span class="sxs-lookup"><span data-stu-id="9e659-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e659-153"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e659-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e659-154">DLL</span><span class="sxs-lookup"><span data-stu-id="9e659-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e659-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9e659-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9e659-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e659-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e659-157">**\_Возможности CIM**</span><span class="sxs-lookup"><span data-stu-id="9e659-157">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

