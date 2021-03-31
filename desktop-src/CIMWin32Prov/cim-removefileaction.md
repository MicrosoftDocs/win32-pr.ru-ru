---
description: Класс CIM \_ ремовефилеактион удаляет файлы.
ms.assetid: 32d5e537-eee2-4f93-9b1f-ecee0d36c99a
ms.tgt_platform: multiple
title: Класс CIM_RemoveFileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveFileAction
- CIM_RemoveFileAction.ActionID
- CIM_RemoveFileAction.Caption
- CIM_RemoveFileAction.Description
- CIM_RemoveFileAction.Direction
- CIM_RemoveFileAction.Name
- CIM_RemoveFileAction.SoftwareElementID
- CIM_RemoveFileAction.SoftwareElementState
- CIM_RemoveFileAction.TargetOperatingSystem
- CIM_RemoveFileAction.Version
- CIM_RemoveFileAction.File
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c9454f39e5389d61ea23c89e5e1aada7dc860ac9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895509"
---
# <a name="cim_removefileaction-class"></a><span data-ttu-id="70ed4-103">\_Класс CIM ремовефилеактион</span><span class="sxs-lookup"><span data-stu-id="70ed4-103">CIM\_RemoveFileAction class</span></span>

<span data-ttu-id="70ed4-104">Класс **CIM \_ ремовефилеактион** удаляет файлы.</span><span class="sxs-lookup"><span data-stu-id="70ed4-104">The **CIM\_RemoveFileAction** class uninstalls files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="70ed4-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="70ed4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="70ed4-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="70ed4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="70ed4-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="70ed4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="70ed4-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="70ed4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ed4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70ed4-109">Syntax</span></span>

``` syntax
[UUID("{C75D89F8-DB30-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_RemoveFileAction : CIM_FileAction
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
  string File;
};
```

## <a name="members"></a><span data-ttu-id="70ed4-110">Члены</span><span class="sxs-lookup"><span data-stu-id="70ed4-110">Members</span></span>

<span data-ttu-id="70ed4-111">Класс **CIM \_ ремовефилеактион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="70ed4-111">The **CIM\_RemoveFileAction** class has these types of members:</span></span>

-   [<span data-ttu-id="70ed4-112">Методы</span><span class="sxs-lookup"><span data-stu-id="70ed4-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="70ed4-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="70ed4-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="70ed4-114">Методы</span><span class="sxs-lookup"><span data-stu-id="70ed4-114">Methods</span></span>

<span data-ttu-id="70ed4-115">Класс **CIM \_ ремовефилеактион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="70ed4-115">The **CIM\_RemoveFileAction** class has these methods.</span></span>



| <span data-ttu-id="70ed4-116">Метод</span><span class="sxs-lookup"><span data-stu-id="70ed4-116">Method</span></span>                                                        | <span data-ttu-id="70ed4-117">Описание</span><span class="sxs-lookup"><span data-stu-id="70ed4-117">Description</span></span>                                                   |
|:--------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="70ed4-118">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="70ed4-118">**Invoke**</span></span>](invoke-method-in-class-cim-removefileaction.md) | <span data-ttu-id="70ed4-119">Выполняет определенное действие.</span><span class="sxs-lookup"><span data-stu-id="70ed4-119">Takes a particular action.</span></span> <span data-ttu-id="70ed4-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="70ed4-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="70ed4-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="70ed4-121">Properties</span></span>

<span data-ttu-id="70ed4-122">Класс **CIM \_ ремовефилеактион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="70ed4-122">The **CIM\_RemoveFileAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70ed4-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="70ed4-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ed4-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="70ed4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70ed4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-126">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="70ed4-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="70ed4-127">Уникальный идентификатор, назначенный конкретному действию для программного элемента.</span><span class="sxs-lookup"><span data-stu-id="70ed4-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="70ed4-128">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="70ed4-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="70ed4-129">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="70ed4-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ed4-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="70ed4-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70ed4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-132">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="70ed4-132">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="70ed4-133">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="70ed4-133">Short textual description of the object.</span></span>

<span data-ttu-id="70ed4-134">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="70ed4-134">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="70ed4-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="70ed4-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ed4-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="70ed4-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70ed4-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70ed4-138">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="70ed4-138">Description of the object.</span></span>

