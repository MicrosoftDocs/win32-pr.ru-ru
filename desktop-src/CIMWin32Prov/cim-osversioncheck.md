---
description: Класс CIM \_ осверсиончекк указывает версии операционной системы, которые могут поддерживать программный элемент.
ms.assetid: 6796cfc4-3b6f-43a4-b5f0-854a95284238
ms.tgt_platform: multiple
title: Класс CIM_OSVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck
- CIM_OSVersionCheck.CheckID
- CIM_OSVersionCheck.Caption
- CIM_OSVersionCheck.Description
- CIM_OSVersionCheck.CheckMode
- CIM_OSVersionCheck.Name
- CIM_OSVersionCheck.TargetOperatingSystem
- CIM_OSVersionCheck.Version
- CIM_OSVersionCheck.SoftwareElementID
- CIM_OSVersionCheck.SoftwareElementState
- CIM_OSVersionCheck.MaximumVersion
- CIM_OSVersionCheck.MinimumVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c341b9038b5b40b559b4a121adb88fbb2d7b5205
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072466"
---
# <a name="cim_osversioncheck-class"></a><span data-ttu-id="7c39e-103">\_Класс CIM осверсиончекк</span><span class="sxs-lookup"><span data-stu-id="7c39e-103">CIM\_OSVersionCheck class</span></span>

<span data-ttu-id="7c39e-104">Класс **CIM \_ осверсиончекк** указывает версии операционной системы, которые могут поддерживать программный элемент.</span><span class="sxs-lookup"><span data-stu-id="7c39e-104">The **CIM\_OSVersionCheck** class specifies the versions of the operating system that can support a software element.</span></span> <span data-ttu-id="7c39e-105">Проверка может выполняться для определенного, минимального, максимального или диапазона выпусков операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7c39e-105">The check can be run for a specific, minimum, maximum, or a range of operating system releases.</span></span> <span data-ttu-id="7c39e-106">Чтобы указать конкретную версию операционной системы, минимальная и максимальная версии должны быть равны.</span><span class="sxs-lookup"><span data-stu-id="7c39e-106">To specify a specific operating system version, the minimum and maximum versions must be equal.</span></span> <span data-ttu-id="7c39e-107">Чтобы указать минимальную версию, необходимо указать только минимальную версию.</span><span class="sxs-lookup"><span data-stu-id="7c39e-107">To specify the minimum version, the minimum version only must be specified.</span></span> <span data-ttu-id="7c39e-108">Чтобы указать максимальную версию, необходимо указать только максимальную версию.</span><span class="sxs-lookup"><span data-stu-id="7c39e-108">To specify a maximum version, the maximum version only needs to be specified.</span></span> <span data-ttu-id="7c39e-109">Чтобы указать диапазон, необходимо указать как минимальную, так и максимальную версии.</span><span class="sxs-lookup"><span data-stu-id="7c39e-109">To specify a range, both minimum and maximum versions must be specified.</span></span>

<span data-ttu-id="7c39e-110">Тип операционной системы указывается в свойстве **таржетоператингсистем** программного элемента-владельца.</span><span class="sxs-lookup"><span data-stu-id="7c39e-110">The type of operating system is specified in the **TargetOperatingSystem** property of the owning software element.</span></span> <span data-ttu-id="7c39e-111">Подробные сведения о проверках сравниваются с соответствующими сведениями в объекте [**\_ операционной системы CIM**](cim-operatingsystem.md) , на который ссылается Ассоциация [**\_ инсталледос CIM**](cim-installedos.md) для объекта [**CIM \_ ComputerSystem**](cim-computersystem.md) , описывающего среду.</span><span class="sxs-lookup"><span data-stu-id="7c39e-111">Details of the checks are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="7c39e-112">По крайней мере один класс **\_ операционной системы CIM** должен удовлетворять сведениям о условии, чтобы проверка была удовлетворена.</span><span class="sxs-lookup"><span data-stu-id="7c39e-112">At least one **CIM\_OperatingSystem** class must satisfy the details of the condition for the check to be satisfied.</span></span> <span data-ttu-id="7c39e-113">Иными словами, не все операционные системы на соответствующей компьютерной системе должны соответствовать условию.</span><span class="sxs-lookup"><span data-stu-id="7c39e-113">In other words, not all of the operating systems on the relevant computer system need to satisfy the condition.</span></span> <span data-ttu-id="7c39e-114">Кроме того, свойство **OSType** класса версии **системы \_ CIM** должно соответствовать типу свойства **таржетоператингсистем** .</span><span class="sxs-lookup"><span data-stu-id="7c39e-114">Also, the **OSType** property of the **CIM\_OperatingSystem** class must match the type of the **TargetOperatingSystem** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c39e-115">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7c39e-115">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7c39e-116">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7c39e-116">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7c39e-117">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7c39e-117">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7c39e-118">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7c39e-118">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c39e-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c39e-119">Syntax</span></span>

