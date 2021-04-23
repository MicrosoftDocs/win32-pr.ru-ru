---
description: Класс CIM \_ модифисеттингактион представляет сведения для изменения определенного файла параметров для конкретной записи с указанным значением.
ms.assetid: 6d22bc11-f798-4634-8688-797d4a4a4bee
ms.tgt_platform: multiple
title: Класс CIM_ModifySettingAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ModifySettingAction
- CIM_ModifySettingAction.ActionID
- CIM_ModifySettingAction.Caption
- CIM_ModifySettingAction.Description
- CIM_ModifySettingAction.Direction
- CIM_ModifySettingAction.Name
- CIM_ModifySettingAction.SoftwareElementID
- CIM_ModifySettingAction.SoftwareElementState
- CIM_ModifySettingAction.TargetOperatingSystem
- CIM_ModifySettingAction.Version
- CIM_ModifySettingAction.ActionType
- CIM_ModifySettingAction.EntryName
- CIM_ModifySettingAction.EntryValue
- CIM_ModifySettingAction.FileName
- CIM_ModifySettingAction.SectionKey
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 450e73eaa6f405e47d79cbf3840932e0f106a4b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807667"
---
# <a name="cim_modifysettingaction-class"></a><span data-ttu-id="7bbe5-103">\_Класс CIM модифисеттингактион</span><span class="sxs-lookup"><span data-stu-id="7bbe5-103">CIM\_ModifySettingAction class</span></span>

<span data-ttu-id="7bbe5-104">Класс **CIM \_ модифисеттингактион** представляет сведения для изменения определенного файла параметров для конкретной записи с указанным значением.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-104">The **CIM\_ModifySettingAction** class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bbe5-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7bbe5-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7bbe5-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7bbe5-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbe5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bbe5-109">Syntax</span></span>

``` syntax
[UUID("{ECDE0B90-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ModifySettingAction : CIM_Action
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
  uint16 ActionType;
  string EntryName;
  string EntryValue;
  string FileName;
  string SectionKey;
};
```

## <a name="members"></a><span data-ttu-id="7bbe5-110">Члены</span><span class="sxs-lookup"><span data-stu-id="7bbe5-110">Members</span></span>

<span data-ttu-id="7bbe5-111">Класс **CIM \_ модифисеттингактион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7bbe5-111">The **CIM\_ModifySettingAction** class has these types of members:</span></span>

