---
description: Класс CIM \_ сеттингчекк определяет сведения, необходимые для проверки конкретного файла параметров для конкретной записи, которая содержит значение, равное указанному значению. Предполагается, что все сравнения не чувствительны к регистру.
ms.assetid: 0e40276c-e794-4ea1-8937-c6d7f110f97d
ms.tgt_platform: multiple
title: Класс CIM_SettingCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingCheck
- CIM_SettingCheck.Caption
- CIM_SettingCheck.CheckID
- CIM_SettingCheck.CheckMode
- CIM_SettingCheck.CheckType
- CIM_SettingCheck.Description
- CIM_SettingCheck.EntryName
- CIM_SettingCheck.EntryValue
- CIM_SettingCheck.FileName
- CIM_SettingCheck.Name
- CIM_SettingCheck.SectionKey
- CIM_SettingCheck.SoftwareElementID
- CIM_SettingCheck.SoftwareElementState
- CIM_SettingCheck.TargetOperatingSystem
- CIM_SettingCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4b360833f216d9feb839a4ed84a0e1ba4cd61ebf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655822"
---
# <a name="cim_settingcheck-class"></a><span data-ttu-id="dbddb-104">\_Класс CIM сеттингчекк</span><span class="sxs-lookup"><span data-stu-id="dbddb-104">CIM\_SettingCheck class</span></span>

<span data-ttu-id="dbddb-105">Класс **CIM \_ сеттингчекк** определяет сведения, необходимые для проверки конкретного файла параметров для конкретной записи, которая содержит значение, равное указанному значению.</span><span class="sxs-lookup"><span data-stu-id="dbddb-105">The **CIM\_SettingCheck** class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="dbddb-106">Предполагается, что все сравнения не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="dbddb-106">All comparisons are assumed to be case insensitive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbddb-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="dbddb-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dbddb-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dbddb-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dbddb-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dbddb-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dbddb-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="dbddb-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbddb-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbddb-111">Syntax</span></span>

