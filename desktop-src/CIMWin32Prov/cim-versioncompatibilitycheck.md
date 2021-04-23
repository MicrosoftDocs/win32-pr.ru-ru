---
description: Класс CIM \_ версионкомпатибилитичекк указывает, разрешено ли создание следующего состояния программного элемента.
ms.assetid: 3a04c489-e44e-44c7-8945-d6047ba0d6df
ms.tgt_platform: multiple
title: Класс CIM_VersionCompatibilityCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck
- CIM_VersionCompatibilityCheck.CheckID
- CIM_VersionCompatibilityCheck.Caption
- CIM_VersionCompatibilityCheck.Description
- CIM_VersionCompatibilityCheck.CheckMode
- CIM_VersionCompatibilityCheck.Name
- CIM_VersionCompatibilityCheck.TargetOperatingSystem
- CIM_VersionCompatibilityCheck.Version
- CIM_VersionCompatibilityCheck.SoftwareElementID
- CIM_VersionCompatibilityCheck.SoftwareElementState
- CIM_VersionCompatibilityCheck.AllowDownVersion
- CIM_VersionCompatibilityCheck.AllowMultipleVersions
- CIM_VersionCompatibilityCheck.Reinstall
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 00a37d52add8c9697371fd0ee8d0a24d9c487f61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990526"
---
# <a name="cim_versioncompatibilitycheck-class"></a><span data-ttu-id="f639f-103">\_Класс CIM версионкомпатибилитичекк</span><span class="sxs-lookup"><span data-stu-id="f639f-103">CIM\_VersionCompatibilityCheck class</span></span>

<span data-ttu-id="f639f-104">Класс **CIM \_ версионкомпатибилитичекк** указывает, разрешено ли создание следующего состояния программного элемента.</span><span class="sxs-lookup"><span data-stu-id="f639f-104">The **CIM\_VersionCompatibilityCheck** class specifies whether it is permissible to create the next state of a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f639f-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f639f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f639f-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f639f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f639f-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f639f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f639f-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f639f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f639f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f639f-109">Syntax</span></span>

``` syntax
[UUID("{D368CA4A-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VersionCompatibilityCheck : CIM_Check
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
  boolean AllowDownVersion;
  boolean AllowMultipleVersions;
  boolean Reinstall;
};
```

## <a name="members"></a><span data-ttu-id="f639f-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f639f-110">Members</span></span>

<span data-ttu-id="f639f-111">Класс **CIM \_ версионкомпатибилитичекк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f639f-111">The **CIM\_VersionCompatibilityCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="f639f-112">Методы</span><span class="sxs-lookup"><span data-stu-id="f639f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f639f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f639f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f639f-114">Методы</span><span class="sxs-lookup"><span data-stu-id="f639f-114">Methods</span></span>

<span data-ttu-id="f639f-115">Класс **CIM \_ версионкомпатибилитичекк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f639f-115">The **CIM\_VersionCompatibilityCheck** class has these methods.</span></span>



| <span data-ttu-id="f639f-116">Метод</span><span class="sxs-lookup"><span data-stu-id="f639f-116">Method</span></span>                                                                 | <span data-ttu-id="f639f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f639f-117">Description</span></span>                                                   |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="f639f-118">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="f639f-118">**Invoke**</span></span>](invoke-method-in-class-cim-versioncompatibilitycheck.md) | <span data-ttu-id="f639f-119">Выполняет определенное действие.</span><span class="sxs-lookup"><span data-stu-id="f639f-119">Takes a particular action.</span></span> <span data-ttu-id="f639f-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="f639f-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f639f-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="f639f-121">Properties</span></span>

<span data-ttu-id="f639f-122">Класс **CIM \_ версионкомпатибилитичекк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f639f-122">The **CIM\_VersionCompatibilityCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f639f-123">**алловдовнверсион**</span><span class="sxs-lookup"><span data-stu-id="f639f-123">**AllowDownVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-124">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f639f-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f639f-126">Если **значение — true**, программный элемент может перейти к следующему состоянию независимо от того, существует ли в среде более новая или последняя версия программного элемента.</span><span class="sxs-lookup"><span data-stu-id="f639f-126">If **TRUE**, the software element can transition to its next state whether or not if a higher or latter version of the software element already exists in the environment.</span></span>

</dd> <dt>

