---
title: Системмонитор. Логвиевстарт, свойство
description: Возвращает или задает начальную дату, используемую для получения значений счетчика из файлов журнала.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Сисмон свойство Логвиевстарт
- Логвиевстарт Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Логвиевстарт
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967c44940b195c4d8ddd3028e1d4f307827bbbfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988523"
---
# <a name="systemmonitorlogviewstart-property"></a><span data-ttu-id="97358-106">Системмонитор. Логвиевстарт, свойство</span><span class="sxs-lookup"><span data-stu-id="97358-106">SystemMonitor.LogViewStart property</span></span>

<span data-ttu-id="97358-107">Возвращает или задает начальную дату, используемую для получения значений счетчика из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="97358-107">Retrieves or sets the starting date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="97358-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="97358-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="97358-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97358-109">Syntax</span></span>


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a><span data-ttu-id="97358-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="97358-110">Property value</span></span>

<span data-ttu-id="97358-111">Дата начала, используемая для получения значений счетчиков из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="97358-111">Starting date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="97358-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97358-112">Remarks</span></span>

<span data-ttu-id="97358-113">СИСМОН получает значения счетчиков из файлов журнала, которые находятся в датах начала и [**системмонитор. логвиевстоп**](systemmonitor-logviewstop.md) включительно.</span><span class="sxs-lookup"><span data-stu-id="97358-113">SYSMON retrieves counter values from the log files that falls within the start and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) dates, inclusively.</span></span>

<span data-ttu-id="97358-114">Если не указать дату начала или задать для этого свойства значение даты, находящееся вне диапазона значений даты, находящихся в файлах журнала, СИСМОН изменяет значение на самое раннее значение даты, найденное в файлах журнала.</span><span class="sxs-lookup"><span data-stu-id="97358-114">If you do not specify a start date or if you set this property to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span>

<span data-ttu-id="97358-115">Если для этого свойства задано значение даты, превышающее [**логвиевстоп**](systemmonitor-logviewstop.md), сисмон изменяет значение на **логвиевстоп**.</span><span class="sxs-lookup"><span data-stu-id="97358-115">If this property is set to a date value that is greater than [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON changes the value to the value of **LogViewStop**.</span></span>

<span data-ttu-id="97358-116">Если указать дату начала и окончания, следует указать даты перед настройкой [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="97358-116">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97358-117">Требования</span><span class="sxs-lookup"><span data-stu-id="97358-117">Requirements</span></span>



| <span data-ttu-id="97358-118">Требование</span><span class="sxs-lookup"><span data-stu-id="97358-118">Requirement</span></span> | <span data-ttu-id="97358-119">Значение</span><span class="sxs-lookup"><span data-stu-id="97358-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97358-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97358-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97358-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="97358-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="97358-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97358-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97358-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="97358-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97358-124">DLL</span><span class="sxs-lookup"><span data-stu-id="97358-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97358-125"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="97358-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97358-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97358-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97358-127">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="97358-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="97358-128">**Системмонитор. Жетлогвиевранже**</span><span class="sxs-lookup"><span data-stu-id="97358-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="97358-129">**Системмонитор. файл_журнала**</span><span class="sxs-lookup"><span data-stu-id="97358-129">**SystemMonitor.LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> <dt>

[<span data-ttu-id="97358-130">**Системмонитор. Логвиевстоп**</span><span class="sxs-lookup"><span data-stu-id="97358-130">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="97358-131">**Системмонитор. Логсаурцестарттиме**</span><span class="sxs-lookup"><span data-stu-id="97358-131">**SystemMonitor.LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[<span data-ttu-id="97358-132">**Системмонитор. Сетлогвиевранже**</span><span class="sxs-lookup"><span data-stu-id="97358-132">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





