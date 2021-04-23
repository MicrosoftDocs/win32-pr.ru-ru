---
description: Класс CIM \_ оспроцесс связывает операционную систему и один или несколько процессов, выполняющихся в контексте операционной системы.
ms.assetid: 59d52b29-9d97-464f-bbbc-4191305df8c7
ms.tgt_platform: multiple
title: Класс CIM_OSProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSProcess
- CIM_OSProcess.PartComponent
- CIM_OSProcess.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b11738669c87b402f12932ad65237a512360427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895518"
---
# <a name="cim_osprocess-class"></a><span data-ttu-id="4aaab-103">\_Класс CIM оспроцесс</span><span class="sxs-lookup"><span data-stu-id="4aaab-103">CIM\_OSProcess class</span></span>

<span data-ttu-id="4aaab-104">Класс **CIM \_ оспроцесс** связывает операционную систему и один или несколько процессов, выполняющихся в контексте операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4aaab-104">The **CIM\_OSProcess** class associates the operating system and one or more processes running in the context of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4aaab-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4aaab-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4aaab-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4aaab-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4aaab-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4aaab-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4aaab-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4aaab-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aaab-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4aaab-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A361A7AE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OSProcess : CIM_Component
{
  CIM_Process         REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4aaab-110">Члены</span><span class="sxs-lookup"><span data-stu-id="4aaab-110">Members</span></span>

<span data-ttu-id="4aaab-111">Класс **CIM \_ оспроцесс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4aaab-111">The **CIM\_OSProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="4aaab-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4aaab-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4aaab-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4aaab-113">Properties</span></span>

<span data-ttu-id="4aaab-114">Класс **CIM \_ оспроцесс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4aaab-114">The **CIM\_OSProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4aaab-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="4aaab-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aaab-116">Тип данных: **\_ Операционная система CIM**</span><span class="sxs-lookup"><span data-stu-id="4aaab-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4aaab-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4aaab-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aaab-118">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="4aaab-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4aaab-119">Система [**CIM \_**](cim-operatingsystem.md) , описывающая операционную систему.</span><span class="sxs-lookup"><span data-stu-id="4aaab-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="4aaab-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4aaab-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aaab-121">Тип данных: **\_ процесс CIM**</span><span class="sxs-lookup"><span data-stu-id="4aaab-121">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="4aaab-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4aaab-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aaab-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4aaab-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4aaab-124">[**\_ Процесс CIM**](cim-process.md) , описывающий процесс, выполняемый в контексте операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4aaab-124">A [**CIM\_Process**](cim-process.md) describing the process running in the context of the operating system</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4aaab-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4aaab-125">Remarks</span></span>

<span data-ttu-id="4aaab-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4aaab-126">WMI does not implement this class.</span></span>

<span data-ttu-id="4aaab-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4aaab-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4aaab-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4aaab-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aaab-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4aaab-129">Requirements</span></span>



| <span data-ttu-id="4aaab-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4aaab-130">Requirement</span></span> | <span data-ttu-id="4aaab-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4aaab-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4aaab-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4aaab-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4aaab-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aaab-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4aaab-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4aaab-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4aaab-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4aaab-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4aaab-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4aaab-136">Namespace</span></span><br/>                | <span data-ttu-id="4aaab-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4aaab-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4aaab-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4aaab-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4aaab-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4aaab-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4aaab-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4aaab-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aaab-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aaab-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aaab-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4aaab-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aaab-143">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="4aaab-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