<span data-ttu-id="f639f-127">**алловмултиплеверсионс**</span><span class="sxs-lookup"><span data-stu-id="f639f-127">**AllowMultipleVersions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f639f-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f639f-130">Управляет возможностью настройки нескольких версий продукта в системе.</span><span class="sxs-lookup"><span data-stu-id="f639f-130">Controls the ability to configure multiple versions of a product on a system.</span></span>

</dd> <dt>

<span data-ttu-id="f639f-131">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f639f-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f639f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f639f-134">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f639f-134">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f639f-135">Краткое текстовое описание субъекта.</span><span class="sxs-lookup"><span data-stu-id="f639f-135">A short textual description of the subject.</span></span>

<span data-ttu-id="f639f-136">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f639f-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f639f-137">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="f639f-137">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f639f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f639f-140">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f639f-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f639f-141">Идентификатор, используемый в сочетании с другими ключами для уникальной идентификации проверки.</span><span class="sxs-lookup"><span data-stu-id="f639f-141">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="f639f-142">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f639f-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f639f-143">**чеккмоде**</span><span class="sxs-lookup"><span data-stu-id="f639f-143">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-144">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f639f-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f639f-146">Если **значение равно true**, то условие должно существовать в среде.</span><span class="sxs-lookup"><span data-stu-id="f639f-146">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="f639f-147">Например, предполагается, что файл находится в системе, поэтому метод [**Invoke**](invoke-method-in-class-cim-check.md) должен возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f639f-147">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="f639f-148">Если **значение равно false**, условие не должно существовать.</span><span class="sxs-lookup"><span data-stu-id="f639f-148">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="f639f-149">Например, файл не находится в системе, поэтому метод [**Invoke**](invoke-method-in-class-cim-check.md) должен возвращать **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f639f-149">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="f639f-150">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f639f-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f639f-151">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f639f-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f639f-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f639f-154">Описание объектов.</span><span class="sxs-lookup"><span data-stu-id="f639f-154">A description of the objects.</span></span>

<span data-ttu-id="f639f-155">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f639f-155">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f639f-156">**Name**</span><span class="sxs-lookup"><span data-stu-id="f639f-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f639f-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f639f-159">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f639f-159">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f639f-160">Имя, используемое для распознавания программного элемента</span><span class="sxs-lookup"><span data-stu-id="f639f-160">Name used to identify the software element</span></span>

<span data-ttu-id="f639f-161">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f639f-161">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f639f-162">**Переустановка**</span><span class="sxs-lookup"><span data-stu-id="f639f-162">**Reinstall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-163">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f639f-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f639f-165">Если **значение — true**, программный элемент может переходить к следующему состоянию, независимо от того, существует ли в среде программный элемент той же версии.</span><span class="sxs-lookup"><span data-stu-id="f639f-165">If **TRUE**, the software element can transition to its next state whether or not a software element of the same version already exists in the environment.</span></span>

</dd> <dt>

<span data-ttu-id="f639f-166">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="f639f-166">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f639f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f639f-169">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементид**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f639f-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f639f-170">Это идентификатор этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="f639f-170">This is an identifier for this software element.</span></span>

<span data-ttu-id="f639f-171">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f639f-171">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="f639f-172">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="f639f-172">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-173">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f639f-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f639f-175">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементстате**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f639f-175">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f639f-176">Состояние программного элемента программного элемента.</span><span class="sxs-lookup"><span data-stu-id="f639f-176">The software element state of a software element.</span></span>

<span data-ttu-id="f639f-177">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f639f-177">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="f639f-178"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="f639f-178"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="f639f-179"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="f639f-179"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="f639f-180"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="f639f-180"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="f639f-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="f639f-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f639f-182">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="f639f-182">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-183">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f639f-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f639f-185">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Таржетоператингсистем**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="f639f-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="f639f-186">Целевая операционная система программного элемента.</span><span class="sxs-lookup"><span data-stu-id="f639f-186">Target operating system of the software element.</span></span>

