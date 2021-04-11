---
description: Класс CIM \_ процесссреад представляет связь между процессом и потоками, выполняемыми в контексте процесса.
ms.assetid: e71543c5-d9b3-4f98-93a6-08f977a26305
ms.tgt_platform: multiple
title: Класс CIM_ProcessThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessThread
- CIM_ProcessThread.PartComponent
- CIM_ProcessThread.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: afc29d1576355eda1f9e3dfd7ed55d2cca399d5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262560"
---
# <a name="cim_processthread-class"></a><span data-ttu-id="b7d67-103">\_Класс CIM процесссреад</span><span class="sxs-lookup"><span data-stu-id="b7d67-103">CIM\_ProcessThread class</span></span>

<span data-ttu-id="b7d67-104">Класс **CIM \_ процесссреад** представляет связь между процессом и потоками, выполняемыми в контексте процесса.</span><span class="sxs-lookup"><span data-stu-id="b7d67-104">The **CIM\_ProcessThread** class represents a link between a process and the threads running in the context of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7d67-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b7d67-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b7d67-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b7d67-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b7d67-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b7d67-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b7d67-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b7d67-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d67-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7d67-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{B7E6042C-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ProcessThread : CIM_Component
{
  CIM_Thread  REF PartComponent;
  CIM_Process REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="b7d67-110">Члены</span><span class="sxs-lookup"><span data-stu-id="b7d67-110">Members</span></span>

<span data-ttu-id="b7d67-111">Класс **CIM \_ процесссреад** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b7d67-111">The **CIM\_ProcessThread** class has these types of members:</span></span>

-   [<span data-ttu-id="b7d67-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7d67-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7d67-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7d67-113">Properties</span></span>

<span data-ttu-id="b7d67-114">Класс **CIM \_ процесссреад** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b7d67-114">The **CIM\_ProcessThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7d67-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="b7d67-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d67-116">Тип данных: **\_ процесс CIM**</span><span class="sxs-lookup"><span data-stu-id="b7d67-116">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="b7d67-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7d67-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7d67-118">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="b7d67-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b7d67-119">[**\_ Процесс CIM**](cim-process.md) , описывающий процесс.</span><span class="sxs-lookup"><span data-stu-id="b7d67-119">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="b7d67-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b7d67-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d67-121">Тип данных: **\_ поток CIM**</span><span class="sxs-lookup"><span data-stu-id="b7d67-121">Data type: **CIM\_Thread**</span></span>
</dt> <dt>

<span data-ttu-id="b7d67-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7d67-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7d67-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7d67-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7d67-124">[**\_ Поток CIM**](cim-thread.md) , описывающий поток, выполняемый в контексте процесса.</span><span class="sxs-lookup"><span data-stu-id="b7d67-124">A [**CIM\_Thread**](cim-thread.md) that describes the thread running in the context of the process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7d67-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7d67-125">Remarks</span></span>

<span data-ttu-id="b7d67-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b7d67-126">WMI does not implement this class.</span></span>

<span data-ttu-id="b7d67-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b7d67-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b7d67-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b7d67-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d67-129">Требования</span><span class="sxs-lookup"><span data-stu-id="b7d67-129">Requirements</span></span>



| <span data-ttu-id="b7d67-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b7d67-130">Requirement</span></span> | <span data-ttu-id="b7d67-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b7d67-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d67-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7d67-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d67-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7d67-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7d67-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7d67-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d67-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7d67-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7d67-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b7d67-136">Namespace</span></span><br/>                | <span data-ttu-id="b7d67-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b7d67-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7d67-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b7d67-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7d67-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7d67-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7d67-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b7d67-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7d67-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7d67-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d67-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7d67-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d67-143">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="b7d67-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