``` syntax
[UUID("{FEE8368A-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_OSVersionCheck : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  string  MaximumVersion;
  string  MinimumVersion;
};
```

## <a name="members"></a><span data-ttu-id="7c39e-120">Члены</span><span class="sxs-lookup"><span data-stu-id="7c39e-120">Members</span></span>

<span data-ttu-id="7c39e-121">Класс **CIM \_ осверсиончекк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7c39e-121">The **CIM\_OSVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="7c39e-122">Методы</span><span class="sxs-lookup"><span data-stu-id="7c39e-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="7c39e-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="7c39e-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7c39e-124">Методы</span><span class="sxs-lookup"><span data-stu-id="7c39e-124">Methods</span></span>

<span data-ttu-id="7c39e-125">Класс **CIM \_ осверсиончекк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7c39e-125">The **CIM\_OSVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="7c39e-126">Метод</span><span class="sxs-lookup"><span data-stu-id="7c39e-126">Method</span></span>                                                      | <span data-ttu-id="7c39e-127">Описание</span><span class="sxs-lookup"><span data-stu-id="7c39e-127">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="7c39e-128">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="7c39e-128">**Invoke**</span></span>](invoke-method-in-class-cim-osversioncheck.md) | <span data-ttu-id="7c39e-129">Выполняет определенное действие.</span><span class="sxs-lookup"><span data-stu-id="7c39e-129">Takes a particular action.</span></span> <span data-ttu-id="7c39e-130">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="7c39e-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7c39e-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="7c39e-131">Properties</span></span>

<span data-ttu-id="7c39e-132">Класс **CIM \_ осверсиончекк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7c39e-132">The **CIM\_OSVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c39e-133">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7c39e-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7c39e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-136">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7c39e-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-137">Краткое текстовое описание субъекта.</span><span class="sxs-lookup"><span data-stu-id="7c39e-137">A short textual description of the subject.</span></span>

<span data-ttu-id="7c39e-138">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="7c39e-138">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c39e-139">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="7c39e-139">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7c39e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-142">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7c39e-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-143">Идентификатор, используемый в сочетании с другими ключами для уникальной идентификации проверки.</span><span class="sxs-lookup"><span data-stu-id="7c39e-143">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="7c39e-144">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="7c39e-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c39e-145">**чеккмоде**</span><span class="sxs-lookup"><span data-stu-id="7c39e-145">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-146">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7c39e-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-148">Если **значение равно true**, то условие должно существовать в среде.</span><span class="sxs-lookup"><span data-stu-id="7c39e-148">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="7c39e-149">Например, предполагается, что файл находится в системе, поэтому метод [**Invoke**](invoke-method-in-class-cim-check.md) должен возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="7c39e-149">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="7c39e-150">Если **значение равно false**, условие не должно существовать.</span><span class="sxs-lookup"><span data-stu-id="7c39e-150">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="7c39e-151">Например, файл не находится в системе, поэтому метод [**Invoke**](invoke-method-in-class-cim-check.md) должен возвращать **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7c39e-151">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="7c39e-152">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="7c39e-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c39e-153">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7c39e-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7c39e-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-156">Описание объектов.</span><span class="sxs-lookup"><span data-stu-id="7c39e-156">A description of the objects.</span></span>