<span data-ttu-id="70ed4-139">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="70ed4-139">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="70ed4-140">**Направление**</span><span class="sxs-lookup"><span data-stu-id="70ed4-140">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ed4-141">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70ed4-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70ed4-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70ed4-143">Указывает, является ли конкретный объект [**\_ действия CIM**](cim-action.md) частью последовательности действий, чтобы перевести текущий программный элемент в следующее состояние, например "установить", или удалить текущий программный элемент, например "Удалить".</span><span class="sxs-lookup"><span data-stu-id="70ed4-143">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="70ed4-144">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="70ed4-144">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="70ed4-145">**Установка** (0)</span><span class="sxs-lookup"><span data-stu-id="70ed4-145">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="70ed4-146">**Удаление** (1)</span><span class="sxs-lookup"><span data-stu-id="70ed4-146">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="70ed4-147">**Файл**</span><span class="sxs-lookup"><span data-stu-id="70ed4-147">**File**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ed4-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="70ed4-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70ed4-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-150">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="70ed4-150">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="70ed4-151">Имя удаляемого файла.</span><span class="sxs-lookup"><span data-stu-id="70ed4-151">Name of the file to remove.</span></span>

</dd> <dt>

<span data-ttu-id="70ed4-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="70ed4-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ed4-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="70ed4-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70ed4-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-155">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="70ed4-155">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="70ed4-156">Определяет программный элемент.</span><span class="sxs-lookup"><span data-stu-id="70ed4-156">Identifies the software element.</span></span>

<span data-ttu-id="70ed4-157">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="70ed4-157">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="70ed4-158">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="70ed4-158">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ed4-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="70ed4-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70ed4-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-161">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементид**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="70ed4-161">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="70ed4-162">Идентификатор программного элемента.</span><span class="sxs-lookup"><span data-stu-id="70ed4-162">Identifier for the software element.</span></span>

<span data-ttu-id="70ed4-163">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="70ed4-163">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="70ed4-164">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="70ed4-164">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ed4-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70ed4-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70ed4-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-167">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементстате**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="70ed4-167">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="70ed4-168">Состояние программного элемента.</span><span class="sxs-lookup"><span data-stu-id="70ed4-168">State of a software element.</span></span>

<span data-ttu-id="70ed4-169">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="70ed4-169">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="70ed4-170"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="70ed4-170"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-171">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="70ed4-171">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="70ed4-172"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="70ed4-172"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-173">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="70ed4-173">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="70ed4-174"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="70ed4-174"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-175">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="70ed4-175">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="70ed4-176"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="70ed4-176"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-177">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="70ed4-177">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="70ed4-178">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="70ed4-178">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ed4-179">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70ed4-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70ed4-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-181">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Таржетоператингсистем**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="70ed4-181">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="70ed4-182">Целевая операционная система программного элемента-владельца.</span><span class="sxs-lookup"><span data-stu-id="70ed4-182">Target operating system of the owning software element.</span></span>

