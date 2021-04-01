---
description: '\_Класс СОПОСТАВЛЕНИЯ CIM софтварилементчеккс связывает программный элемент с условием или сведениями о расположении, которые может потребоваться компоненту.'
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: Класс CIM_SoftwareElementChecks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895609"
---
# <a name="cim_softwareelementchecks-class"></a><span data-ttu-id="693d5-103">\_Класс CIM софтварилементчеккс</span><span class="sxs-lookup"><span data-stu-id="693d5-103">CIM\_SoftwareElementChecks class</span></span>

<span data-ttu-id="693d5-104">Класс сопоставления **CIM \_ софтварилементчеккс** связывает программный элемент с условием или сведениями о расположении, которые может потребоваться компоненту.</span><span class="sxs-lookup"><span data-stu-id="693d5-104">The **CIM\_SoftwareElementChecks** association class relates a software element with condition or location information that a feature may require.</span></span>

<span data-ttu-id="693d5-105">Поскольку программные элементы в состоянии готовности к запуску не могут переходить в другое состояние, значение свойства **Phase** ограничено состоянием в состоянии "в", чтобы объекты [**CIM \_ софтварилемент**](cim-softwareelement.md) в состоянии готовности к запуску.</span><span class="sxs-lookup"><span data-stu-id="693d5-105">Because software elements in a ready-to-run state cannot transition into another state, the value of the **Phase** property is restricted to in-state for [**CIM\_SoftwareElement**](cim-softwareelement.md) objects in a ready-to-run state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="693d5-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="693d5-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="693d5-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="693d5-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="693d5-108">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="693d5-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="693d5-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="693d5-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="693d5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="693d5-110">Syntax</span></span>

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a><span data-ttu-id="693d5-111">Члены</span><span class="sxs-lookup"><span data-stu-id="693d5-111">Members</span></span>

<span data-ttu-id="693d5-112">Класс **CIM \_ софтварилементчеккс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="693d5-112">The **CIM\_SoftwareElementChecks** class has these types of members:</span></span>

-   [<span data-ttu-id="693d5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="693d5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="693d5-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="693d5-114">Properties</span></span>

<span data-ttu-id="693d5-115">Класс **CIM \_ софтварилементчеккс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="693d5-115">The **CIM\_SoftwareElementChecks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="693d5-116">**Проверка**</span><span class="sxs-lookup"><span data-stu-id="693d5-116">**Check**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="693d5-117">Тип данных: **\_ Проверка CIM**</span><span class="sxs-lookup"><span data-stu-id="693d5-117">Data type: **CIM\_Check**</span></span>
</dt> <dt>

<span data-ttu-id="693d5-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="693d5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="693d5-119">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**слабая**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="693d5-119">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="693d5-120">Ссылка на проверку.</span><span class="sxs-lookup"><span data-stu-id="693d5-120">Reference to the check.</span></span>

</dd> <dt>

<span data-ttu-id="693d5-121">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="693d5-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="693d5-122">Тип данных: **CIM \_ софтварилемент**</span><span class="sxs-lookup"><span data-stu-id="693d5-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="693d5-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="693d5-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="693d5-124">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="693d5-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="693d5-125">Ссылка на элемент.</span><span class="sxs-lookup"><span data-stu-id="693d5-125">Reference to the element.</span></span>

</dd> <dt>

<span data-ttu-id="693d5-126">**Этап**</span><span class="sxs-lookup"><span data-stu-id="693d5-126">**Phase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="693d5-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="693d5-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="693d5-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="693d5-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="693d5-129">Указывает, является ли проверка, на которую указывает ссылка, проверка в состоянии или проверка следующего состояния.</span><span class="sxs-lookup"><span data-stu-id="693d5-129">Indicates whether the referenced check is an in-state check or a next-state check.</span></span>

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

<span data-ttu-id="693d5-130">**В состоянии** (0)</span><span class="sxs-lookup"><span data-stu-id="693d5-130">**In-State** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

<span data-ttu-id="693d5-131">**Следующее состояние** (1)</span><span class="sxs-lookup"><span data-stu-id="693d5-131">**Next-State** (1)</span></span>


<span data-ttu-id="693d5-132"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="693d5-132"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="693d5-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="693d5-133">Remarks</span></span>

<span data-ttu-id="693d5-134">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="693d5-134">WMI does not implement this class.</span></span> <span data-ttu-id="693d5-135">Классы WMI, производные от **CIM \_ софтварилементчеккс**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="693d5-135">For WMI classes derived from **CIM\_SoftwareElementChecks**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="693d5-136">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="693d5-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="693d5-137">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="693d5-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="693d5-138">Требования</span><span class="sxs-lookup"><span data-stu-id="693d5-138">Requirements</span></span>



| <span data-ttu-id="693d5-139">Требование</span><span class="sxs-lookup"><span data-stu-id="693d5-139">Requirement</span></span> | <span data-ttu-id="693d5-140">Значение</span><span class="sxs-lookup"><span data-stu-id="693d5-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="693d5-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="693d5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="693d5-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="693d5-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="693d5-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="693d5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="693d5-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="693d5-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="693d5-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="693d5-145">Namespace</span></span><br/>                | <span data-ttu-id="693d5-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="693d5-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="693d5-147">MOF</span><span class="sxs-lookup"><span data-stu-id="693d5-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="693d5-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="693d5-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="693d5-149">DLL</span><span class="sxs-lookup"><span data-stu-id="693d5-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="693d5-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="693d5-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

