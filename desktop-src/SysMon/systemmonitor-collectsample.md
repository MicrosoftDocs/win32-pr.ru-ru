---
title: Системмонитор Коллектсампле, метод
description: Выбирает значение для каждого счетчика в объекте Counters.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Метод Коллектсампле Сисмон
- Метод Коллектсампле Сисмон, интерфейс Системмонитор
- Интерфейс Системмонитор Сисмон, метод Коллектсампле
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490989"
---
# <a name="systemmonitorcollectsample-method"></a><span data-ttu-id="f38be-106">Метод Системмонитор:: Коллектсампле</span><span class="sxs-lookup"><span data-stu-id="f38be-106">SystemMonitor::CollectSample method</span></span>

<span data-ttu-id="f38be-107">Выбирает значение для каждого счетчика в объекте [**Counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="f38be-107">Samples a value for each counter in the [**Counters**](counters.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f38be-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f38be-108">Syntax</span></span>


```VB
Sub CollectSample()
```



## <a name="parameters"></a><span data-ttu-id="f38be-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f38be-109">Parameters</span></span>

<span data-ttu-id="f38be-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f38be-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f38be-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f38be-111">Return value</span></span>

<span data-ttu-id="f38be-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f38be-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f38be-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f38be-113">Remarks</span></span>

<span data-ttu-id="f38be-114">Вызывайте **коллектсампле** только в том случае, если [**Мануалупдате**](systemmonitor-manualupdate.md) имеет значение true, а значения счетчика выборки из текущей активности компьютера не используют этот метод при выборке из файла журнала.</span><span class="sxs-lookup"><span data-stu-id="f38be-114">Call **CollectSample** only if [**ManualUpdate**](systemmonitor-manualupdate.md) is True and you are sampling counter values from the current activity of the computer do not use this method when sampling from a log file.</span></span> <span data-ttu-id="f38be-115">Диаграмма или отчет будут обновлены новым значением.</span><span class="sxs-lookup"><span data-stu-id="f38be-115">The graph or report is updated with the new value.</span></span> <span data-ttu-id="f38be-116">Обратите внимание, что для диаграмм некоторых типов диаграмм требуются два образца, например линейный график.</span><span class="sxs-lookup"><span data-stu-id="f38be-116">Note that some types of graphs need two samples in order to graph the data, for example, the line graph.</span></span>

<span data-ttu-id="f38be-117">Чтобы получить уведомление при сборе примера, реализуйте событие [**онсамплеколлектед**](-systemmonitor-onsamplecollected.md) .</span><span class="sxs-lookup"><span data-stu-id="f38be-117">To receive notification when the sample has been collected, implement the [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="f38be-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f38be-118">Requirements</span></span>



| <span data-ttu-id="f38be-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f38be-119">Requirement</span></span> | <span data-ttu-id="f38be-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f38be-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f38be-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f38be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f38be-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f38be-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f38be-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f38be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f38be-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f38be-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f38be-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f38be-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f38be-126"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f38be-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f38be-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f38be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38be-128">**Счетчики**</span><span class="sxs-lookup"><span data-stu-id="f38be-128">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="f38be-129">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="f38be-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