<span data-ttu-id="7c39e-157">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="7c39e-157">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c39e-158">**MaximumVersion**</span><span class="sxs-lookup"><span data-stu-id="7c39e-158">**MaximumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7c39e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-161">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**модель \_ CIM**](cim-operatingsystem.md).**Версия**")</span><span class="sxs-lookup"><span data-stu-id="7c39e-161">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-162">Максимальная версия требуемой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7c39e-162">Maximum version of the required operating system.</span></span>

<span data-ttu-id="7c39e-163">Значение кодируется в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="7c39e-163">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="7c39e-164"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="7c39e-164"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="7c39e-165"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="7c39e-165"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="7c39e-166">**MinimumVersion**</span><span class="sxs-lookup"><span data-stu-id="7c39e-166">**MinimumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7c39e-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-169">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**модель \_ CIM**](cim-operatingsystem.md).**Версия**")</span><span class="sxs-lookup"><span data-stu-id="7c39e-169">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-170">Минимальная версия требуемой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7c39e-170">Minimum version of the required operating system.</span></span>

<span data-ttu-id="7c39e-171">Значение кодируется в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="7c39e-171">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="7c39e-172"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="7c39e-172"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="7c39e-173"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="7c39e-173"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="7c39e-174">**Name**</span><span class="sxs-lookup"><span data-stu-id="7c39e-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7c39e-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-177">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7c39e-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-178">Имя, используемое для распознавания программного элемента</span><span class="sxs-lookup"><span data-stu-id="7c39e-178">Name used to identify the software element</span></span>

<span data-ttu-id="7c39e-179">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="7c39e-179">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c39e-180">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="7c39e-180">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7c39e-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-183">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементид**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7c39e-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-184">Это идентификатор этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="7c39e-184">This is an identifier for this software element.</span></span>

<span data-ttu-id="7c39e-185">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="7c39e-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c39e-186">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="7c39e-186">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-187">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c39e-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-189">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементстате**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7c39e-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-190">Состояние программного элемента программного элемента.</span><span class="sxs-lookup"><span data-stu-id="7c39e-190">The software element state of a software element.</span></span>

<span data-ttu-id="7c39e-191">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="7c39e-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="7c39e-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="7c39e-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-193">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="7c39e-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="7c39e-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="7c39e-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-195">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="7c39e-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="7c39e-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="7c39e-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-197">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="7c39e-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="7c39e-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="7c39e-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-199">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="7c39e-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7c39e-200">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="7c39e-200">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-201">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c39e-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-203">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Таржетоператингсистем**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="7c39e-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-204">Целевая операционная система программного элемента.</span><span class="sxs-lookup"><span data-stu-id="7c39e-204">Target operating system of the software element.</span></span>

