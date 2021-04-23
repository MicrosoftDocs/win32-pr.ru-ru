---
title: Системмонитор. Логвиевстоп, свойство
description: Возвращает или задает дату окончания, используемую для получения значений счетчика из файлов журнала.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Сисмон свойство Логвиевстоп
- Свойство Логвиевстоп Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, свойство Логвиевстоп
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b725ee2efba22453d44f1e15fb9ce231b07cdb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988615"
---
# <a name="systemmonitorlogviewstop-property"></a><span data-ttu-id="eccd4-106">Системмонитор. Логвиевстоп, свойство</span><span class="sxs-lookup"><span data-stu-id="eccd4-106">SystemMonitor.LogViewStop property</span></span>

<span data-ttu-id="eccd4-107">Возвращает или задает дату окончания, используемую для получения значений счетчика из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="eccd4-107">Retrieves or sets the ending date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="eccd4-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eccd4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eccd4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eccd4-109">Syntax</span></span>


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a><span data-ttu-id="eccd4-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="eccd4-110">Property value</span></span>

<span data-ttu-id="eccd4-111">Дата окончания, используемая для получения значений счетчика из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="eccd4-111">Ending date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="eccd4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eccd4-112">Remarks</span></span>

<span data-ttu-id="eccd4-113">СИСМОН получает значения счетчиков из файлов журнала, которые попадают в [**системмонитор. логвиевстарт**](systemmonitor-logviewstart.md) и даты окончания включительно.</span><span class="sxs-lookup"><span data-stu-id="eccd4-113">SYSMON retrieves counter values from the log files that falls within the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and stop dates, inclusively.</span></span>

<span data-ttu-id="eccd4-114">Если вы не укажете значение для параметра «останавливает» или присвойте этому свойству значение даты, которое позже последней даты, содержащейся в файле журнала, СИСМОН изменяет значение на Последнее значение даты, найденное в файлах журнала.</span><span class="sxs-lookup"><span data-stu-id="eccd4-114">If you do not specify a stop value or you set this property to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span>

<span data-ttu-id="eccd4-115">Если для этого свойства задано значение даты меньше [**логвиевстарт**](systemmonitor-logviewstart.md), сисмон изменяет значение на **логвиевстарт**.</span><span class="sxs-lookup"><span data-stu-id="eccd4-115">If this property is set to a date value that is less than [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON changes the value to the value of **LogViewStart**.</span></span>

<span data-ttu-id="eccd4-116">Необходимо задать дату начала до установки даты окончания. в противном случае оба значения задаются как Date. MinValue, и если даты заданы после установки [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md), то из файла журнала извлекается только первое значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="eccd4-116">You must set the start date before you set the stop date; otherwise, both values are set to Date.MinValue, and if you set the dates after setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md), then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="eccd4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="eccd4-117">Requirements</span></span>



| <span data-ttu-id="eccd4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="eccd4-118">Requirement</span></span> | <span data-ttu-id="eccd4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="eccd4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eccd4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eccd4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eccd4-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="eccd4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="eccd4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eccd4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eccd4-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="eccd4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eccd4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="eccd4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eccd4-125"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="eccd4-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eccd4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eccd4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eccd4-127">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="eccd4-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="eccd4-128">**Системмонитор. Жетлогвиевранже**</span><span class="sxs-lookup"><span data-stu-id="eccd4-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="eccd4-129">**Системмонитор. Логсаурцестоптиме**</span><span class="sxs-lookup"><span data-stu-id="eccd4-129">**SystemMonitor.LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[<span data-ttu-id="eccd4-130">**Системмонитор. Логвиевстарт**</span><span class="sxs-lookup"><span data-stu-id="eccd4-130">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="eccd4-131">**Системмонитор. Сетлогвиевранже**</span><span class="sxs-lookup"><span data-stu-id="eccd4-131">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





