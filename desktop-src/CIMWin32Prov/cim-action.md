---
description: '\_Класс действия CIM — это операция, которая является частью процесса для создания программного элемента в следующем состоянии или для исключения программного элемента в текущем состоянии.'
ms.assetid: d1f72aaf-7e26-414f-99e7-ff8f14d66360
ms.tgt_platform: multiple
title: Класс CIM_Action
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action
- CIM_Action.ActionID
- CIM_Action.Caption
- CIM_Action.Description
- CIM_Action.Direction
- CIM_Action.Name
- CIM_Action.SoftwareElementID
- CIM_Action.SoftwareElementState
- CIM_Action.TargetOperatingSystem
- CIM_Action.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5f37fa4b62c1e8b678533de4abaa7f6a172904e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141346"
---
# <a name="cim_action-class"></a><span data-ttu-id="1fdbb-103">\_Класс действия CIM</span><span class="sxs-lookup"><span data-stu-id="1fdbb-103">CIM\_Action class</span></span>

<span data-ttu-id="1fdbb-104">Класс **\_ действия CIM** — это операция, которая является частью процесса для создания программного элемента в следующем состоянии или для исключения программного элемента в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-104">A **CIM\_Action** class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1fdbb-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1fdbb-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1fdbb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1fdbb-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1fdbb-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fdbb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fdbb-109">Syntax</span></span>

