---
description: Класс CIM \_ свапспацечекк определяет объем пространства подкачки, который должен быть доступен в системе.
ms.assetid: c5e5ec68-bc62-4bdf-93b7-ce868e738dee
ms.tgt_platform: multiple
title: Класс CIM_SwapSpaceCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwapSpaceCheck
- CIM_SwapSpaceCheck.CheckID
- CIM_SwapSpaceCheck.Caption
- CIM_SwapSpaceCheck.Description
- CIM_SwapSpaceCheck.CheckMode
- CIM_SwapSpaceCheck.Name
- CIM_SwapSpaceCheck.TargetOperatingSystem
- CIM_SwapSpaceCheck.Version
- CIM_SwapSpaceCheck.SoftwareElementID
- CIM_SwapSpaceCheck.SoftwareElementState
- CIM_SwapSpaceCheck.SwapSpaceSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 992d8a314797c7a977e9a672ecb9d3dcdb561292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539011"
---
# <a name="cim_swapspacecheck-class"></a><span data-ttu-id="1f9d3-103">\_Класс CIM свапспацечекк</span><span class="sxs-lookup"><span data-stu-id="1f9d3-103">CIM\_SwapSpaceCheck class</span></span>

<span data-ttu-id="1f9d3-104">Класс **CIM \_ свапспацечекк** определяет объем пространства подкачки, который должен быть доступен в системе.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-104">The **CIM\_SwapSpaceCheck** class specifies the amount of swap space that must be available on the system.</span></span> <span data-ttu-id="1f9d3-105">Значение указывается в свойстве **свапспацесизе** .</span><span class="sxs-lookup"><span data-stu-id="1f9d3-105">The amount is specified in the **SwapSpaceSize** property.</span></span> <span data-ttu-id="1f9d3-106">Сведения об этой проверке сравниваются с соответствующими сведениями в объекте среды [**CIM \_**](cim-operatingsystem.md) , на который ссылается Ассоциация [**\_ инсталледос CIM**](cim-installedos.md) для объекта [**CIM \_ ComputerSystem**](cim-computersystem.md) , описывающего среду.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-106">Details of this check are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by the [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="1f9d3-107">Если значение свойства **тоталсвапспацесизе** больше или равно значению, указанному в свойстве **свапспацесизе** , условие выполнено.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-107">When the value of the **TotalSwapSpaceSize** property is greater than or equal to the value specified in the **SwapSpaceSize** property, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f9d3-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1f9d3-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1f9d3-110">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1f9d3-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f9d3-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f9d3-112">Syntax</span></span>

``` syntax
[UUID("{A5AE701E-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SwapSpaceCheck : CIM_Check
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
  uint64  SwapSpaceSize;
};
```

## <a name="members"></a><span data-ttu-id="1f9d3-113">Члены</span><span class="sxs-lookup"><span data-stu-id="1f9d3-113">Members</span></span>

<span data-ttu-id="1f9d3-114">Класс **CIM \_ свапспацечекк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1f9d3-114">The **CIM\_SwapSpaceCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="1f9d3-115">Методы</span><span class="sxs-lookup"><span data-stu-id="1f9d3-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="1f9d3-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f9d3-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1f9d3-117">Методы</span><span class="sxs-lookup"><span data-stu-id="1f9d3-117">Methods</span></span>

<span data-ttu-id="1f9d3-118">Класс **CIM \_ свапспацечекк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-118">The **CIM\_SwapSpaceCheck** class has these methods.</span></span>



| <span data-ttu-id="1f9d3-119">Метод</span><span class="sxs-lookup"><span data-stu-id="1f9d3-119">Method</span></span>                                                      | <span data-ttu-id="1f9d3-120">Описание</span><span class="sxs-lookup"><span data-stu-id="1f9d3-120">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="1f9d3-121">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-121">**Invoke**</span></span>](invoke-method-in-class-cim-swapspacecheck.md) | <span data-ttu-id="1f9d3-122">Выполняет определенное действие.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-122">Takes a particular action.</span></span> <span data-ttu-id="1f9d3-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1f9d3-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f9d3-124">Properties</span></span>

<span data-ttu-id="1f9d3-125">Класс **CIM \_ свапспацечекк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-125">The **CIM\_SwapSpaceCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f9d3-126">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f9d3-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f9d3-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-129">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1f9d3-130">Краткое текстовое описание субъекта.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-130">A short textual description of the subject.</span></span>

<span data-ttu-id="1f9d3-131">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f9d3-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f9d3-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f9d3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-135">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1f9d3-136">Идентификатор, используемый в сочетании с другими ключами для уникальной идентификации проверки.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="1f9d3-137">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f9d3-138">**чеккмоде**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f9d3-139">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f9d3-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f9d3-141">Если **значение равно true**, то условие должно существовать в среде.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="1f9d3-142">Например, предполагается, что файл находится в системе, поэтому метод [**Invoke**](invoke-method-in-class-cim-check.md) должен возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="1f9d3-143">Если **значение равно false**, условие не должно существовать.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="1f9d3-144">Например, файл не находится в системе, поэтому метод [**Invoke**](invoke-method-in-class-cim-check.md) должен возвращать **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="1f9d3-145">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f9d3-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f9d3-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f9d3-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f9d3-149">Описание объектов.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-149">A description of the objects.</span></span>

<span data-ttu-id="1f9d3-150">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f9d3-151">**Name**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f9d3-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f9d3-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-154">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1f9d3-155">Имя, используемое для распознавания программного элемента</span><span class="sxs-lookup"><span data-stu-id="1f9d3-155">Name used to identify the software element</span></span>

<span data-ttu-id="1f9d3-156">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-156">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f9d3-157">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-157">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f9d3-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f9d3-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-160">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементид**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1f9d3-161">Это идентификатор этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-161">This is an identifier for this software element.</span></span>

<span data-ttu-id="1f9d3-162">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-162">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f9d3-163">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-163">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f9d3-164">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f9d3-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-166">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементстате**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f9d3-167">Состояние программного элемента программного элемента.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-167">The software element state of a software element.</span></span>

<span data-ttu-id="1f9d3-168">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-168">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="1f9d3-169"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-169"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-170">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-170">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="1f9d3-171"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-171"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-172">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-172">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="1f9d3-173"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-173"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-174">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-174">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="1f9d3-175"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-175"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-176">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-176">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f9d3-177">**свапспацесизе**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-177">**SwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f9d3-178">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f9d3-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-180">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**система \_ CIM**](cim-operatingsystem.md)".**Тоталсвапспацесизе**"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="1f9d3-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**TotalSwapSpaceSize**"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1f9d3-181">Минимальный размер пространства подкачки (в килобайтах), который должен быть доступен в целевой системе.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-181">Minimum swap-space size, in kilobytes, that must be available on the target system.</span></span>

<span data-ttu-id="1f9d3-182">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1f9d3-183">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f9d3-184">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f9d3-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-186">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Таржетоператингсистем**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="1f9d3-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="1f9d3-187">Целевая операционная система программного элемента.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-187">Target operating system of the software element.</span></span>

<span data-ttu-id="1f9d3-188">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-188">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1f9d3-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1f9d3-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="1f9d3-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-192">MacOS</span><span class="sxs-lookup"><span data-stu-id="1f9d3-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="1f9d3-193"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-194">АТРИ UNIX</span><span class="sxs-lookup"><span data-stu-id="1f9d3-194">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="1f9d3-195"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="1f9d3-196"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="1f9d3-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="1f9d3-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-199">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="1f9d3-199">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="1f9d3-200"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-201">HP-UX</span><span class="sxs-lookup"><span data-stu-id="1f9d3-201">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="1f9d3-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="1f9d3-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="1f9d3-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="1f9d3-205"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="1f9d3-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-207">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="1f9d3-207">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="1f9d3-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="1f9d3-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-210">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="1f9d3-210">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="1f9d3-211"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-212">Windows 95</span><span class="sxs-lookup"><span data-stu-id="1f9d3-212">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="1f9d3-213"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-214">Windows 98</span><span class="sxs-lookup"><span data-stu-id="1f9d3-214">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="1f9d3-215"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-216">Windows NT</span><span class="sxs-lookup"><span data-stu-id="1f9d3-216">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="1f9d3-217"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-218">Windows CE</span><span class="sxs-lookup"><span data-stu-id="1f9d3-218">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="1f9d3-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-220">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="1f9d3-220">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="1f9d3-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="1f9d3-222"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="1f9d3-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="1f9d3-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="1f9d3-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="1f9d3-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="1f9d3-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="1f9d3-228"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="1f9d3-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="1f9d3-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="1f9d3-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="1f9d3-232"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-233">Серия</span><span class="sxs-lookup"><span data-stu-id="1f9d3-233">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="1f9d3-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-235">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="1f9d3-235">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="1f9d3-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-237">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="1f9d3-237">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="1f9d3-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-239">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="1f9d3-239">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="1f9d3-240"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="1f9d3-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="1f9d3-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="1f9d3-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="1f9d3-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="1f9d3-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-246">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="1f9d3-246">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="1f9d3-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="1f9d3-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="1f9d3-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="1f9d3-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-251">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="1f9d3-251">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="1f9d3-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="1f9d3-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="1f9d3-254"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="1f9d3-255"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="1f9d3-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="1f9d3-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="1f9d3-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="1f9d3-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="1f9d3-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="1f9d3-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="1f9d3-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="1f9d3-263">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="1f9d3-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="1f9d3-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="1f9d3-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="1f9d3-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="1f9d3-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="1f9d3-268"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="1f9d3-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1f9d3-269">**Version**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f9d3-270">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f9d3-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f9d3-272">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Версия**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="1f9d3-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="1f9d3-273">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-273">Version of the operation.</span></span>

<span data-ttu-id="1f9d3-274">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="1f9d3-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="1f9d3-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="1f9d3-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="1f9d3-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="1f9d3-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="1f9d3-277">Это свойство наследуется [**от \_ проверки CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d3-277">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f9d3-278">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f9d3-278">Remarks</span></span>

<span data-ttu-id="1f9d3-279">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-279">WMI does not implement this class.</span></span>

<span data-ttu-id="1f9d3-280">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-280">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1f9d3-281">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="1f9d3-281">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f9d3-282">Требования</span><span class="sxs-lookup"><span data-stu-id="1f9d3-282">Requirements</span></span>



| <span data-ttu-id="1f9d3-283">Требование</span><span class="sxs-lookup"><span data-stu-id="1f9d3-283">Requirement</span></span> | <span data-ttu-id="1f9d3-284">Значение</span><span class="sxs-lookup"><span data-stu-id="1f9d3-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9d3-285">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f9d3-285">Minimum supported client</span></span><br/> | <span data-ttu-id="1f9d3-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f9d3-286">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f9d3-287">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f9d3-287">Minimum supported server</span></span><br/> | <span data-ttu-id="1f9d3-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f9d3-288">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f9d3-289">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1f9d3-289">Namespace</span></span><br/>                | <span data-ttu-id="1f9d3-290">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1f9d3-290">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1f9d3-291">MOF</span><span class="sxs-lookup"><span data-stu-id="1f9d3-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f9d3-292"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f9d3-292"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f9d3-293">DLL</span><span class="sxs-lookup"><span data-stu-id="1f9d3-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f9d3-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f9d3-294"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9d3-295">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f9d3-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9d3-296">**\_Проверка CIM**</span><span class="sxs-lookup"><span data-stu-id="1f9d3-296">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

