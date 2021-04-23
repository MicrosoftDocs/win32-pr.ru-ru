---
description: Класс CIM \_ руннингос представляет выполняющуюся в данный момент операционную систему. В любой момент в компьютерной системе может выполняться не более одной операционной системы; возможно, компьютерная система не загрузилась или ее операционная система неизвестна.
ms.assetid: 93e3d425-d751-4252-aa81-7d6774c8f8c5
ms.tgt_platform: multiple
title: Класс CIM_RunningOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RunningOS
- CIM_RunningOS.Dependent
- CIM_RunningOS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ff86af88342a1b8f0147ecd9721765794faf39e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807864"
---
# <a name="cim_runningos-class"></a><span data-ttu-id="414a2-104">\_Класс CIM руннингос</span><span class="sxs-lookup"><span data-stu-id="414a2-104">CIM\_RunningOS class</span></span>

<span data-ttu-id="414a2-105">Класс **CIM \_ руннингос** представляет выполняющуюся в данный момент операционную систему.</span><span class="sxs-lookup"><span data-stu-id="414a2-105">The **CIM\_RunningOS** class represents the currently executing operating system.</span></span> <span data-ttu-id="414a2-106">В любой момент в компьютерной системе может выполняться не более одной операционной системы; возможно, компьютерная система не загрузилась или ее операционная система неизвестна.</span><span class="sxs-lookup"><span data-stu-id="414a2-106">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="414a2-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="414a2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="414a2-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="414a2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="414a2-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="414a2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="414a2-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="414a2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="414a2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="414a2-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1F2EA300-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RunningOS : CIM_Dependency
{
  CIM_ComputerSystem  REF Dependent;
  CIM_OperatingSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="414a2-112">Члены</span><span class="sxs-lookup"><span data-stu-id="414a2-112">Members</span></span>

<span data-ttu-id="414a2-113">Класс **CIM \_ руннингос** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="414a2-113">The **CIM\_RunningOS** class has these types of members:</span></span>

-   [<span data-ttu-id="414a2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="414a2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="414a2-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="414a2-115">Properties</span></span>

<span data-ttu-id="414a2-116">Класс **CIM \_ руннингос** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="414a2-116">The **CIM\_RunningOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="414a2-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="414a2-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="414a2-118">Тип данных: **\_ Операционная система CIM**</span><span class="sxs-lookup"><span data-stu-id="414a2-118">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="414a2-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="414a2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="414a2-120">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="414a2-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="414a2-121">Операционная система CIM, описывающая операционную систему, работающую в данный момент на компьютере. [**\_**](cim-operatingsystem.md)</span><span class="sxs-lookup"><span data-stu-id="414a2-121">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system currently running on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="414a2-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="414a2-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="414a2-123">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="414a2-123">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="414a2-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="414a2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="414a2-125">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="414a2-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="414a2-126">Система [**CIM \_**](cim-computersystem.md) , описывающая компьютерную систему.</span><span class="sxs-lookup"><span data-stu-id="414a2-126">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="414a2-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="414a2-127">Remarks</span></span>

<span data-ttu-id="414a2-128">Класс **CIM \_ руннингос** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="414a2-128">The **CIM\_RunningOS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="414a2-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="414a2-129">WMI does not implement this class.</span></span>

<span data-ttu-id="414a2-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="414a2-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="414a2-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="414a2-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="414a2-132">Требования</span><span class="sxs-lookup"><span data-stu-id="414a2-132">Requirements</span></span>



| <span data-ttu-id="414a2-133">Требование</span><span class="sxs-lookup"><span data-stu-id="414a2-133">Requirement</span></span> | <span data-ttu-id="414a2-134">Значение</span><span class="sxs-lookup"><span data-stu-id="414a2-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="414a2-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="414a2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="414a2-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="414a2-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="414a2-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="414a2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="414a2-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="414a2-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="414a2-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="414a2-139">Namespace</span></span><br/>                | <span data-ttu-id="414a2-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="414a2-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="414a2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="414a2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="414a2-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="414a2-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="414a2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="414a2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="414a2-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="414a2-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="414a2-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="414a2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414a2-146">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="414a2-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

