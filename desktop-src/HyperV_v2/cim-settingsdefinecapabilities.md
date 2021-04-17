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
# <a name="cim_settingsdefinecapabilities-class"></a><span data-ttu-id="e3815-103">\_Класс CIM сеттингсдефинекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="e3815-103">CIM\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="e3815-104">Представляет ассоциацию между свойствами экземпляра [**CIM и \_**](cim-settingdata.md) экземпляра [**\_ возможностей CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="e3815-104">Represents an association between properties of a [**CIM\_SettingData**](cim-settingdata.md) instance and a [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3815-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3815-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="e3815-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e3815-106">Members</span></span>

<span data-ttu-id="e3815-107">Класс **CIM \_ сеттингсдефинекапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e3815-107">The **CIM\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="e3815-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="e3815-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3815-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e3815-109">Properties</span></span>

<span data-ttu-id="e3815-110">Класс **CIM \_ сеттингсдефинекапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e3815-110">The **CIM\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3815-111">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="e3815-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3815-112">Тип данных: **\_ возможности CIM**</span><span class="sxs-lookup"><span data-stu-id="e3815-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="e3815-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3815-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3815-114">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e3815-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e3815-115">Ссылка на экземпляр [**\_ возможностей CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="e3815-115">A reference to the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="e3815-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e3815-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3815-117">Тип данных: **\_ SettingData CIM**</span><span class="sxs-lookup"><span data-stu-id="e3815-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e3815-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3815-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3815-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e3815-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e3815-120">Ссылка на экземпляр [**CIM \_ SettingData**](cim-settingdata.md) , используемый для определения экземпляра [**\_ возможностей CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="e3815-120">A reference to the [**CIM\_SettingData**](cim-settingdata.md) instance used to define the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="e3815-121">**пропертиполици**</span><span class="sxs-lookup"><span data-stu-id="e3815-121">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3815-122">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3815-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3815-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3815-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3815-124">Квалификаторы: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сеттингсдефинекапабилитиес**.**Валуероле**","**CIM \_ сеттингсдефинекапабилитиес**.**Валуеранже**")</span><span class="sxs-lookup"><span data-stu-id="e3815-124">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**ValueRole**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="e3815-125">Указывает, обрабатываются ли непустые, ненулевые свойства связанного экземпляра [**CIM \_ -класса**](cim-settingdata.md) , независимо друг от друга или как коррелированный набор.</span><span class="sxs-lookup"><span data-stu-id="e3815-125">Indicates whether the non-null, non-key properties of the associated [**CIM\_SettingData**](cim-settingdata.md) instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="e3815-126">Например, независимый набор максимальных свойств может быть определен при отсутствии связи между каждым свойством.</span><span class="sxs-lookup"><span data-stu-id="e3815-126">For instance, an independent set of maximum properties might be defined when there is no relationship between each property.</span></span> <span data-ttu-id="e3815-127">Напротив, может потребоваться определить несколько коррелированных наборов максимальных свойств, если максимальное значение каждого из них зависит от некоторых других.</span><span class="sxs-lookup"><span data-stu-id="e3815-127">In contrast, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="e3815-128">**Независимое** (0)</span><span class="sxs-lookup"><span data-stu-id="e3815-128">**Independent** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

<span data-ttu-id="e3815-129">**Коррелировано** (1)</span><span class="sxs-lookup"><span data-stu-id="e3815-129">**Correlated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e3815-130">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e3815-130">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3815-131">**валуеранже**</span><span class="sxs-lookup"><span data-stu-id="e3815-131">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3815-132">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3815-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3815-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3815-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3815-134">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сеттингсдефинекапабилитиес**.**Пропертиполици**","**CIM \_ сеттингсдефинекапабилитиес**.**Валуероле**")</span><span class="sxs-lookup"><span data-stu-id="e3815-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRole**")</span></span>
</dt> </dl>

