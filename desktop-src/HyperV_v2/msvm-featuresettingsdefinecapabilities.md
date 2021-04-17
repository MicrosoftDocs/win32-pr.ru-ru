---
description: Предоставляет ссылку между экземпляром возможностей коммутатора Ethernet и минимальными, максимальными, добавочными и параметрами по умолчанию для ресурса.
ms.assetid: 5abd8b2a-9f72-4875-be5c-ce5a2f526e9a
title: Класс Msvm_FeatureSettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingsDefineCapabilities
- Msvm_FeatureSettingsDefineCapabilities.GroupComponent
- Msvm_FeatureSettingsDefineCapabilities.PartComponent
- Msvm_FeatureSettingsDefineCapabilities.PropertyPolicy
- Msvm_FeatureSettingsDefineCapabilities.ValueRole
- Msvm_FeatureSettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ec91a73931458cb6f7e07a7cfc23e71e4665fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662523"
---
# <a name="msvm_featuresettingsdefinecapabilities-class"></a><span data-ttu-id="6dba7-103">\_Класс мсвм феатуресеттингсдефинекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="6dba7-103">Msvm\_FeatureSettingsDefineCapabilities class</span></span>

<span data-ttu-id="6dba7-104">Предоставляет ссылку между экземпляром возможностей коммутатора Ethernet и минимальными, максимальными, добавочными и параметрами по умолчанию для ресурса.</span><span class="sxs-lookup"><span data-stu-id="6dba7-104">Provides a link between the Ethernet switch feature capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="6dba7-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6dba7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dba7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6dba7-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  Msvm_EthernetSwitchFeatureCapabilities REF GroupComponent;
  Msvm_FeatureSettingData                REF PartComponent;
  uint16                                     PropertyPolicy = 0;
  uint16                                     ValueRole = 3;
  uint16                                     ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="6dba7-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6dba7-107">Members</span></span>

<span data-ttu-id="6dba7-108">Класс **мсвм \_ феатуресеттингсдефинекапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6dba7-108">The **Msvm\_FeatureSettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="6dba7-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6dba7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6dba7-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6dba7-110">Properties</span></span>

