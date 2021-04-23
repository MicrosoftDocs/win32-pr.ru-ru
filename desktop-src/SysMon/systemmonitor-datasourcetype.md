---
title: Системмонитор DataSourceType, свойство
description: Возвращает или задает источник данных счетчика производительности.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Сисмон свойство DataSourceType
- Свойство DataSourceType Сисмон, интерфейс Системмонитор
- Интерфейс Системмонитор Сисмон, свойство DataSourceType
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071839"
---
# <a name="systemmonitordatasourcetype-property"></a><span data-ttu-id="f2e85-106">Системмонитор: свойство Атасаурцетипе:D</span><span class="sxs-lookup"><span data-stu-id="f2e85-106">SystemMonitor::DataSourceType property</span></span>

<span data-ttu-id="f2e85-107">Возвращает или задает источник данных счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="f2e85-107">Retrieves or sets the source of the performance counter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e85-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2e85-108">Syntax</span></span>


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="f2e85-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2e85-109">Property value</span></span>

<span data-ttu-id="f2e85-110">Источник данных счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="f2e85-110">Source of the performance counter data.</span></span> <span data-ttu-id="f2e85-111">Возможные значения см. в разделе [**датасаурцетипеконстантс**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="f2e85-111">For possible values, see [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="f2e85-112">Исключения</span><span class="sxs-lookup"><span data-stu-id="f2e85-112">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2e85-113">Тип исключения</span><span class="sxs-lookup"><span data-stu-id="f2e85-113">Exception type</span></span></th>
<th><span data-ttu-id="f2e85-114">Условие</span><span class="sxs-lookup"><span data-stu-id="f2e85-114">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f2e85-115"><strong>System. ArgumentException</strong></span><span class="sxs-lookup"><span data-stu-id="f2e85-115"><strong>System.ArgumentException</strong></span></span></td>
<td><span data-ttu-id="f2e85-116">Это исключение может быть получено по одной из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="f2e85-116">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="f2e85-117">Указано недопустимое значение источника данных.</span><span class="sxs-lookup"><span data-stu-id="f2e85-117">The specified data source value is not valid.</span></span></li>
<li><span data-ttu-id="f2e85-118">Если источником данных является файл журнала, СИСМОН не может найти один из указанных файлов.</span><span class="sxs-lookup"><span data-stu-id="f2e85-118">If the data source is a log file, SYSMON cannot find one of the specified files.</span></span> <span data-ttu-id="f2e85-119">Значение Err. Number — 0xC0000BD1.</span><span class="sxs-lookup"><span data-stu-id="f2e85-119">The Err.Number value is 0xC0000BD1.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f2e85-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2e85-120">Remarks</span></span>

<span data-ttu-id="f2e85-121">**До Windows Vista:** Невозможно добавить или удалить файлы журнала из [**коллекции файлов журнала**](systemmonitor-logfiles.md) , если для этого свойства задано значение сисмонлогфилес.</span><span class="sxs-lookup"><span data-stu-id="f2e85-121">**Prior to Windows Vista:** You cannot add or remove a log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of this property is set to sysmonLogFiles.</span></span> <span data-ttu-id="f2e85-122">Присвойте этому свойству значение Сисмонлогфилес после создания или изменения коллекции файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="f2e85-122">Only set the value of this property to sysmonLogFiles after creating or modifying the log file collection.</span></span>

<span data-ttu-id="f2e85-123">Кроме того, нельзя изменить свойства [**склдсннаме**](systemmonitor-sqldsnname.md) и [**скллогсетнаме**](systemmonitor-sqllogsetname.md) , если для этого свойства не должно быть задано значение сисмонскллог.</span><span class="sxs-lookup"><span data-stu-id="f2e85-123">Also, you cannot modify the [**SqlDsnName**](systemmonitor-sqldsnname.md) and [**SqlLogSetName**](systemmonitor-sqllogsetname.md) properties if the value of this property must not be set to sysmonSqlLog.</span></span> <span data-ttu-id="f2e85-124">Присвойте этому свойству значение Сисмонскллог после изменения имен сервера и базы данных.</span><span class="sxs-lookup"><span data-stu-id="f2e85-124">Only set the value of this property to sysmonSqlLog after modifying the server and database names.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e85-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f2e85-125">Requirements</span></span>



| <span data-ttu-id="f2e85-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f2e85-126">Requirement</span></span> | <span data-ttu-id="f2e85-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f2e85-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e85-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2e85-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e85-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2e85-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f2e85-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2e85-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e85-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2e85-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2e85-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f2e85-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2e85-133"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f2e85-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e85-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2e85-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e85-135">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="f2e85-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





