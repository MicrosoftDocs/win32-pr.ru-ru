---
description: '\_Ассоциация ЖОБДЕСТИНАТИОНЖОБС CIM описывает место отправки задания для обработки (то есть назначение задания).'
ms.assetid: 6f732d34-2284-4909-a966-6b4066780cb0
ms.tgt_platform: multiple
title: Класс CIM_JobDestinationJobs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestinationJobs
- CIM_JobDestinationJobs.Dependent
- CIM_JobDestinationJobs.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e59e20f776c410db53294b6f6e98a1b13aef0de
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262664"
---
# <a name="cim_jobdestinationjobs-class"></a><span data-ttu-id="02e8d-103">\_Класс CIM жобдестинатионжобс</span><span class="sxs-lookup"><span data-stu-id="02e8d-103">CIM\_JobDestinationJobs class</span></span>

<span data-ttu-id="02e8d-104">Ассоциация **\_ жобдестинатионжобс CIM** описывает место отправки задания для обработки (то есть назначение задания).</span><span class="sxs-lookup"><span data-stu-id="02e8d-104">The **CIM\_JobDestinationJobs** association describes where a job is submitted for processing (that is, to which job destination).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02e8d-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="02e8d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="02e8d-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="02e8d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="02e8d-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="02e8d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="02e8d-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="02e8d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e8d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02e8d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D079BEE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestinationJobs : CIM_Dependency
{
  CIM_Job            REF Dependent;
  CIM_JobDestination REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="02e8d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="02e8d-110">Members</span></span>

<span data-ttu-id="02e8d-111">Класс **CIM \_ жобдестинатионжобс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="02e8d-111">The **CIM\_JobDestinationJobs** class has these types of members:</span></span>

-   [<span data-ttu-id="02e8d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="02e8d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02e8d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="02e8d-113">Properties</span></span>

<span data-ttu-id="02e8d-114">Класс **CIM \_ жобдестинатионжобс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="02e8d-114">The **CIM\_JobDestinationJobs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02e8d-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="02e8d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02e8d-116">Тип данных: **CIM \_ жобдестинатион**</span><span class="sxs-lookup"><span data-stu-id="02e8d-116">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="02e8d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02e8d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02e8d-118">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="02e8d-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="02e8d-119">[**\_ Жобдестинатион CIM**](cim-jobdestination.md) , описывающий назначение задания, возможно, очередь.</span><span class="sxs-lookup"><span data-stu-id="02e8d-119">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination, possibly a queue.</span></span>

</dd> <dt>

<span data-ttu-id="02e8d-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="02e8d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02e8d-121">Тип данных: **\_ Задание CIM** .</span><span class="sxs-lookup"><span data-stu-id="02e8d-121">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="02e8d-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02e8d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02e8d-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="02e8d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="02e8d-124">[**\_ Задание CIM**](cim-job.md) , описывающее задание, которое находится в очереди или назначении заданий.</span><span class="sxs-lookup"><span data-stu-id="02e8d-124">A [**CIM\_Job**](cim-job.md) describing the job that is in the job queue/Destination.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02e8d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02e8d-125">Remarks</span></span>

<span data-ttu-id="02e8d-126">**Модель CIM \_ Жобдестинатионжобс** является производным [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="02e8d-126">**CIM\_JobDestinationJobs** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="02e8d-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="02e8d-127">WMI does not implement this class.</span></span>

<span data-ttu-id="02e8d-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="02e8d-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="02e8d-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="02e8d-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e8d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="02e8d-130">Requirements</span></span>



| <span data-ttu-id="02e8d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="02e8d-131">Requirement</span></span> | <span data-ttu-id="02e8d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="02e8d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02e8d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02e8d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="02e8d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02e8d-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02e8d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02e8d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="02e8d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02e8d-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02e8d-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="02e8d-137">Namespace</span></span><br/>                | <span data-ttu-id="02e8d-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="02e8d-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02e8d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="02e8d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02e8d-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02e8d-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02e8d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="02e8d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02e8d-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02e8d-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02e8d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02e8d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e8d-144">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="02e8d-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

