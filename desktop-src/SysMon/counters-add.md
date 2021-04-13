---
title: Метод Counters. Add
description: Добавляет экземпляр Каунтеритем в коллекцию.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Добавить метод Сисмон
- Метод Add Сисмон, класс Counters
- Класс счетчиков Сисмон, метод Add
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489720"
---
# <a name="countersadd-method"></a><span data-ttu-id="b0960-106">Метод Counters. Add</span><span class="sxs-lookup"><span data-stu-id="b0960-106">Counters.Add method</span></span>

<span data-ttu-id="b0960-107">Добавляет экземпляр [**каунтеритем**](counteritem.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="b0960-107">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0960-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0960-108">Syntax</span></span>


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a><span data-ttu-id="b0960-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0960-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0960-110">*путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0960-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0960-111">Путь к счетчику.</span><span class="sxs-lookup"><span data-stu-id="b0960-111">Path to the counter.</span></span> <span data-ttu-id="b0960-112">Путь может включать имя компьютера и должно включать имя объекта производительности, имя экземпляра объекта, если указанный объект производительности поддерживает несколько экземпляров, и имя счетчика.</span><span class="sxs-lookup"><span data-stu-id="b0960-112">The path can include a machine name, and must include a performance object name, an object instance name if the specified performance object supports multiple instances, and a counter name.</span></span> <span data-ttu-id="b0960-113">В этой спецификации пути регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="b0960-113">This path specification is not case-sensitive.</span></span>

<span data-ttu-id="b0960-114">Дополнительные сведения об указании пути счетчика см. в разделе [Указание пути счетчика](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span><span class="sxs-lookup"><span data-stu-id="b0960-114">For details on specifying a counter path, see [Specifying a Counter Path](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span></span>

</dd> </dl>

## <a name="exceptions"></a><span data-ttu-id="b0960-115">Исключения</span><span class="sxs-lookup"><span data-stu-id="b0960-115">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0960-116">Тип исключения</span><span class="sxs-lookup"><span data-stu-id="b0960-116">Exception type</span></span></th>
<th><span data-ttu-id="b0960-117">Условие</span><span class="sxs-lookup"><span data-stu-id="b0960-117">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b0960-118"><strong>System. Runtime. InteropServices. COMException</strong></span><span class="sxs-lookup"><span data-stu-id="b0960-118"><strong>System.Runtime.InteropServices.COMException</strong></span></span></td>
<td><span data-ttu-id="b0960-119">Это исключение может быть получено по одной из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="b0960-119">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="b0960-120">Указанный объект производительности не найден на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b0960-120">The specified performance object was not found on the computer.</span></span> <span data-ttu-id="b0960-121">Значение Err. Number — 0xC0000BB8.</span><span class="sxs-lookup"><span data-stu-id="b0960-121">The Err.Number value is 0xC0000BB8.</span></span></li>
<li><span data-ttu-id="b0960-122">Не удалось найти указанный счетчик.</span><span class="sxs-lookup"><span data-stu-id="b0960-122">The specified counter could not be found.</span></span> <span data-ttu-id="b0960-123">Значение Err. Number — 0xC0000BB9.</span><span class="sxs-lookup"><span data-stu-id="b0960-123">The Err.Number value is 0xC0000BB9.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b0960-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0960-124">Remarks</span></span>

<span data-ttu-id="b0960-125">Если в параметре *PathName* указан подстановочный знак, метод **Add** создает по одному объекту [**каунтеритем**](counteritem.md) для каждого развернутого пути.</span><span class="sxs-lookup"><span data-stu-id="b0960-125">If you specify a wildcard counter in the *pathname* parameter, the **Add** method creates one [**CounterItem**](counteritem.md) object for each expanded path.</span></span> <span data-ttu-id="b0960-126">Метод **Add** возвращает указатель на первый добавленный **каунтеритем**.</span><span class="sxs-lookup"><span data-stu-id="b0960-126">The **Add** method then returns a pointer to the first added **CounterItem**.</span></span>

<span data-ttu-id="b0960-127">Если подстановочный знак приведет к дублированию счетчика, то ошибка не будет передана и дубликаты не будут созданы.</span><span class="sxs-lookup"><span data-stu-id="b0960-127">If the wildcard would result in a duplicate counter, the error is not reported and no duplicate is created.</span></span> <span data-ttu-id="b0960-128">Если состояние ошибки возникает до создания всех счетчиков, отображается сообщение об ошибке и оставшиеся счетчики не создаются.</span><span class="sxs-lookup"><span data-stu-id="b0960-128">If an error condition occurs before all counters are created, the error is reported and the remaining counters are not created.</span></span>

<span data-ttu-id="b0960-129">Количество счетчиков, которые можно добавить, не ограничено. Однако СИСМОН будет выграфике только первые счетчики 1 024 в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b0960-129">There is no limit to the number of counters that you can add; however, SYSMON will graph only the first 1,024 counters in the collection.</span></span> <span data-ttu-id="b0960-130">Количество счетчиков, которые СИСМОН будут отображаться в отчете, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="b0960-130">There is no limit on the number of counters that SYSMON will display in a report.</span></span>

<span data-ttu-id="b0960-131">Чтобы получить уведомление при добавлении счетчика, реализуйте событие [онкаунтераддед](systemmonitor-oncounteradded.md) .</span><span class="sxs-lookup"><span data-stu-id="b0960-131">To receive notification when a counter is added, implement the [OnCounterAdded](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0960-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b0960-132">Requirements</span></span>



| <span data-ttu-id="b0960-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b0960-133">Requirement</span></span> | <span data-ttu-id="b0960-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b0960-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0960-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0960-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b0960-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0960-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b0960-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0960-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b0960-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0960-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0960-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b0960-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0960-140"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b0960-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0960-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0960-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0960-142">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="b0960-142">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="b0960-143">**Счетчики**</span><span class="sxs-lookup"><span data-stu-id="b0960-143">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="b0960-144">**Системмонитор. Бровсекаунтерс**</span><span class="sxs-lookup"><span data-stu-id="b0960-144">**SystemMonitor.BrowseCounters**</span></span>](systemmonitor-browsecounters.md)
</dt> </dl>

 

