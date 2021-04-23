---
title: Системмонитор. Жетлогвиевранже, метод
description: Возвращает дату начала, используемую для получения значений счетчика из файлов журнала.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Метод Жетлогвиевранже Сисмон
- Метод Жетлогвиевранже Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, метод Жетлогвиевранже
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534184"
---
# <a name="systemmonitorgetlogviewrange-method"></a><span data-ttu-id="4cd5d-106">Системмонитор. Жетлогвиевранже, метод</span><span class="sxs-lookup"><span data-stu-id="4cd5d-106">SystemMonitor.GetLogViewRange method</span></span>

<span data-ttu-id="4cd5d-107">Возвращает дату начала, используемую для получения значений счетчика из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="4cd5d-107">Retrieves the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd5d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cd5d-108">Syntax</span></span>


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="4cd5d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cd5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cd5d-110">Время *начала* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4cd5d-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd5d-111">Дата начала, используемая для получения значений счетчиков из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="4cd5d-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="4cd5d-112">*StopTime* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4cd5d-112">*StopTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd5d-113">Дата окончания, используемая для получения значений счетчика из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="4cd5d-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cd5d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cd5d-114">Return value</span></span>

<span data-ttu-id="4cd5d-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4cd5d-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cd5d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cd5d-116">Remarks</span></span>

<span data-ttu-id="4cd5d-117">СИСМОН получает значения счетчиков из файлов журнала, которые находятся в пределах даты начала и окончания, включительно.</span><span class="sxs-lookup"><span data-stu-id="4cd5d-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="4cd5d-118">Использование этого метода аналогично доступу к свойствам [**системмонитор. логвиевстарт**](systemmonitor-logviewstart.md) и [**системмонитор. логвиевстоп**](systemmonitor-logviewstop.md) .</span><span class="sxs-lookup"><span data-stu-id="4cd5d-118">Using this method is the same as accessing the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cd5d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4cd5d-119">Requirements</span></span>



| <span data-ttu-id="4cd5d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4cd5d-120">Requirement</span></span> | <span data-ttu-id="4cd5d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd5d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd5d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cd5d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4cd5d-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cd5d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cd5d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cd5d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4cd5d-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4cd5d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4cd5d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4cd5d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cd5d-127"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="4cd5d-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd5d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cd5d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd5d-129">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="4cd5d-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="4cd5d-130">**Системмонитор. Сетлогвиевранже**</span><span class="sxs-lookup"><span data-stu-id="4cd5d-130">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