``` syntax
[UUID("{2F156260-DB21-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Action
{
  string ActionID;
  string Caption;
  string Description;
  uint16 Direction;
  string Name;
  string SoftwareElementID;
  uint16 SoftwareElementState;
  uint16 TargetOperatingSystem;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="1fdbb-110">Члены</span><span class="sxs-lookup"><span data-stu-id="1fdbb-110">Members</span></span>

<span data-ttu-id="1fdbb-111">Класс **\_ действий CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1fdbb-111">The **CIM\_Action** class has these types of members:</span></span>

-   [<span data-ttu-id="1fdbb-112">Методы</span><span class="sxs-lookup"><span data-stu-id="1fdbb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1fdbb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1fdbb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1fdbb-114">Методы</span><span class="sxs-lookup"><span data-stu-id="1fdbb-114">Methods</span></span>

<span data-ttu-id="1fdbb-115">Класс **\_ действия CIM** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-115">The **CIM\_Action** class has these methods.</span></span>



| <span data-ttu-id="1fdbb-116">Метод</span><span class="sxs-lookup"><span data-stu-id="1fdbb-116">Method</span></span>                                              | <span data-ttu-id="1fdbb-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1fdbb-117">Description</span></span>                                                   |
|:----------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="1fdbb-118">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-118">**Invoke**</span></span>](invoke-method-in-class-cim-action.md) | <span data-ttu-id="1fdbb-119">Выполняет определенное действие.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-119">Takes a particular action.</span></span> <span data-ttu-id="1fdbb-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1fdbb-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="1fdbb-121">Properties</span></span>

<span data-ttu-id="1fdbb-122">Класс **\_ действия CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-122">The **CIM\_Action** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1fdbb-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fdbb-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fdbb-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-126">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1fdbb-127">Уникальный идентификатор, назначенный конкретному действию для программного элемента.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-127">Unique identifier assigned to a particular action for a software element.</span></span>

</dd> <dt>

<span data-ttu-id="1fdbb-128">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fdbb-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fdbb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-131">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-131">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1fdbb-132">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-132">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="1fdbb-133">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fdbb-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fdbb-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fdbb-136">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-136">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="1fdbb-137">**Направление**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-137">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fdbb-138">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fdbb-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fdbb-140">Указывает, является ли конкретный объект **\_ действия CIM** частью последовательности действий, чтобы перевести текущий программный элемент в следующее состояние, например "установить", или удалить текущий программный элемент, например "Удалить".</span><span class="sxs-lookup"><span data-stu-id="1fdbb-140">Indicates whether a particular **CIM\_Action** object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="1fdbb-141">**Установка** (0)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-141">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="1fdbb-142">**Удаление** (1)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-142">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1fdbb-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fdbb-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fdbb-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-146">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1fdbb-147">Определяет программный элемент.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-147">Identifies the software element.</span></span>

</dd> <dt>

<span data-ttu-id="1fdbb-148">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-148">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fdbb-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fdbb-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-151">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементид**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-151">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1fdbb-152">Идентификатор программного элемента.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-152">Identifier for the software element.</span></span>

</dd> <dt>

<span data-ttu-id="1fdbb-153">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-153">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fdbb-154">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fdbb-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-156">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементстате**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-156">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1fdbb-157">Состояние программного элемента.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-157">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="1fdbb-158"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-158"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-159">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="1fdbb-159">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="1fdbb-160"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-160"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-161">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="1fdbb-161">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="1fdbb-162"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-162"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-163">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="1fdbb-163">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="1fdbb-164"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-164"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-165">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-165">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1fdbb-166">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-166">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fdbb-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fdbb-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-169">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Таржетоператингсистем**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="1fdbb-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="1fdbb-170">Целевая операционная система программного элемента-владельца.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-170">Target operating system of the owning software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1fdbb-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1fdbb-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="1fdbb-173"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-173"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-174">MacOS</span><span class="sxs-lookup"><span data-stu-id="1fdbb-174">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="1fdbb-175"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-175"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="1fdbb-176"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-176"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="1fdbb-177"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-177"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="1fdbb-178"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-178"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="1fdbb-179"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-179"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-180">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="1fdbb-180">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="1fdbb-181"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-181"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-182">HP-UX</span><span class="sxs-lookup"><span data-stu-id="1fdbb-182">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="1fdbb-183"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-183"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="1fdbb-184"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-184"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="1fdbb-185"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-185"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="1fdbb-186"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-186"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="1fdbb-187"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-187"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-188">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="1fdbb-188">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="1fdbb-189"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-189"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="1fdbb-190"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-190"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-191">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="1fdbb-191">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="1fdbb-192"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-192"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-193">Windows 95</span><span class="sxs-lookup"><span data-stu-id="1fdbb-193">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="1fdbb-194"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-194"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-195">Windows 98</span><span class="sxs-lookup"><span data-stu-id="1fdbb-195">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="1fdbb-196"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-196"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-197">Windows NT</span><span class="sxs-lookup"><span data-stu-id="1fdbb-197">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="1fdbb-198"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-198"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-199">Windows CE</span><span class="sxs-lookup"><span data-stu-id="1fdbb-199">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="1fdbb-200"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-200"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-201">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="1fdbb-201">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="1fdbb-202"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-202"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="1fdbb-203"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-203"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="1fdbb-204"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-204"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="1fdbb-205"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-205"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="1fdbb-206"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-206"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="1fdbb-207"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-207"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="1fdbb-208"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-208"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="1fdbb-209"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-209"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="1fdbb-210"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-210"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="1fdbb-211"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-211"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="1fdbb-212"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-212"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="1fdbb-213"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-213"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-214">Серия</span><span class="sxs-lookup"><span data-stu-id="1fdbb-214">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="1fdbb-215"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-215"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-216">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="1fdbb-216">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="1fdbb-217"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-217"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-218">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="1fdbb-218">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="1fdbb-219"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-219"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-220">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="1fdbb-220">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="1fdbb-221"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-221"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="1fdbb-222"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-222"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="1fdbb-223"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-223"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="1fdbb-224"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-224"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="1fdbb-225"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-225"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="1fdbb-226"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-226"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-227">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="1fdbb-227">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="1fdbb-228"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-228"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="1fdbb-229"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-229"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="1fdbb-230"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-230"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="1fdbb-231"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-231"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-232">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="1fdbb-232">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="1fdbb-233"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-233"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="1fdbb-234"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-234"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="1fdbb-235"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-235"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="1fdbb-236"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-236"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="1fdbb-237"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-237"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="1fdbb-238"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-238"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="1fdbb-239"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-239"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="1fdbb-240"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-240"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-241">Быть ОС</span><span class="sxs-lookup"><span data-stu-id="1fdbb-241">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="1fdbb-242"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-242"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="1fdbb-243"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-243"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="1fdbb-244"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-244"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="1fdbb-245">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="1fdbb-245">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="1fdbb-246"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-246"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="1fdbb-247"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-247"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="1fdbb-248"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-248"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="1fdbb-249"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-249"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="1fdbb-250"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="1fdbb-250"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1fdbb-251">**Version**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-251">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fdbb-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fdbb-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fdbb-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fdbb-254">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Версия**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="1fdbb-254">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="1fdbb-255">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-255">Version of the operation.</span></span>

<span data-ttu-id="1fdbb-256">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="1fdbb-256">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="1fdbb-257"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="1fdbb-257"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="1fdbb-258"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="1fdbb-258"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fdbb-259">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1fdbb-259">Remarks</span></span>

<span data-ttu-id="1fdbb-260">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-260">WMI does not implement this class.</span></span> <span data-ttu-id="1fdbb-261">См. раздел [Классы Win32](win32-provider.md) для классов, производных от **\_ действия CIM**.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-261">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_Action**.</span></span>

<span data-ttu-id="1fdbb-262">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1fdbb-263">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="1fdbb-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fdbb-264">Требования</span><span class="sxs-lookup"><span data-stu-id="1fdbb-264">Requirements</span></span>



| <span data-ttu-id="1fdbb-265">Требование</span><span class="sxs-lookup"><span data-stu-id="1fdbb-265">Requirement</span></span> | <span data-ttu-id="1fdbb-266">Значение</span><span class="sxs-lookup"><span data-stu-id="1fdbb-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fdbb-267">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fdbb-267">Minimum supported client</span></span><br/> | <span data-ttu-id="1fdbb-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fdbb-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1fdbb-269">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fdbb-269">Minimum supported server</span></span><br/> | <span data-ttu-id="1fdbb-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fdbb-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1fdbb-271">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1fdbb-271">Namespace</span></span><br/>                | <span data-ttu-id="1fdbb-272">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1fdbb-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1fdbb-273">MOF</span><span class="sxs-lookup"><span data-stu-id="1fdbb-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fdbb-274"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fdbb-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fdbb-275">DLL</span><span class="sxs-lookup"><span data-stu-id="1fdbb-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fdbb-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fdbb-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fdbb-277">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fdbb-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fdbb-278">Классы CIM</span><span class="sxs-lookup"><span data-stu-id="1fdbb-278">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