<span data-ttu-id="f639f-187">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f639f-187">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f639f-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f639f-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f639f-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f639f-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="f639f-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="f639f-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-191">MacOS</span><span class="sxs-lookup"><span data-stu-id="f639f-191">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="f639f-192"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="f639f-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-193">АТРИ UNIX</span><span class="sxs-lookup"><span data-stu-id="f639f-193">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="f639f-194"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="f639f-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="f639f-195"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="f639f-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="f639f-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="f639f-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="f639f-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="f639f-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-198">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="f639f-198">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="f639f-199"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="f639f-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-200">HP-UX</span><span class="sxs-lookup"><span data-stu-id="f639f-200">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="f639f-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="f639f-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="f639f-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="f639f-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="f639f-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="f639f-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="f639f-204"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="f639f-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="f639f-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="f639f-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-206">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="f639f-206">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="f639f-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="f639f-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="f639f-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="f639f-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-209">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="f639f-209">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="f639f-210"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="f639f-210"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-211">Windows 95</span><span class="sxs-lookup"><span data-stu-id="f639f-211">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="f639f-212"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="f639f-212"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-213">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f639f-213">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="f639f-214"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="f639f-214"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-215">Windows NT</span><span class="sxs-lookup"><span data-stu-id="f639f-215">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="f639f-216"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="f639f-216"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-217">Windows CE</span><span class="sxs-lookup"><span data-stu-id="f639f-217">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="f639f-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="f639f-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-219">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="f639f-219">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="f639f-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="f639f-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="f639f-221"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="f639f-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="f639f-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="f639f-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="f639f-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="f639f-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="f639f-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="f639f-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="f639f-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="f639f-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="f639f-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="f639f-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="f639f-227"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="f639f-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="f639f-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="f639f-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="f639f-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="f639f-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="f639f-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="f639f-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="f639f-231"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="f639f-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-232">Серия</span><span class="sxs-lookup"><span data-stu-id="f639f-232">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="f639f-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="f639f-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-234">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="f639f-234">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="f639f-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="f639f-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-236">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="f639f-236">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="f639f-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="f639f-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-238">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="f639f-238">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="f639f-239"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="f639f-239"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="f639f-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="f639f-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="f639f-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="f639f-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="f639f-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="f639f-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="f639f-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="f639f-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="f639f-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="f639f-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-245">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="f639f-245">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="f639f-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="f639f-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="f639f-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="f639f-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="f639f-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="f639f-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="f639f-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="f639f-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-250">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="f639f-250">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="f639f-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="f639f-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="f639f-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="f639f-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="f639f-253"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="f639f-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="f639f-254"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="f639f-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="f639f-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="f639f-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="f639f-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="f639f-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="f639f-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="f639f-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="f639f-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="f639f-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="f639f-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="f639f-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="f639f-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="f639f-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="f639f-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="f639f-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="f639f-262">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="f639f-262">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="f639f-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="f639f-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="f639f-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="f639f-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="f639f-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="f639f-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="f639f-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="f639f-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="f639f-267"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="f639f-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f639f-268">**Version**</span><span class="sxs-lookup"><span data-stu-id="f639f-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f639f-269">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f639f-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f639f-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f639f-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f639f-271">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Версия**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="f639f-271">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f639f-272">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="f639f-272">Version of the operation.</span></span>

<span data-ttu-id="f639f-273">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="f639f-273">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="f639f-274"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="f639f-274"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="f639f-275"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="f639f-275"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="f639f-276">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="f639f-276">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f639f-277">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f639f-277">Remarks</span></span>

<span data-ttu-id="f639f-278">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="f639f-278">WMI does not implement this class.</span></span>

<span data-ttu-id="f639f-279">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f639f-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f639f-280">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f639f-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f639f-281">Требования</span><span class="sxs-lookup"><span data-stu-id="f639f-281">Requirements</span></span>



| <span data-ttu-id="f639f-282">Требование</span><span class="sxs-lookup"><span data-stu-id="f639f-282">Requirement</span></span> | <span data-ttu-id="f639f-283">Значение</span><span class="sxs-lookup"><span data-stu-id="f639f-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f639f-284">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f639f-284">Minimum supported client</span></span><br/> | <span data-ttu-id="f639f-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f639f-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f639f-286">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f639f-286">Minimum supported server</span></span><br/> | <span data-ttu-id="f639f-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f639f-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f639f-288">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f639f-288">Namespace</span></span><br/>                | <span data-ttu-id="f639f-289">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f639f-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f639f-290">MOF</span><span class="sxs-lookup"><span data-stu-id="f639f-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f639f-291"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f639f-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f639f-292">DLL</span><span class="sxs-lookup"><span data-stu-id="f639f-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f639f-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f639f-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f639f-294">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f639f-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f639f-295">**\_Проверка CIM**</span><span class="sxs-lookup"><span data-stu-id="f639f-295">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