<span data-ttu-id="6dba7-111">Класс **мсвм \_ феатуресеттингсдефинекапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6dba7-111">The **Msvm\_FeatureSettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6dba7-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="6dba7-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dba7-113">Тип данных: **[ **мсвм \_ есернетсвитчфеатурекапабилитиес**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="6dba7-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6dba7-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6dba7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dba7-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="6dba7-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6dba7-116">Ссылка на экземпляр класса [**мсвм \_ есернетсвитчфеатурекапабилитиес**](msvm-ethernetswitchfeaturecapabilities.md) , представляющий возможности функции коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="6dba7-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the Ethernet switch feature capabilities.</span></span> <span data-ttu-id="6dba7-117">Это свойство наследуется [**от \_ компонента CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="6dba7-117">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="6dba7-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6dba7-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dba7-119">Тип данных: **[ **мсвм \_ феатуресеттингдата**](msvm-featuresettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="6dba7-119">Data type: **[**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6dba7-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6dba7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dba7-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="6dba7-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6dba7-122">Ссылка на экземпляр класса [**мсвм \_ феатуресеттингдата**](msvm-featuresettingdata.md) , представляющий параметры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6dba7-122">A reference to an instance of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represents the resource settings.</span></span> <span data-ttu-id="6dba7-123">Это свойство наследуется [**от \_ компонента CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="6dba7-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="6dba7-124">**пропертиполици**</span><span class="sxs-lookup"><span data-stu-id="6dba7-124">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dba7-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6dba7-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6dba7-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6dba7-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6dba7-127">Указывает, обрабатываются ли **ненулевые** неключевые свойства **PartComponent** независимо или как коррелированный набор.</span><span class="sxs-lookup"><span data-stu-id="6dba7-127">Specifies whether the non-**Null**, non-key properties of the **PartComponent** are treated independently or as a correlated set.</span></span> <span data-ttu-id="6dba7-128">Например, может быть определен независимый набор максимальных свойств, но связь между ними отсутствует.</span><span class="sxs-lookup"><span data-stu-id="6dba7-128">For example, an independent set of maximum properties might be defined, yet there is no relationship between each property.</span></span> <span data-ttu-id="6dba7-129">С другой стороны, может потребоваться определить несколько коррелированных наборов максимальных свойств, если максимальное значение каждого из них зависит от некоторых других.</span><span class="sxs-lookup"><span data-stu-id="6dba7-129">On the other hand, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<span data-ttu-id="6dba7-130">Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6dba7-130">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="6dba7-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Независимое** (0)</span><span class="sxs-lookup"><span data-stu-id="6dba7-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independent** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6dba7-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Коррелировано** (1)</span><span class="sxs-lookup"><span data-stu-id="6dba7-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlated** (1)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6dba7-133">**валуеранже**</span><span class="sxs-lookup"><span data-stu-id="6dba7-133">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dba7-134">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6dba7-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6dba7-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6dba7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dba7-136">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="6dba7-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6dba7-137">Указывает более семантическую семантику для интерпретации всех **ненулевых** неключевых свойств данных параметров.</span><span class="sxs-lookup"><span data-stu-id="6dba7-137">Indicates further semantics on the interpretation of all non-**Null**, non-key properties of the setting data.</span></span>

<span data-ttu-id="6dba7-138">Приведенные ниже значения оцениваются только для **ненулевых**, неключевых, неперечислимых, нелогических числовых свойств данных параметров.</span><span class="sxs-lookup"><span data-stu-id="6dba7-138">The values below are only evaluated against non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the setting data.</span></span> <span data-ttu-id="6dba7-139">Каждое свойство этого набора должно быть математически сравнимым с другими экземплярами этого свойства.</span><span class="sxs-lookup"><span data-stu-id="6dba7-139">Each property of that set must be mathematically comparable to other instances of that property.</span></span>

<span data-ttu-id="6dba7-140">Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6dba7-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="6dba7-141">Значение</span><span class="sxs-lookup"><span data-stu-id="6dba7-141">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="6dba7-142">Значение</span><span class="sxs-lookup"><span data-stu-id="6dba7-142">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="6dba7-143"><dt>**Точка**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6dba7-143"><dt>**Point**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="6dba7-144">В этом экземпляре данных параметра предоставляется один набор значений.</span><span class="sxs-lookup"><span data-stu-id="6dba7-144">This setting data instance provides a single set of values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <span data-ttu-id="6dba7-145"><dt>**Минимум**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6dba7-145"><dt>**Minimums**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="6dba7-146">Данные этого параметра предоставляют минимальные значения для вычисляемых свойств.</span><span class="sxs-lookup"><span data-stu-id="6dba7-146">This setting data provides minimum values for evaluated properties.</span></span> <span data-ttu-id="6dba7-147">При использовании с **пропертиполици** = "независимым" для каждого из возможностей необходимо указать только один такой параметр для каждого конкретного экземпляра данных параметра.</span><span class="sxs-lookup"><span data-stu-id="6dba7-147">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="6dba7-148">Если ограничение не ограничено максимальным значением для одного и того же набора свойств, то все значения, сравниваемые выше указанных значений, также считаются поддерживаемыми экземпляром связанных возможностей.</span><span class="sxs-lookup"><span data-stu-id="6dba7-148">Unless restricted by a Maximums value on the same set of properties, all values that compare higher than the specified values are also considered to be supported by the associated capabilities instance.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <span data-ttu-id="6dba7-149"><dt>**Максимум**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6dba7-149"><dt>**Maximums**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="6dba7-150">Данные этого параметра предоставляют максимальные значения для вычисляемых свойств.</span><span class="sxs-lookup"><span data-stu-id="6dba7-150">This setting data provides maximum values for evaluated properties.</span></span> <span data-ttu-id="6dba7-151">При использовании с **пропертиполици** = "независимым" для каждого из возможностей необходимо указать только один такой параметр для каждого конкретного экземпляра данных параметра.</span><span class="sxs-lookup"><span data-stu-id="6dba7-151">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="6dba7-152">Если ограничение не ограничено значением минимума для одного и того же набора свойств, то все значения, сравниваемые ниже указанных значений, также считаются поддерживаемыми экземпляром связанных возможностей.</span><span class="sxs-lookup"><span data-stu-id="6dba7-152">Unless restricted by a Minimums value on the same set of properties, all values that compare lower than the specified values are also considered to be supported by the associated capabilities instance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <span data-ttu-id="6dba7-153"><dt>**Приращение**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6dba7-153"><dt>**Increments**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="6dba7-154">Данные этого параметра предоставляют значения приращения для вычисляемых свойств.</span><span class="sxs-lookup"><span data-stu-id="6dba7-154">This setting data provides increment values for evaluated properties.</span></span> <span data-ttu-id="6dba7-155">Для связанных возможностей, если оцененное свойство в настоящее время не имеет соответствующих минимальных или максимальных значений, свойство не влияет на.</span><span class="sxs-lookup"><span data-stu-id="6dba7-155">For the associated capabilities, if an evaluated property currently has no corresponding Minimums or Maximums values, then the property has no affect.</span></span> <span data-ttu-id="6dba7-156">В противном случае для каждого оцененного свойства его значение (*x*) должно находиться между *минимумвалуе* и *MaximumValue*, включительно, и должно иметь свойство, которое как результат *MaximumValue* минус *x* , так и результат *x* минус *минимумвалуе* , являются целыми числами, кратными *инкременту*.</span><span class="sxs-lookup"><span data-stu-id="6dba7-156">Otherwise, for each evaluated property, its value (*x*) must be between the *MinimumValue* and *MaximumValue*, inclusively, and must have the property that both the result of *MaximumValue* minus *x* and the result of *x* minus *MinimumValue* are each an integer multiple of the *Increment*.</span></span> <span data-ttu-id="6dba7-157">Если параметр *минимумвалуе* или *MaximumValue* не указан, а другой —, то значение Missing должно быть соответственно самым низким или самым высоким поддерживаемым значением для типа данных свойства.</span><span class="sxs-lookup"><span data-stu-id="6dba7-157">If either *MinimumValue* or *MaximumValue* is not specified and the other is, then the missing value must be respectively assumed to be the lowest or highest supported value for the property's data type.</span></span> <span data-ttu-id="6dba7-158">Кроме того, если для оцененного свойства указаны как *минимумвалуе* , так и *MaximumValue* , результат *MaximumValue* минус *минимумвалуе* должен быть целым числом, кратным *инкременту*.</span><span class="sxs-lookup"><span data-stu-id="6dba7-158">Additionally, if both a *MinimumValue* and a *MaximumValue* are specified for an evaluated property, then the result of *MaximumValue* minus *MinimumValue* must be an integer multiple of the *Increment*.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="6dba7-159">**валуероле**</span><span class="sxs-lookup"><span data-stu-id="6dba7-159">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dba7-160">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6dba7-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6dba7-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6dba7-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dba7-162">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="6dba7-162">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6dba7-163">Задает дополнительную семантику для интерпретации **ненулевых** неключевых свойств данных параметров.</span><span class="sxs-lookup"><span data-stu-id="6dba7-163">Specifies further semantics on the interpretation of the non-**Null**, non-key properties of the setting data.</span></span> <span data-ttu-id="6dba7-164">Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6dba7-164">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="6dba7-165">Значение</span><span class="sxs-lookup"><span data-stu-id="6dba7-165">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="6dba7-166">Значение</span><span class="sxs-lookup"><span data-stu-id="6dba7-166">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="6dba7-167"><dt>**По умолчанию**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6dba7-167"><dt>**Default**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="6dba7-168">Значения свойств данных параметров будут использоваться в качестве значений по умолчанию при создании нового экземпляра данных параметров для элементов, возможности которых определяются связанными возможностями.</span><span class="sxs-lookup"><span data-stu-id="6dba7-168">The property values of the setting data will be used as default values, when a new setting data instance is created for elements whose capabilities are defined by the associated capabilities.</span></span> <span data-ttu-id="6dba7-169">В разных экземплярах данных параметра для определенных свойств, имеющих одинаковое семантическое назначение, в качестве значения по умолчанию необходимо указать не более одного экземпляра данных параметров.</span><span class="sxs-lookup"><span data-stu-id="6dba7-169">Across instances of the setting data, for particular properties having the same semantic purpose, at most one such setting data instance must be specified as a default.</span></span><br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <span data-ttu-id="6dba7-170"><dt>**Оптимальный**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6dba7-170"><dt>**Optimal**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="6dba7-171">Экземпляр данных Setting представляет оптимальные значения параметров для элементов, связанных с соответствующими возможностями.</span><span class="sxs-lookup"><span data-stu-id="6dba7-171">The setting data instance represents optimal setting values for elements associated with the associated capabilities.</span></span> <span data-ttu-id="6dba7-172">Экземпляры данных параметров нескольких компонентов могут быть объявлены как оптимальные.</span><span class="sxs-lookup"><span data-stu-id="6dba7-172">Multiple component setting data instances may be declared as optimal.</span></span><br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <span data-ttu-id="6dba7-173"><dt>**Среднее значение**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6dba7-173"><dt>**Mean**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="6dba7-174">**Ненулевые**, неключевые, неперечислимые, не являющиеся логическими, Нелогические свойства, которые являются числовыми свойствами связанного экземпляра данных параметров, представляют среднюю точку по отношению к определенному измерению.</span><span class="sxs-lookup"><span data-stu-id="6dba7-174">The non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the associated setting data instance represents an average point along some dimension.</span></span> <span data-ttu-id="6dba7-175">Для различных сочетаний параметров свойств данных экземпляры данных параметров нескольких компонентов могут быть объявлены как **средние**.</span><span class="sxs-lookup"><span data-stu-id="6dba7-175">For different combinations of setting data properties, multiple component setting data instances may be declared as **Mean**.</span></span> <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <span data-ttu-id="6dba7-176"><dt>**Поддерживается**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6dba7-176"><dt>**Supported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="6dba7-177">**Ненулевые**, неключевые свойства данных параметров представляют набор поддерживаемых значений свойств, которые в противном случае не являются полными.</span><span class="sxs-lookup"><span data-stu-id="6dba7-177">The non-**Null**, non-key properties of the setting data represents a set of supported property values that are not otherwise qualified.</span></span> <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6dba7-178">Требования</span><span class="sxs-lookup"><span data-stu-id="6dba7-178">Requirements</span></span>



| <span data-ttu-id="6dba7-179">Требование</span><span class="sxs-lookup"><span data-stu-id="6dba7-179">Requirement</span></span> | <span data-ttu-id="6dba7-180">Значение</span><span class="sxs-lookup"><span data-stu-id="6dba7-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dba7-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6dba7-181">Minimum supported client</span></span><br/> | <span data-ttu-id="6dba7-182">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6dba7-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6dba7-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6dba7-183">Minimum supported server</span></span><br/> | <span data-ttu-id="6dba7-184">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6dba7-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6dba7-185">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6dba7-185">Namespace</span></span><br/>                | <span data-ttu-id="6dba7-186">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6dba7-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6dba7-187">MOF</span><span class="sxs-lookup"><span data-stu-id="6dba7-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6dba7-188"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6dba7-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6dba7-189">DLL</span><span class="sxs-lookup"><span data-stu-id="6dba7-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dba7-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6dba7-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

