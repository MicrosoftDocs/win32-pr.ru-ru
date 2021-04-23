---
description: Класс CIM \_ хостеджобдестинатион представляет ассоциацию между назначением задания и системой, в которой оно находится. В системе может размещаться много очередей заданий. Назначения заданий откладываются на систему размещения.
ms.assetid: 5d853826-1f27-417b-a053-5e0ee9816376
ms.tgt_platform: multiple
title: Класс CIM_HostedJobDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedJobDestination
- CIM_HostedJobDestination.Dependent
- CIM_HostedJobDestination.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c22e911c6b0adcc38de11fd2410e4797c9381a25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262668"
---
# <a name="cim_hostedjobdestination-class"></a><span data-ttu-id="be9e9-105">\_Класс CIM хостеджобдестинатион</span><span class="sxs-lookup"><span data-stu-id="be9e9-105">CIM\_HostedJobDestination class</span></span>

<span data-ttu-id="be9e9-106">Класс **CIM \_ хостеджобдестинатион** представляет ассоциацию между назначением задания и системой, в которой оно находится.</span><span class="sxs-lookup"><span data-stu-id="be9e9-106">The **CIM\_HostedJobDestination** class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="be9e9-107">В системе может размещаться много очередей заданий.</span><span class="sxs-lookup"><span data-stu-id="be9e9-107">A system may host many job queues.</span></span> <span data-ttu-id="be9e9-108">Назначения заданий откладываются на систему размещения.</span><span class="sxs-lookup"><span data-stu-id="be9e9-108">Job destinations defer to the hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be9e9-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="be9e9-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="be9e9-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="be9e9-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="be9e9-111">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="be9e9-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="be9e9-112">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="be9e9-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9e9-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be9e9-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{7880DD16-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedJobDestination : CIM_Dependency
{
  CIM_JobDestination REF Dependent;
  CIM_System         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="be9e9-114">Члены</span><span class="sxs-lookup"><span data-stu-id="be9e9-114">Members</span></span>

<span data-ttu-id="be9e9-115">Класс **CIM \_ хостеджобдестинатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be9e9-115">The **CIM\_HostedJobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="be9e9-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="be9e9-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be9e9-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="be9e9-117">Properties</span></span>

<span data-ttu-id="be9e9-118">Класс **CIM \_ хостеджобдестинатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be9e9-118">The **CIM\_HostedJobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be9e9-119">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="be9e9-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be9e9-120">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="be9e9-120">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="be9e9-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be9e9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be9e9-122">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="be9e9-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="be9e9-123">[**\_ Система CIM**](cim-system.md) , которая описывает систему размещения.</span><span class="sxs-lookup"><span data-stu-id="be9e9-123">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="be9e9-124">**Него**</span><span class="sxs-lookup"><span data-stu-id="be9e9-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be9e9-125">Тип данных: **CIM \_ жобдестинатион**</span><span class="sxs-lookup"><span data-stu-id="be9e9-125">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="be9e9-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be9e9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be9e9-127">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимый), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="be9e9-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="be9e9-128">[**\_ Жобдестинатион CIM**](cim-jobdestination.md) , описывающий назначение задания, размещенного в системе.</span><span class="sxs-lookup"><span data-stu-id="be9e9-128">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be9e9-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be9e9-129">Remarks</span></span>

<span data-ttu-id="be9e9-130">**Модель CIM \_ Хостеджобдестинатион** является производным [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="be9e9-130">**CIM\_HostedJobDestination** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="be9e9-131">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="be9e9-131">WMI does not implement this class.</span></span>

<span data-ttu-id="be9e9-132">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="be9e9-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="be9e9-133">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="be9e9-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="be9e9-134">Требования</span><span class="sxs-lookup"><span data-stu-id="be9e9-134">Requirements</span></span>



| <span data-ttu-id="be9e9-135">Требование</span><span class="sxs-lookup"><span data-stu-id="be9e9-135">Requirement</span></span> | <span data-ttu-id="be9e9-136">Значение</span><span class="sxs-lookup"><span data-stu-id="be9e9-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be9e9-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be9e9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="be9e9-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be9e9-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be9e9-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be9e9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="be9e9-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be9e9-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be9e9-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="be9e9-141">Namespace</span></span><br/>                | <span data-ttu-id="be9e9-142">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="be9e9-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be9e9-143">MOF</span><span class="sxs-lookup"><span data-stu-id="be9e9-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be9e9-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be9e9-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be9e9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="be9e9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be9e9-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be9e9-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9e9-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be9e9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9e9-148">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="be9e9-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

