---
description: '\_Класс проверки CIM представляет условие или характеристику, которые должны быть истинными в среде, определенной или определяемой экземпляром класса системы CIM \_ .'
ms.assetid: f7862fe5-4412-4d57-b5fa-03c939ddba02
ms.tgt_platform: multiple
title: Класс CIM_Check
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check
- CIM_Check.CheckID
- CIM_Check.Caption
- CIM_Check.Description
- CIM_Check.CheckMode
- CIM_Check.Name
- CIM_Check.TargetOperatingSystem
- CIM_Check.Version
- CIM_Check.SoftwareElementID
- CIM_Check.SoftwareElementState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cbe742fb4cd2510ec4c502f89b3b3b1eb79bc47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896117"
---
# <a name="cim_check-class"></a><span data-ttu-id="a5ac5-103">\_Класс проверки CIM</span><span class="sxs-lookup"><span data-stu-id="a5ac5-103">CIM\_Check class</span></span>

<span data-ttu-id="a5ac5-104">Класс **\_ проверки CIM** представляет условие или характеристику, которые должны быть истинными в среде, определенной или определяемой экземпляром класса системы [**\_ CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="a5ac5-104">The **CIM\_Check** class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="a5ac5-105">Проверки, связанные с определенным программным элементом, организованы в одну из двух групп с помощью свойства **Phase** ассоциации [**CIM \_ софтварилементчеккс**](cim-softwareelementchecks.md) .</span><span class="sxs-lookup"><span data-stu-id="a5ac5-105">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

<span data-ttu-id="a5ac5-106">Условия, которые должны быть удовлетворены, если программный элемент находится в определенной среде, называются условиями в состоянии.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-106">Conditions that are expected to be satisfied when a software element is in a particular environment are known as in-state conditions.</span></span> <span data-ttu-id="a5ac5-107">Условия, которые должны быть удовлетворены для перехода текущего программного элемента в следующее состояние, называются условиями следующего состояния.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-107">Conditions that must be satisfied to transition the current software element to its next state are known as next-state conditions.</span></span>

<span data-ttu-id="a5ac5-108">Объект [**CIM \_ ComputerSystem**](cim-computersystem.md) представляет среду, в которой уже установлена [**модель CIM \_ софтварилемент**](cim-softwareelement.md) или в которой будет установлена **\_ софтварилемент CIM** .</span><span class="sxs-lookup"><span data-stu-id="a5ac5-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) object represents the environment in which a [**CIM\_SoftwareElement**](cim-softwareelement.md) is already installed, or in which a **CIM\_SoftwareElement** will be installed.</span></span> <span data-ttu-id="a5ac5-109">Для случая, когда программный элемент уже установлен, Ассоциация [**CIM \_ инсталледсофтварилемент**](cim-installedsoftwareelement.md) используется для указания объекта **CIM \_ ComputerSystem** , представляющего среду.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-109">For the case in which a software element is already installed, the [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association is used to identify the **CIM\_ComputerSystem** object that represents the "environment."</span></span> <span data-ttu-id="a5ac5-110">При распространении и установке программного элемента на другом компьютере объект **CIM \_ ComputerSystem** для целевой системы является средой.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-110">When a software element is being distributed and installed on a different computer, the **CIM\_ComputerSystem** object for the targeted system is the environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5ac5-111">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a5ac5-112">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a5ac5-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a5ac5-113">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a5ac5-114">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5ac5-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5ac5-115">Syntax</span></span>

``` syntax
[UUID("{7A9135CA-DB21-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Check
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
};
```

## <a name="members"></a><span data-ttu-id="a5ac5-116">Члены</span><span class="sxs-lookup"><span data-stu-id="a5ac5-116">Members</span></span>

<span data-ttu-id="a5ac5-117">Класс **\_ проверки CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a5ac5-117">The **CIM\_Check** class has these types of members:</span></span>

-   [<span data-ttu-id="a5ac5-118">Методы</span><span class="sxs-lookup"><span data-stu-id="a5ac5-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="a5ac5-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5ac5-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a5ac5-120">Методы</span><span class="sxs-lookup"><span data-stu-id="a5ac5-120">Methods</span></span>

<span data-ttu-id="a5ac5-121">Класс **\_ проверки CIM** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-121">The **CIM\_Check** class has these methods.</span></span>



| <span data-ttu-id="a5ac5-122">Метод</span><span class="sxs-lookup"><span data-stu-id="a5ac5-122">Method</span></span>                                             | <span data-ttu-id="a5ac5-123">Описание</span><span class="sxs-lookup"><span data-stu-id="a5ac5-123">Description</span></span>                                                   |
|:---------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="a5ac5-124">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-124">**Invoke**</span></span>](invoke-method-in-class-cim-check.md) | <span data-ttu-id="a5ac5-125">Выполняет определенное действие.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-125">Takes a particular action.</span></span> <span data-ttu-id="a5ac5-126">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a5ac5-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5ac5-127">Properties</span></span>

<span data-ttu-id="a5ac5-128">Класс **\_ проверки CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-128">The **CIM\_Check** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5ac5-129">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ac5-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ac5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-132">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a5ac5-133">Краткое текстовое описание субъекта.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-133">A short textual description of the subject.</span></span>

</dd> <dt>

<span data-ttu-id="a5ac5-134">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-134">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ac5-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ac5-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-137">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5ac5-138">Идентификатор, используемый в сочетании с другими ключами для уникальной идентификации проверки.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-138">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

</dd> <dt>

<span data-ttu-id="a5ac5-139">**чеккмоде**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-139">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ac5-140">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ac5-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5ac5-142">Если **значение равно true**, то условие должно существовать в среде.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-142">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="a5ac5-143">Например, предполагается, что файл находится в системе, поэтому метод [**Invoke**](invoke-method-in-class-cim-check.md) должен возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-143">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="a5ac5-144">Если **значение равно false**, условие не должно существовать.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-144">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="a5ac5-145">Например, файл не находится в системе, поэтому метод [**Invoke**](invoke-method-in-class-cim-check.md) должен возвращать **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-145">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a5ac5-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ac5-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ac5-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5ac5-149">Описание объектов.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-149">A description of the objects.</span></span>

</dd> <dt>

<span data-ttu-id="a5ac5-150">**Name**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ac5-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ac5-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-153">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5ac5-154">Имя, используемое для распознавания программного элемента.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-154">Name used to identify the software element.</span></span>

</dd> <dt>

<span data-ttu-id="a5ac5-155">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-155">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ac5-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ac5-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-158">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементид**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-158">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a5ac5-159">Это идентификатор этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-159">This is an identifier for this software element.</span></span>

</dd> <dt>

<span data-ttu-id="a5ac5-160">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-160">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ac5-161">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ac5-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-163">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементстате**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a5ac5-164">Состояние программного элемента программного элемента.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-164">The software element state of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="a5ac5-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-166">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="a5ac5-166">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="a5ac5-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-168">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="a5ac5-168">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="a5ac5-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-170">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="a5ac5-170">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="a5ac5-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-172">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-172">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a5ac5-173">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-173">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ac5-174">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ac5-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-176">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Таржетоператингсистем**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="a5ac5-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="a5ac5-177">Целевая операционная система программного элемента.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-177">Target operating system of the software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a5ac5-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a5ac5-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="a5ac5-180"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-180"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-181">MacOS</span><span class="sxs-lookup"><span data-stu-id="a5ac5-181">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="a5ac5-182"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-182"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-183">АТРИ UNIX</span><span class="sxs-lookup"><span data-stu-id="a5ac5-183">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="a5ac5-184"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="a5ac5-185"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="a5ac5-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="a5ac5-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-188">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="a5ac5-188">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="a5ac5-189"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-190">HP-UX</span><span class="sxs-lookup"><span data-stu-id="a5ac5-190">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="a5ac5-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="a5ac5-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="a5ac5-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="a5ac5-194"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-194"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="a5ac5-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-196">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="a5ac5-196">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="a5ac5-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="a5ac5-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-199">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="a5ac5-199">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="a5ac5-200"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-200"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-201">Windows 95</span><span class="sxs-lookup"><span data-stu-id="a5ac5-201">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="a5ac5-202"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-202"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-203">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a5ac5-203">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="a5ac5-204"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-204"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-205">Windows NT</span><span class="sxs-lookup"><span data-stu-id="a5ac5-205">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="a5ac5-206"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-206"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-207">Windows CE</span><span class="sxs-lookup"><span data-stu-id="a5ac5-207">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="a5ac5-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-209">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="a5ac5-209">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="a5ac5-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="a5ac5-211"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-211"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="a5ac5-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="a5ac5-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="a5ac5-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="a5ac5-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="a5ac5-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="a5ac5-217"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="a5ac5-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="a5ac5-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="a5ac5-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="a5ac5-221"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-222">Серия</span><span class="sxs-lookup"><span data-stu-id="a5ac5-222">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="a5ac5-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-224">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="a5ac5-224">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="a5ac5-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-226">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="a5ac5-226">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="a5ac5-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-228">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="a5ac5-228">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="a5ac5-229"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-229"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="a5ac5-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="a5ac5-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="a5ac5-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="a5ac5-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="a5ac5-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-235">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="a5ac5-235">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="a5ac5-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="a5ac5-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="a5ac5-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="a5ac5-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-240">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="a5ac5-240">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="a5ac5-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="a5ac5-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="a5ac5-243"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="a5ac5-244"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="a5ac5-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="a5ac5-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="a5ac5-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="a5ac5-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="a5ac5-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="a5ac5-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="a5ac5-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="a5ac5-252">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="a5ac5-252">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="a5ac5-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="a5ac5-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="a5ac5-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="a5ac5-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="a5ac5-257"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="a5ac5-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5ac5-258">**Version**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ac5-259">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5ac5-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ac5-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5ac5-261">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Версия**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="a5ac5-261">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a5ac5-262">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-262">Version of the operation.</span></span>

<span data-ttu-id="a5ac5-263">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="a5ac5-263">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="a5ac5-264"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="a5ac5-264"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="a5ac5-265"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="a5ac5-265"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5ac5-266">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5ac5-266">Remarks</span></span>

<span data-ttu-id="a5ac5-267">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-267">WMI does not implement this class.</span></span> <span data-ttu-id="a5ac5-268">Дополнительные сведения о классах, производных от **\_ проверки CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a5ac5-268">For more information about classes derived from **CIM\_Check**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a5ac5-269">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-269">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a5ac5-270">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a5ac5-270">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ac5-271">Требования</span><span class="sxs-lookup"><span data-stu-id="a5ac5-271">Requirements</span></span>



| <span data-ttu-id="a5ac5-272">Требование</span><span class="sxs-lookup"><span data-stu-id="a5ac5-272">Requirement</span></span> | <span data-ttu-id="a5ac5-273">Значение</span><span class="sxs-lookup"><span data-stu-id="a5ac5-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ac5-274">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5ac5-274">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ac5-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5ac5-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a5ac5-276">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5ac5-276">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ac5-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5ac5-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5ac5-278">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5ac5-278">Namespace</span></span><br/>                | <span data-ttu-id="a5ac5-279">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a5ac5-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a5ac5-280">MOF</span><span class="sxs-lookup"><span data-stu-id="a5ac5-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5ac5-281"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5ac5-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5ac5-282">DLL</span><span class="sxs-lookup"><span data-stu-id="a5ac5-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5ac5-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5ac5-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

