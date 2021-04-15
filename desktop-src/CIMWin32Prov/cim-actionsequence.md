---
description: '\_Ассоциация АКТИОНСЕКУЕНЦЕ CIM определяет ряд операций, которые переходят программный элемент (на который ссылается \_ Ассоциация софтварилементактионс CIM) в следующее состояние или удаляет программный элемент из текущего состояния.'
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: Класс CIM_ActionSequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655842"
---
# <a name="cim_actionsequence-class"></a><span data-ttu-id="4ba45-103">\_Класс CIM актионсекуенце</span><span class="sxs-lookup"><span data-stu-id="4ba45-103">CIM\_ActionSequence class</span></span>

<span data-ttu-id="4ba45-104">Ассоциация **\_ актионсекуенце CIM** определяет ряд операций, которые переходят программный элемент (на который ссылается Ассоциация [**\_ софтварилементактионс CIM**](cim-softwareelementactions.md) ) в следующее состояние или удаляет программный элемент из текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="4ba45-104">The **CIM\_ActionSequence** association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

<span data-ttu-id="4ba45-105">Действия следующего состояния и действия по удалению, связанные с определенным программным элементом, должны быть непрерывной последовательностью.</span><span class="sxs-lookup"><span data-stu-id="4ba45-105">The next-state actions and uninstall actions associated with a particular software element must be a continuous sequence.</span></span> <span data-ttu-id="4ba45-106">Так как **CIM \_ актионсекуенце** является ассоциацией, циклы класса [**\_ действия CIM**](cim-action.md) с ролями для действия "предыдущие" и "Далее" формируют последовательность.</span><span class="sxs-lookup"><span data-stu-id="4ba45-106">Since **CIM\_ActionSequence** is an association, the loops on the [**CIM\_Action**](cim-action.md) class, with roles for the "prior" action and "next" action, form a sequence.</span></span>

<span data-ttu-id="4ba45-107">Необходимость в непрерывной последовательности подразумевает следующее:</span><span class="sxs-lookup"><span data-stu-id="4ba45-107">The need for a continuous sequence implies:</span></span>

-   <span data-ttu-id="4ba45-108">В наборе действий следующего состояния или удаления существует только одно действие, которое не имеет экземпляра ассоциации **CIM \_ актионсекуенце** , ссылающегося на него в "следующей" роли.</span><span class="sxs-lookup"><span data-stu-id="4ba45-108">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "next" role.</span></span> <span data-ttu-id="4ba45-109">Это первое действие в последовательности.</span><span class="sxs-lookup"><span data-stu-id="4ba45-109">This is the first action in the sequence.</span></span>
-   <span data-ttu-id="4ba45-110">В наборе действий следующего состояния или удаления существует только одно действие, которое не имеет экземпляра ассоциации **CIM \_ актионсекуенце** , ссылающегося на него в "предыдущей" роли.</span><span class="sxs-lookup"><span data-stu-id="4ba45-110">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "prior" role.</span></span> <span data-ttu-id="4ba45-111">Это последнее действие в последовательности.</span><span class="sxs-lookup"><span data-stu-id="4ba45-111">This is the last action in the sequence.</span></span>
-   <span data-ttu-id="4ba45-112">Все остальные действия в наборе действий следующего состояния и удаления должны участвовать в двух экземплярах ассоциации **\_ актионсекуенце CIM** , одной в «предыдущей» роли, а другая — в «следующей» роли.</span><span class="sxs-lookup"><span data-stu-id="4ba45-112">All other actions within the set of next-state and uninstall actions must participate in two instances of the **CIM\_ActionSequence** association, one in a "prior" role and one in the "next" role.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ba45-113">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4ba45-113">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4ba45-114">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4ba45-114">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4ba45-115">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4ba45-115">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4ba45-116">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4ba45-116">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ba45-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ba45-117">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a><span data-ttu-id="4ba45-118">Члены</span><span class="sxs-lookup"><span data-stu-id="4ba45-118">Members</span></span>

<span data-ttu-id="4ba45-119">Класс **CIM \_ актионсекуенце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4ba45-119">The **CIM\_ActionSequence** class has these types of members:</span></span>

-   [<span data-ttu-id="4ba45-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="4ba45-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ba45-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="4ba45-121">Properties</span></span>

<span data-ttu-id="4ba45-122">Класс **CIM \_ актионсекуенце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4ba45-122">The **CIM\_ActionSequence** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ba45-123">**Вперед**</span><span class="sxs-lookup"><span data-stu-id="4ba45-123">**Next**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ba45-124">Тип данных: **\_ действие CIM**</span><span class="sxs-lookup"><span data-stu-id="4ba45-124">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="4ba45-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4ba45-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ba45-126">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="4ba45-126">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="4ba45-127">Ссылка на следующее действие.</span><span class="sxs-lookup"><span data-stu-id="4ba45-127">Reference to the next action.</span></span>

</dd> <dt>

<span data-ttu-id="4ba45-128">**Установкой**</span><span class="sxs-lookup"><span data-stu-id="4ba45-128">**Prior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ba45-129">Тип данных: **\_ действие CIM**</span><span class="sxs-lookup"><span data-stu-id="4ba45-129">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="4ba45-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4ba45-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ba45-131">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="4ba45-131">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="4ba45-132">Ссылка на прежнее действие.</span><span class="sxs-lookup"><span data-stu-id="4ba45-132">Reference to the prior action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ba45-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ba45-133">Remarks</span></span>

<span data-ttu-id="4ba45-134">Классы [**\_ действий CIM**](cim-action.md) , участвующие в этой ассоциации, должны иметь одинаковое значение для свойства **Direction** .</span><span class="sxs-lookup"><span data-stu-id="4ba45-134">The [**CIM\_Action**](cim-action.md) classes participating in this association must have the same value for the **Direction** property.</span></span>

<span data-ttu-id="4ba45-135">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4ba45-135">WMI does not implement this class.</span></span>

<span data-ttu-id="4ba45-136">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4ba45-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4ba45-137">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4ba45-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ba45-138">Требования</span><span class="sxs-lookup"><span data-stu-id="4ba45-138">Requirements</span></span>



| <span data-ttu-id="4ba45-139">Требование</span><span class="sxs-lookup"><span data-stu-id="4ba45-139">Requirement</span></span> | <span data-ttu-id="4ba45-140">Значение</span><span class="sxs-lookup"><span data-stu-id="4ba45-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba45-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ba45-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4ba45-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ba45-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ba45-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ba45-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4ba45-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ba45-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ba45-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4ba45-145">Namespace</span></span><br/>                | <span data-ttu-id="4ba45-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4ba45-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4ba45-147">MOF</span><span class="sxs-lookup"><span data-stu-id="4ba45-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ba45-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ba45-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ba45-149">DLL</span><span class="sxs-lookup"><span data-stu-id="4ba45-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ba45-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ba45-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ba45-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ba45-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ba45-152">Классы CIM</span><span class="sxs-lookup"><span data-stu-id="4ba45-152">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

