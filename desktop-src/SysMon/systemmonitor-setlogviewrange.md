---
title: Системмонитор. Сетлогвиевранже, метод
description: Задает начальную дату, используемую для получения значений счетчика из файлов журнала.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Метод Сетлогвиевранже Сисмон
- Метод Сетлогвиевранже Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, метод Сетлогвиевранже
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415116"
---
# <a name="systemmonitorsetlogviewrange-method"></a><span data-ttu-id="16c2c-106">Системмонитор. Сетлогвиевранже, метод</span><span class="sxs-lookup"><span data-stu-id="16c2c-106">SystemMonitor.SetLogViewRange method</span></span>

<span data-ttu-id="16c2c-107">Задает начальную дату, используемую для получения значений счетчика из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="16c2c-107">Sets the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c2c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16c2c-108">Syntax</span></span>


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="16c2c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="16c2c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16c2c-110">Время *начала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16c2c-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16c2c-111">Дата начала, используемая для получения значений счетчиков из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="16c2c-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="16c2c-112">*StopTime* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16c2c-112">*StopTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16c2c-113">Дата окончания, используемая для получения значений счетчика из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="16c2c-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16c2c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16c2c-114">Return value</span></span>

<span data-ttu-id="16c2c-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="16c2c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16c2c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16c2c-116">Remarks</span></span>

<span data-ttu-id="16c2c-117">СИСМОН получает значения счетчиков из файлов журнала, которые находятся в пределах даты начала и окончания, включительно.</span><span class="sxs-lookup"><span data-stu-id="16c2c-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="16c2c-118">Если не указать дату начала или если для даты начала задано значение даты, находящееся вне диапазона значений даты, находящихся в файлах журнала, СИСМОН изменяет значение на самое раннее значение даты, найденное в файлах журнала.</span><span class="sxs-lookup"><span data-stu-id="16c2c-118">If you do not specify a start date or if you set the start date to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span> <span data-ttu-id="16c2c-119">Если начальное значение больше, чем значение параметра, СИСМОН изменяет начальное значение на то же значение, что и значение параметра «останавливает».</span><span class="sxs-lookup"><span data-stu-id="16c2c-119">If the start value is greater than the stop value, SYSMON changes the start value to be the same value as the stop value.</span></span>

<span data-ttu-id="16c2c-120">Если вы не укажете значение для параметра "прерывать" или задали значение даты, которое позже последней даты, содержащейся в файле журнала, СИСМОН изменяет значение на Последнее значение даты, найденное в файлах журнала.</span><span class="sxs-lookup"><span data-stu-id="16c2c-120">If you do not specify a stop value or you set the stop value to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span> <span data-ttu-id="16c2c-121">Если значение параметра "превышено" меньше значения "останавливает", СИСМОН изменяет значение параметра "останавливаюте" на то же значение, что и начальное значение.</span><span class="sxs-lookup"><span data-stu-id="16c2c-121">If the stop value is less than the stop value, SYSMON changes the stop value to be the same value as the start value.</span></span>

<span data-ttu-id="16c2c-122">Если указать дату начала и окончания, следует указать даты перед настройкой [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="16c2c-122">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span> <span data-ttu-id="16c2c-123">Если задать даты после установки **системмонитор. DataSourceType**, то из файла журнала будет получено только первое значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="16c2c-123">If you set the dates after setting **SystemMonitor.DataSourceType**, then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c2c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="16c2c-124">Requirements</span></span>



| <span data-ttu-id="16c2c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="16c2c-125">Requirement</span></span> | <span data-ttu-id="16c2c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="16c2c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16c2c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16c2c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="16c2c-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16c2c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16c2c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16c2c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="16c2c-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16c2c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16c2c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="16c2c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16c2c-132"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="16c2c-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16c2c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16c2c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c2c-134">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="16c2c-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="16c2c-135">**Системмонитор. Жетлогвиевранже**</span><span class="sxs-lookup"><span data-stu-id="16c2c-135">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