<span data-ttu-id="e3815-135">Указывает тип диапазона значений, используемый свойствами ненулевых неключевых свойств экземпляра типа данных [**CIM \_**](cim-settingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="e3815-135">Indicates the type of value range used by properties of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="e3815-136">**Точка** (0)</span><span class="sxs-lookup"><span data-stu-id="e3815-136">**Point** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

<span data-ttu-id="e3815-137">**Минимум** (1)</span><span class="sxs-lookup"><span data-stu-id="e3815-137">**Minimums** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

<span data-ttu-id="e3815-138">**Максимум** (2)</span><span class="sxs-lookup"><span data-stu-id="e3815-138">**Maximums** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

<span data-ttu-id="e3815-139">**Приращения** (3)</span><span class="sxs-lookup"><span data-stu-id="e3815-139">**Increments** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e3815-140">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e3815-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3815-141">**валуероле**</span><span class="sxs-lookup"><span data-stu-id="e3815-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3815-142">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3815-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3815-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3815-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3815-144">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сеттингсдефинекапабилитиес**.**Пропертиполици**","**CIM \_ сеттингсдефинекапабилитиес**.**Валуеранже**")</span><span class="sxs-lookup"><span data-stu-id="e3815-144">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="e3815-145">Дополнительная семантика для интерпретации ненулевых неключевых свойств экземпляра типа данных [**CIM \_**](cim-settingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="e3815-145">The additional semantics for the interpretation of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<span data-ttu-id="e3815-146">"Default" указывает, что значения свойств экземпляра SettingData компонента будут использоваться в качестве значений по умолчанию при создании нового экземпляра SettingData для элементов, возможности которых определяются связанным экземпляром возможностей.</span><span class="sxs-lookup"><span data-stu-id="e3815-146">"Default" indicates that property values of the component SettingData instance will be used as default values, when a new SettingData instance is created for elements whose capabilities are defined by the associated Capabilities instance.</span></span>

<span data-ttu-id="e3815-147">В экземплярах SettingData для определенных свойств, имеющих одинаковое семантическое назначение, в качестве значения по умолчанию должно быть указано не более одного экземпляра SettingData.</span><span class="sxs-lookup"><span data-stu-id="e3815-147">Across instances of settingdata, for particular properties having the same semantic purpose, at most one such settingdata instance shall be specified as a default.</span></span>

<span data-ttu-id="e3815-148">"Оптимальный" указывает, что экземпляр SettingData представляет оптимальные значения параметров для элементов, связанных с экземпляром связанных возможностей.</span><span class="sxs-lookup"><span data-stu-id="e3815-148">"Optimal" indicates that the SettingData instance represents optimal setting values for elements associated with the associated capabilities instance.</span></span> <span data-ttu-id="e3815-149">Экземпляры SettingData нескольких компонентов могут быть объявлены как оптимальные. " Среднее значение указывает, что числовые свойства, отличные от NULL, неключевые, не являющиеся перечислениями, не являющиеся логическими, а не перечислимые, не являющиеся значениями типа Boolean, представляют собой среднюю точку для некоторого измерения.</span><span class="sxs-lookup"><span data-stu-id="e3815-149">Multiple component SettingData instances may be declared as optimal."Mean" indicates that the non-null, non-key, non-enumerated, non-boolean, numeric properties of the associated SettingData instance represents an average point along some dimension.</span></span> <span data-ttu-id="e3815-150">Для различных сочетаний свойств SettingData экземпляры SettingData с несколькими компонентами могут быть объявлены как "среднее".</span><span class="sxs-lookup"><span data-stu-id="e3815-150">For different combinations of SettingData properties, multiple component SettingData instances may be declared as "Mean".</span></span> <span data-ttu-id="e3815-151">"Supported" указывает, что ненулевые неключевые свойства экземпляра SettingData компонента представляют набор поддерживаемых значений свойств, которые в противном случае не являются полными.</span><span class="sxs-lookup"><span data-stu-id="e3815-151">"Supported" indicates that the non-null, non-key properties of the Component SettingData instance represents a set of supported property values that are not otherwise qualified.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="e3815-152">**По умолчанию** (0)</span><span class="sxs-lookup"><span data-stu-id="e3815-152">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

<span data-ttu-id="e3815-153">**Оптимальный** (1)</span><span class="sxs-lookup"><span data-stu-id="e3815-153">**Optimal** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

<span data-ttu-id="e3815-154">**Среднее значение** (2)</span><span class="sxs-lookup"><span data-stu-id="e3815-154">**Mean** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="e3815-155">**Поддерживается** (3)</span><span class="sxs-lookup"><span data-stu-id="e3815-155">**Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e3815-156">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e3815-156">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="e3815-157"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e3815-157"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e3815-158">Требования</span><span class="sxs-lookup"><span data-stu-id="e3815-158">Requirements</span></span>



| <span data-ttu-id="e3815-159">Требование</span><span class="sxs-lookup"><span data-stu-id="e3815-159">Requirement</span></span> | <span data-ttu-id="e3815-160">Значение</span><span class="sxs-lookup"><span data-stu-id="e3815-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3815-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3815-161">Minimum supported client</span></span><br/> | <span data-ttu-id="e3815-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e3815-162">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e3815-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3815-163">Minimum supported server</span></span><br/> | <span data-ttu-id="e3815-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3815-164">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e3815-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3815-165">Namespace</span></span><br/>                | <span data-ttu-id="e3815-166">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e3815-166">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e3815-167">MOF</span><span class="sxs-lookup"><span data-stu-id="e3815-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3815-168"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3815-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3815-169">DLL</span><span class="sxs-lookup"><span data-stu-id="e3815-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3815-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e3815-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e3815-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3815-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3815-172">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="e3815-172">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