-   [<span data-ttu-id="7bbe5-112">Методы</span><span class="sxs-lookup"><span data-stu-id="7bbe5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7bbe5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="7bbe5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7bbe5-114">Методы</span><span class="sxs-lookup"><span data-stu-id="7bbe5-114">Methods</span></span>

<span data-ttu-id="7bbe5-115">Класс **CIM \_ модифисеттингактион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-115">The **CIM\_ModifySettingAction** class has these methods.</span></span>



| <span data-ttu-id="7bbe5-116">Метод</span><span class="sxs-lookup"><span data-stu-id="7bbe5-116">Method</span></span>                                                           | <span data-ttu-id="7bbe5-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7bbe5-117">Description</span></span>                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="7bbe5-118">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-118">**Invoke**</span></span>](invoke-method-in-class-cim-modifysettingaction.md) | <span data-ttu-id="7bbe5-119">Выполняет определенное действие.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-119">Takes a specific action.</span></span> <span data-ttu-id="7bbe5-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7bbe5-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="7bbe5-121">Properties</span></span>

<span data-ttu-id="7bbe5-122">Класс **CIM \_ модифисеттингактион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-122">The **CIM\_ModifySettingAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bbe5-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-126">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-127">Уникальный идентификатор, назначенный конкретному действию для программного элемента.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="7bbe5-128">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bbe5-129">**Тип действия**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-129">**ActionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-132">Тип действия, выполняемого с указанной записью параметра.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-132">Type of action to perform on the specified setting entry.</span></span> <span data-ttu-id="7bbe5-133">Для дополнений предполагается, что регистр учитывается. Однако предполагается, что удаления не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-133">Additions are assumed to be case sensitive; however, removals are assumed to be case insensitive.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="7bbe5-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**CREATE** (0)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Create** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-135">Создает указанную запись.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-135">Creates the specified entry.</span></span>

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="7bbe5-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Удалить** (1)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-137">Удаляет указанную запись.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-137">Deletes the specified entry.</span></span>

</dd> <dt>

<span id="Append"></span><span id="append"></span><span id="APPEND"></span>

<span data-ttu-id="7bbe5-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Append** (2)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Append** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-139">Добавляет к концу указанной записи.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-139">Appends to the end of the specified entry.</span></span>

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>

<span data-ttu-id="7bbe5-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Удалить** (3)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Remove** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-141">Удаляет значение из указанной записи.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-141">Removes the value from the specified entry.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7bbe5-142">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-145">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-145">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-146">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-146">Short textual description of the object.</span></span>

<span data-ttu-id="7bbe5-147">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-147">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bbe5-148">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-151">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-151">Description of the object.</span></span>

<span data-ttu-id="7bbe5-152">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-152">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bbe5-153">**Направление**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-153">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-154">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-156">Указывает, является ли конкретный объект [**\_ действия CIM**](cim-action.md) частью последовательности действий, чтобы перевести текущий программный элемент в следующее состояние, например "установить", или удалить текущий программный элемент, например "Удалить".</span><span class="sxs-lookup"><span data-stu-id="7bbe5-156">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="7bbe5-157">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-157">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="7bbe5-158">**Установка** (0)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-158">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="7bbe5-159">**Удаление** (1)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-159">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7bbe5-160">**ИмяЗаписи**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-160">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-163">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-163">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-164">Имя изменяемой записи.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-164">Name of the entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="7bbe5-165">**ентривалуе**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-165">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-168">Значение для добавления, добавления или замены указанного параметра.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-168">Value to add, append, or to replace the specified setting.</span></span>

</dd> <dt>

<span data-ttu-id="7bbe5-169">**FileName**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-169">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-172">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-173">Имя файла изменяемой записи файла параметров.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-173">File name of the setting file entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="7bbe5-174">**Name**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-177">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-178">Определяет программный элемент.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-178">Identifies the software element.</span></span>

<span data-ttu-id="7bbe5-179">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-179">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bbe5-180">**сектионкэй**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-180">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-183">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-183">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-184">Ключ раздела изменяемой записи параметра.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-184">Section key of the setting entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="7bbe5-185">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-185">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-188">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементид**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-189">Идентификатор программного элемента.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-189">Identifier for the software element.</span></span>

<span data-ttu-id="7bbe5-190">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-190">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bbe5-191">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-191">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-192">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-194">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Софтварилементстате**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-194">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-195">Состояние программного элемента.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-195">State of a software element.</span></span>

<span data-ttu-id="7bbe5-196">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-196">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="7bbe5-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-198">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-198">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="7bbe5-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-200">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-200">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="7bbe5-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-202">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-202">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="7bbe5-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-204">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-204">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7bbe5-205">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-205">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-206">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-208">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Таржетоператингсистем**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="7bbe5-208">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-209">Целевая операционная система программного элемента-владельца.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-209">Target operating system of the owning software element.</span></span>

<span data-ttu-id="7bbe5-210">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-210">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7bbe5-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7bbe5-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="7bbe5-213"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-213"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-214">MacOS</span><span class="sxs-lookup"><span data-stu-id="7bbe5-214">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="7bbe5-215"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="7bbe5-216"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="7bbe5-217"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="7bbe5-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="7bbe5-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-220">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="7bbe5-220">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="7bbe5-221"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-222">HP-UX</span><span class="sxs-lookup"><span data-stu-id="7bbe5-222">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="7bbe5-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="7bbe5-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="7bbe5-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="7bbe5-226"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-226"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="7bbe5-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-228">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="7bbe5-228">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="7bbe5-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="7bbe5-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-231">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="7bbe5-231">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="7bbe5-232"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-232"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-233">Windows 95</span><span class="sxs-lookup"><span data-stu-id="7bbe5-233">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="7bbe5-234"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-234"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-235">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7bbe5-235">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="7bbe5-236"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-236"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-237">Windows NT</span><span class="sxs-lookup"><span data-stu-id="7bbe5-237">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="7bbe5-238"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-238"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-239">Windows CE</span><span class="sxs-lookup"><span data-stu-id="7bbe5-239">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="7bbe5-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-241">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="7bbe5-241">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="7bbe5-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="7bbe5-243"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="7bbe5-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="7bbe5-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="7bbe5-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="7bbe5-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="7bbe5-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="7bbe5-249"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="7bbe5-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="7bbe5-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="7bbe5-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="7bbe5-253"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-254">Серия</span><span class="sxs-lookup"><span data-stu-id="7bbe5-254">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="7bbe5-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-256">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="7bbe5-256">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="7bbe5-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-258">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="7bbe5-258">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="7bbe5-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-260">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="7bbe5-260">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="7bbe5-261"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-261"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="7bbe5-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="7bbe5-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="7bbe5-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="7bbe5-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="7bbe5-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-267">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="7bbe5-267">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="7bbe5-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="7bbe5-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="7bbe5-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="7bbe5-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-272">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="7bbe5-272">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="7bbe5-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="7bbe5-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="7bbe5-275"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="7bbe5-276"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="7bbe5-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="7bbe5-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="7bbe5-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="7bbe5-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-281">Быть ОС</span><span class="sxs-lookup"><span data-stu-id="7bbe5-281">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="7bbe5-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="7bbe5-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="7bbe5-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="7bbe5-285">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="7bbe5-285">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="7bbe5-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="7bbe5-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="7bbe5-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="7bbe5-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="7bbe5-290"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="7bbe5-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7bbe5-291">**Version**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-291">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbe5-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bbe5-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbe5-294">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ софтварилемент**](cim-softwareelement.md).**Версия**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="7bbe5-294">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="7bbe5-295">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-295">Version of the operation.</span></span>

<span data-ttu-id="7bbe5-296">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="7bbe5-296">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="7bbe5-297"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="7bbe5-297"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="7bbe5-298"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="7bbe5-298"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="7bbe5-299">Это свойство наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-299">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bbe5-300">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7bbe5-300">Remarks</span></span>

<span data-ttu-id="7bbe5-301">Класс **CIM \_ модифисеттингактион** является производным от [**\_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7bbe5-301">The **CIM\_ModifySettingAction** class is derived from [**CIM\_Action**](cim-action.md).</span></span>

<span data-ttu-id="7bbe5-302">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-302">WMI does not implement this class.</span></span>

<span data-ttu-id="7bbe5-303">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-303">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7bbe5-304">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7bbe5-304">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bbe5-305">Требования</span><span class="sxs-lookup"><span data-stu-id="7bbe5-305">Requirements</span></span>



| <span data-ttu-id="7bbe5-306">Требование</span><span class="sxs-lookup"><span data-stu-id="7bbe5-306">Requirement</span></span> | <span data-ttu-id="7bbe5-307">Значение</span><span class="sxs-lookup"><span data-stu-id="7bbe5-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbe5-308">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7bbe5-308">Minimum supported client</span></span><br/> | <span data-ttu-id="7bbe5-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bbe5-309">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7bbe5-310">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7bbe5-310">Minimum supported server</span></span><br/> | <span data-ttu-id="7bbe5-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bbe5-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7bbe5-312">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7bbe5-312">Namespace</span></span><br/>                | <span data-ttu-id="7bbe5-313">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7bbe5-313">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7bbe5-314">MOF</span><span class="sxs-lookup"><span data-stu-id="7bbe5-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bbe5-315"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bbe5-315"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bbe5-316">DLL</span><span class="sxs-lookup"><span data-stu-id="7bbe5-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bbe5-317"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bbe5-317"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bbe5-318">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7bbe5-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbe5-319">**\_Действие CIM**</span><span class="sxs-lookup"><span data-stu-id="7bbe5-319">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