<span data-ttu-id="7c39e-205">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="7c39e-205">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c39e-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7c39e-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7c39e-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7c39e-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="7c39e-208"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="7c39e-208"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-209">MacOS</span><span class="sxs-lookup"><span data-stu-id="7c39e-209">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="7c39e-210"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="7c39e-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-211">АТРИ UNIX</span><span class="sxs-lookup"><span data-stu-id="7c39e-211">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="7c39e-212"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="7c39e-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="7c39e-213"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="7c39e-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="7c39e-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="7c39e-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="7c39e-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="7c39e-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-216">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="7c39e-216">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="7c39e-217"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="7c39e-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-218">HP-UX</span><span class="sxs-lookup"><span data-stu-id="7c39e-218">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="7c39e-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="7c39e-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="7c39e-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="7c39e-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="7c39e-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="7c39e-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="7c39e-222"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="7c39e-222"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="7c39e-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="7c39e-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-224">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="7c39e-224">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="7c39e-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="7c39e-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="7c39e-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="7c39e-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-227">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="7c39e-227">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="7c39e-228"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="7c39e-228"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-229">Windows 95</span><span class="sxs-lookup"><span data-stu-id="7c39e-229">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="7c39e-230"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="7c39e-230"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-231">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7c39e-231">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="7c39e-232"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="7c39e-232"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-233">Windows NT</span><span class="sxs-lookup"><span data-stu-id="7c39e-233">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="7c39e-234"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="7c39e-234"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-235">Windows CE</span><span class="sxs-lookup"><span data-stu-id="7c39e-235">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="7c39e-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="7c39e-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-237">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="7c39e-237">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="7c39e-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="7c39e-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="7c39e-239"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="7c39e-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="7c39e-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="7c39e-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="7c39e-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="7c39e-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="7c39e-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="7c39e-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="7c39e-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="7c39e-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="7c39e-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="7c39e-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="7c39e-245"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="7c39e-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="7c39e-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="7c39e-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="7c39e-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="7c39e-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="7c39e-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="7c39e-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="7c39e-249"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="7c39e-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-250">Серия</span><span class="sxs-lookup"><span data-stu-id="7c39e-250">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="7c39e-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="7c39e-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-252">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="7c39e-252">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="7c39e-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="7c39e-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-254">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="7c39e-254">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="7c39e-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="7c39e-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-256">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="7c39e-256">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="7c39e-257"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="7c39e-257"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="7c39e-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="7c39e-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="7c39e-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="7c39e-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="7c39e-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="7c39e-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="7c39e-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="7c39e-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="7c39e-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="7c39e-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-263">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="7c39e-263">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="7c39e-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="7c39e-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="7c39e-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="7c39e-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="7c39e-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="7c39e-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="7c39e-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="7c39e-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-268">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="7c39e-268">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="7c39e-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="7c39e-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="7c39e-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="7c39e-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="7c39e-271"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="7c39e-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="7c39e-272"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="7c39e-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="7c39e-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="7c39e-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="7c39e-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="7c39e-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="7c39e-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="7c39e-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="7c39e-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="7c39e-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="7c39e-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="7c39e-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="7c39e-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="7c39e-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="7c39e-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="7c39e-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="7c39e-280">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="7c39e-280">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="7c39e-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="7c39e-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="7c39e-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="7c39e-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="7c39e-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="7c39e-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="7c39e-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="7c39e-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="7c39e-285"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="7c39e-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7c39e-286">**Version**</span><span class="sxs-lookup"><span data-stu-id="7c39e-286">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c39e-287">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7c39e-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c39e-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c39e-289">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Версия**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="7c39e-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="7c39e-290">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="7c39e-290">Version of the operation.</span></span>

<span data-ttu-id="7c39e-291">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="7c39e-291">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="7c39e-292"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="7c39e-292"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="7c39e-293"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="7c39e-293"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="7c39e-294">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="7c39e-294">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c39e-295">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c39e-295">Remarks</span></span>

<span data-ttu-id="7c39e-296">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7c39e-296">WMI does not implement this class.</span></span>

<span data-ttu-id="7c39e-297">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7c39e-297">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7c39e-298">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7c39e-298">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c39e-299">Требования</span><span class="sxs-lookup"><span data-stu-id="7c39e-299">Requirements</span></span>



| <span data-ttu-id="7c39e-300">Требование</span><span class="sxs-lookup"><span data-stu-id="7c39e-300">Requirement</span></span> | <span data-ttu-id="7c39e-301">Значение</span><span class="sxs-lookup"><span data-stu-id="7c39e-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c39e-302">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c39e-302">Minimum supported client</span></span><br/> | <span data-ttu-id="7c39e-303">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c39e-303">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c39e-304">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c39e-304">Minimum supported server</span></span><br/> | <span data-ttu-id="7c39e-305">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c39e-305">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c39e-306">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7c39e-306">Namespace</span></span><br/>                | <span data-ttu-id="7c39e-307">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7c39e-307">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c39e-308">MOF</span><span class="sxs-lookup"><span data-stu-id="7c39e-308">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c39e-309"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c39e-309"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c39e-310">DLL</span><span class="sxs-lookup"><span data-stu-id="7c39e-310">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c39e-311"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c39e-311"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c39e-312">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c39e-312">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c39e-313">**\_Проверка CIM**</span><span class="sxs-lookup"><span data-stu-id="7c39e-313">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