``` syntax
[UUID("{DC1D8140-DB30-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SettingCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  uint16  CheckType;
  string  Description;
  string  EntryName;
  string  EntryValue;
  string  FileName;
  string  Name;
  string  SectionKey;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="dbddb-112">Члены</span><span class="sxs-lookup"><span data-stu-id="dbddb-112">Members</span></span>

<span data-ttu-id="dbddb-113">Класс **CIM \_ сеттингчекк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dbddb-113">The **CIM\_SettingCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="dbddb-114">Методы</span><span class="sxs-lookup"><span data-stu-id="dbddb-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="dbddb-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbddb-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dbddb-116">Методы</span><span class="sxs-lookup"><span data-stu-id="dbddb-116">Methods</span></span>

<span data-ttu-id="dbddb-117">Класс **CIM \_ сеттингчекк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dbddb-117">The **CIM\_SettingCheck** class has these methods.</span></span>



| <span data-ttu-id="dbddb-118">Метод</span><span class="sxs-lookup"><span data-stu-id="dbddb-118">Method</span></span>                                                    | <span data-ttu-id="dbddb-119">Описание</span><span class="sxs-lookup"><span data-stu-id="dbddb-119">Description</span></span>                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="dbddb-120">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="dbddb-120">**Invoke**</span></span>](invoke-method-in-class-cim-settingcheck.md) | <span data-ttu-id="dbddb-121">Выполняет определенное действие.</span><span class="sxs-lookup"><span data-stu-id="dbddb-121">Takes a particular action.</span></span> <span data-ttu-id="dbddb-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="dbddb-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dbddb-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbddb-123">Properties</span></span>

<span data-ttu-id="dbddb-124">Класс **CIM \_ сеттингчекк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dbddb-124">The **CIM\_SettingCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbddb-125">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dbddb-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbddb-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-128">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="dbddb-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-129">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dbddb-129">Short textual description of the object.</span></span>

<span data-ttu-id="dbddb-130">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="dbddb-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbddb-131">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="dbddb-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbddb-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-134">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dbddb-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-135">Идентификатор, используемый в сочетании с другими ключами для уникальной идентификации проверки.</span><span class="sxs-lookup"><span data-stu-id="dbddb-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span> <span data-ttu-id="dbddb-136">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="dbddb-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbddb-137">**чеккмоде**</span><span class="sxs-lookup"><span data-stu-id="dbddb-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-138">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dbddb-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-140">Если **значение равно true**, то условие должно существовать в среде (например, если файл находится в системе, метод [**Invoke**](invoke-method-in-class-cim-settingcheck.md) должен возвращать **значение true**).</span><span class="sxs-lookup"><span data-stu-id="dbddb-140">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-settingcheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="dbddb-141">Если **значение равно false**, условие не должно существовать (например, если файл не находится в системе, метод **Invoke** должен возвращать **значение false**).</span><span class="sxs-lookup"><span data-stu-id="dbddb-141">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="dbddb-142">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="dbddb-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbddb-143">**чекктипе**</span><span class="sxs-lookup"><span data-stu-id="dbddb-143">**CheckType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbddb-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-146">Способ сравнения значения параметра.</span><span class="sxs-lookup"><span data-stu-id="dbddb-146">Way in which the setting value should be compared.</span></span>

<dt>

<span id="Matches"></span><span id="matches"></span><span id="MATCHES"></span>

<span data-ttu-id="dbddb-147">**Соответствует** (0)</span><span class="sxs-lookup"><span data-stu-id="dbddb-147">**Matches** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Contains"></span><span id="contains"></span><span id="CONTAINS"></span>

<span data-ttu-id="dbddb-148">**Содержит** (1)</span><span class="sxs-lookup"><span data-stu-id="dbddb-148">**Contains** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbddb-149">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dbddb-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbddb-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-152">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dbddb-152">Description of the object.</span></span>

<span data-ttu-id="dbddb-153">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="dbddb-153">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbddb-154">**ИмяЗаписи**</span><span class="sxs-lookup"><span data-stu-id="dbddb-154">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbddb-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-157">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dbddb-157">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-158">Имя проверяемой записи</span><span class="sxs-lookup"><span data-stu-id="dbddb-158">Name of the entry to be checked</span></span>

</dd> <dt>

<span data-ttu-id="dbddb-159">**ентривалуе**</span><span class="sxs-lookup"><span data-stu-id="dbddb-159">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbddb-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-162">Значение, связанное с именованной записью для проверки.</span><span class="sxs-lookup"><span data-stu-id="dbddb-162">Value that is associated with the named entry to check.</span></span>

</dd> <dt>

<span data-ttu-id="dbddb-163">**FileName**</span><span class="sxs-lookup"><span data-stu-id="dbddb-163">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbddb-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-166">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="dbddb-166">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-167">Имя файла параметров для проверки.</span><span class="sxs-lookup"><span data-stu-id="dbddb-167">File name of the setting file to check.</span></span>

</dd> <dt>

<span data-ttu-id="dbddb-168">**Name**</span><span class="sxs-lookup"><span data-stu-id="dbddb-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbddb-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-171">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dbddb-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-172">Имя, используемое для распознавания программного элемента.</span><span class="sxs-lookup"><span data-stu-id="dbddb-172">Name used to identify the software element.</span></span> <span data-ttu-id="dbddb-173">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="dbddb-173">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbddb-174">**сектионкэй**</span><span class="sxs-lookup"><span data-stu-id="dbddb-174">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbddb-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-177">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dbddb-177">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-178">Ключ раздела, содержащий параметры для проверки.</span><span class="sxs-lookup"><span data-stu-id="dbddb-178">Key of section that contains the settings to check.</span></span>

</dd> <dt>

<span data-ttu-id="dbddb-179">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="dbddb-179">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbddb-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-182">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементид**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dbddb-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-183">Идентификатор программного элемента.</span><span class="sxs-lookup"><span data-stu-id="dbddb-183">Identifier for the software element.</span></span>

<span data-ttu-id="dbddb-184">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="dbddb-184">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbddb-185">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="dbddb-185">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-186">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbddb-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-188">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементстате**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dbddb-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-189">Состояние программного элемента.</span><span class="sxs-lookup"><span data-stu-id="dbddb-189">State of a software element.</span></span>

<span data-ttu-id="dbddb-190">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="dbddb-190">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="dbddb-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="dbddb-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-192">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="dbddb-192">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="dbddb-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="dbddb-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-194">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="dbddb-194">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="dbddb-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="dbddb-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-196">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="dbddb-196">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="dbddb-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="dbddb-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-198">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="dbddb-198">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbddb-199">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="dbddb-199">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-200">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbddb-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-202">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Таржетоператингсистем**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="dbddb-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-203">Целевая операционная система программного элемента.</span><span class="sxs-lookup"><span data-stu-id="dbddb-203">Target operating system of the software element.</span></span>

<span data-ttu-id="dbddb-204">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="dbddb-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbddb-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dbddb-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbddb-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dbddb-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="dbddb-207"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="dbddb-207"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-208">MacOS</span><span class="sxs-lookup"><span data-stu-id="dbddb-208">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="dbddb-209"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="dbddb-209"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-210">АТРИ UNIX</span><span class="sxs-lookup"><span data-stu-id="dbddb-210">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="dbddb-211"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="dbddb-211"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="dbddb-212"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="dbddb-212"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="dbddb-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="dbddb-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="dbddb-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="dbddb-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-215">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="dbddb-215">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="dbddb-216"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="dbddb-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-217">HP-UX</span><span class="sxs-lookup"><span data-stu-id="dbddb-217">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="dbddb-218"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="dbddb-218"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="dbddb-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="dbddb-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="dbddb-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="dbddb-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="dbddb-221"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="dbddb-221"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="dbddb-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="dbddb-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-223">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="dbddb-223">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="dbddb-224"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="dbddb-224"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="dbddb-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="dbddb-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-226">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="dbddb-226">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="dbddb-227"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="dbddb-227"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-228">Windows 95</span><span class="sxs-lookup"><span data-stu-id="dbddb-228">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="dbddb-229"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="dbddb-229"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-230">Windows 98</span><span class="sxs-lookup"><span data-stu-id="dbddb-230">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="dbddb-231"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="dbddb-231"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-232">Windows NT</span><span class="sxs-lookup"><span data-stu-id="dbddb-232">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="dbddb-233"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="dbddb-233"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-234">Windows CE</span><span class="sxs-lookup"><span data-stu-id="dbddb-234">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="dbddb-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="dbddb-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-236">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="dbddb-236">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="dbddb-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="dbddb-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="dbddb-238"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="dbddb-238"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="dbddb-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="dbddb-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="dbddb-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="dbddb-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="dbddb-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="dbddb-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="dbddb-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="dbddb-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="dbddb-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="dbddb-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="dbddb-244"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="dbddb-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="dbddb-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="dbddb-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="dbddb-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="dbddb-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="dbddb-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="dbddb-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="dbddb-248"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="dbddb-248"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-249">Серия</span><span class="sxs-lookup"><span data-stu-id="dbddb-249">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="dbddb-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="dbddb-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-251">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="dbddb-251">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="dbddb-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="dbddb-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-253">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="dbddb-253">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="dbddb-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="dbddb-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-255">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="dbddb-255">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="dbddb-256"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="dbddb-256"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="dbddb-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="dbddb-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="dbddb-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="dbddb-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="dbddb-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="dbddb-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="dbddb-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="dbddb-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="dbddb-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="dbddb-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-262">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="dbddb-262">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="dbddb-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="dbddb-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="dbddb-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="dbddb-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="dbddb-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="dbddb-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="dbddb-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="dbddb-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-267">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="dbddb-267">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="dbddb-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="dbddb-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="dbddb-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="dbddb-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="dbddb-270"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="dbddb-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="dbddb-271"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="dbddb-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="dbddb-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="dbddb-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="dbddb-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="dbddb-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="dbddb-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="dbddb-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="dbddb-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="dbddb-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="dbddb-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="dbddb-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="dbddb-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="dbddb-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="dbddb-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="dbddb-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="dbddb-279">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="dbddb-279">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="dbddb-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="dbddb-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="dbddb-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="dbddb-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="dbddb-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="dbddb-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="dbddb-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="dbddb-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="dbddb-284"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="dbddb-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbddb-285">**Version**</span><span class="sxs-lookup"><span data-stu-id="dbddb-285">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbddb-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbddb-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbddb-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbddb-288">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Версия**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="dbddb-288">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="dbddb-289">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="dbddb-289">Version of the operation.</span></span>

<span data-ttu-id="dbddb-290">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="dbddb-290">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="dbddb-291"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="dbddb-291"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="dbddb-292"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="dbddb-292"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="dbddb-293">Это свойство наследуется от [**класса \_ проверки CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="dbddb-293">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbddb-294">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbddb-294">Remarks</span></span>

<span data-ttu-id="dbddb-295">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="dbddb-295">WMI does not implement this class.</span></span>

<span data-ttu-id="dbddb-296">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="dbddb-296">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dbddb-297">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="dbddb-297">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbddb-298">Требования</span><span class="sxs-lookup"><span data-stu-id="dbddb-298">Requirements</span></span>



| <span data-ttu-id="dbddb-299">Требование</span><span class="sxs-lookup"><span data-stu-id="dbddb-299">Requirement</span></span> | <span data-ttu-id="dbddb-300">Значение</span><span class="sxs-lookup"><span data-stu-id="dbddb-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbddb-301">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbddb-301">Minimum supported client</span></span><br/> | <span data-ttu-id="dbddb-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbddb-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dbddb-303">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbddb-303">Minimum supported server</span></span><br/> | <span data-ttu-id="dbddb-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbddb-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dbddb-305">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dbddb-305">Namespace</span></span><br/>                | <span data-ttu-id="dbddb-306">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dbddb-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dbddb-307">MOF</span><span class="sxs-lookup"><span data-stu-id="dbddb-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbddb-308"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbddb-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbddb-309">DLL</span><span class="sxs-lookup"><span data-stu-id="dbddb-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbddb-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbddb-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbddb-311">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbddb-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbddb-312">**\_Проверка CIM**</span><span class="sxs-lookup"><span data-stu-id="dbddb-312">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