<span data-ttu-id="70ed4-183">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="70ed4-183">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="70ed4-184"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="70ed4-184"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="70ed4-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="70ed4-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="70ed4-186"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="70ed4-186"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-187">MacOS</span><span class="sxs-lookup"><span data-stu-id="70ed4-187">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="70ed4-188"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="70ed4-188"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="70ed4-189"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="70ed4-189"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="70ed4-190"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="70ed4-190"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="70ed4-191"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="70ed4-191"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="70ed4-192"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="70ed4-192"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-193">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="70ed4-193">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="70ed4-194"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="70ed4-194"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-195">HP-UX</span><span class="sxs-lookup"><span data-stu-id="70ed4-195">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="70ed4-196"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="70ed4-196"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="70ed4-197"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="70ed4-197"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="70ed4-198"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="70ed4-198"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="70ed4-199"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="70ed4-199"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="70ed4-200"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="70ed4-200"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-201">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="70ed4-201">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="70ed4-202"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="70ed4-202"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="70ed4-203"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="70ed4-203"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-204">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="70ed4-204">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="70ed4-205"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="70ed4-205"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-206">Windows 95</span><span class="sxs-lookup"><span data-stu-id="70ed4-206">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="70ed4-207"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="70ed4-207"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-208">Windows 98</span><span class="sxs-lookup"><span data-stu-id="70ed4-208">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="70ed4-209"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="70ed4-209"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-210">Windows NT</span><span class="sxs-lookup"><span data-stu-id="70ed4-210">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="70ed4-211"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="70ed4-211"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-212">Windows CE</span><span class="sxs-lookup"><span data-stu-id="70ed4-212">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="70ed4-213"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="70ed4-213"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-214">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="70ed4-214">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="70ed4-215"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="70ed4-215"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="70ed4-216"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="70ed4-216"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="70ed4-217"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="70ed4-217"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="70ed4-218"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="70ed4-218"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="70ed4-219"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="70ed4-219"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="70ed4-220"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="70ed4-220"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="70ed4-221"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="70ed4-221"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="70ed4-222"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="70ed4-222"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="70ed4-223"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="70ed4-223"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="70ed4-224"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="70ed4-224"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="70ed4-225"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="70ed4-225"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="70ed4-226"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="70ed4-226"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-227">Серия</span><span class="sxs-lookup"><span data-stu-id="70ed4-227">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="70ed4-228"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="70ed4-228"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-229">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="70ed4-229">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="70ed4-230"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="70ed4-230"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-231">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="70ed4-231">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="70ed4-232"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="70ed4-232"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-233">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="70ed4-233">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="70ed4-234"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="70ed4-234"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="70ed4-235"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="70ed4-235"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="70ed4-236"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="70ed4-236"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="70ed4-237"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="70ed4-237"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="70ed4-238"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="70ed4-238"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="70ed4-239"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="70ed4-239"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-240">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="70ed4-240">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="70ed4-241"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="70ed4-241"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="70ed4-242"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="70ed4-242"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="70ed4-243"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="70ed4-243"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="70ed4-244"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="70ed4-244"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-245">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="70ed4-245">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="70ed4-246"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="70ed4-246"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="70ed4-247"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="70ed4-247"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="70ed4-248"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="70ed4-248"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="70ed4-249"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="70ed4-249"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="70ed4-250"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="70ed4-250"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="70ed4-251"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="70ed4-251"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="70ed4-252"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="70ed4-252"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="70ed4-253"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="70ed4-253"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-254">Быть ОС</span><span class="sxs-lookup"><span data-stu-id="70ed4-254">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="70ed4-255"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="70ed4-255"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="70ed4-256"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="70ed4-256"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="70ed4-257"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="70ed4-257"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="70ed4-258">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="70ed4-258">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="70ed4-259"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="70ed4-259"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="70ed4-260"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="70ed4-260"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="70ed4-261"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="70ed4-261"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="70ed4-262"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="70ed4-262"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="70ed4-263"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="70ed4-263"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="70ed4-264">**Version**</span><span class="sxs-lookup"><span data-stu-id="70ed4-264">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ed4-265">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="70ed4-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70ed4-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ed4-267">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Версия**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="70ed4-267">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="70ed4-268">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="70ed4-268">Version of the operation.</span></span>

<span data-ttu-id="70ed4-269">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="70ed4-269">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="70ed4-270"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="70ed4-270"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="70ed4-271"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="70ed4-271"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="70ed4-272">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="70ed4-272">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70ed4-273">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70ed4-273">Remarks</span></span>

<span data-ttu-id="70ed4-274">Класс **CIM \_ ремовефилеактион** является производным от [**CIM \_ филеактион**](cim-fileaction.md).</span><span class="sxs-lookup"><span data-stu-id="70ed4-274">The **CIM\_RemoveFileAction** class is derived from [**CIM\_FileAction**](cim-fileaction.md).</span></span>

<span data-ttu-id="70ed4-275">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="70ed4-275">WMI does not implement this class.</span></span>

<span data-ttu-id="70ed4-276">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="70ed4-276">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="70ed4-277">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="70ed4-277">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="70ed4-278">Требования</span><span class="sxs-lookup"><span data-stu-id="70ed4-278">Requirements</span></span>



| <span data-ttu-id="70ed4-279">Требование</span><span class="sxs-lookup"><span data-stu-id="70ed4-279">Requirement</span></span> | <span data-ttu-id="70ed4-280">Значение</span><span class="sxs-lookup"><span data-stu-id="70ed4-280">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70ed4-281">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70ed4-281">Minimum supported client</span></span><br/> | <span data-ttu-id="70ed4-282">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70ed4-282">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="70ed4-283">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70ed4-283">Minimum supported server</span></span><br/> | <span data-ttu-id="70ed4-284">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70ed4-284">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="70ed4-285">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="70ed4-285">Namespace</span></span><br/>                | <span data-ttu-id="70ed4-286">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="70ed4-286">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="70ed4-287">MOF</span><span class="sxs-lookup"><span data-stu-id="70ed4-287">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70ed4-288"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70ed4-288"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="70ed4-289">DLL</span><span class="sxs-lookup"><span data-stu-id="70ed4-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70ed4-290"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70ed4-290"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70ed4-291">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70ed4-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ed4-292">**\_ФИЛЕАКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="70ed4-292">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> </dl>

 

