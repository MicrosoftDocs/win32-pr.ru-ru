---
title: Системмонитор. Скалетофит, метод
description: Масштабирование значений счетчиков в соответствии с графиком.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Метод Скалетофит Сисмон
- Метод Скалетофит Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, метод Скалетофит
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801984"
---
# <a name="systemmonitorscaletofit-method"></a><span data-ttu-id="1affb-106">Системмонитор. Скалетофит, метод</span><span class="sxs-lookup"><span data-stu-id="1affb-106">SystemMonitor.ScaleToFit method</span></span>

<span data-ttu-id="1affb-107">Масштабирование значений счетчиков в соответствии с графиком.</span><span class="sxs-lookup"><span data-stu-id="1affb-107">Scale counter values to fit in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="1affb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1affb-108">Syntax</span></span>


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a><span data-ttu-id="1affb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1affb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1affb-110">*селектедкаунтерсонли* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1affb-110">*selectedCountersOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1affb-111">Значение true, чтобы масштабировать только выбранные счетчики; в противном случае значение false для масштабирования всех счетчиков.</span><span class="sxs-lookup"><span data-stu-id="1affb-111">True to scale only the selected counters; otherwise, false to scale all counters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1affb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1affb-112">Return value</span></span>

<span data-ttu-id="1affb-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1affb-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1affb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1affb-114">Remarks</span></span>

<span data-ttu-id="1affb-115">Этот метод очистит представление графа.</span><span class="sxs-lookup"><span data-stu-id="1affb-115">This method will clear the graph view.</span></span> <span data-ttu-id="1affb-116">Затем СИСМОН использует коэффициент масштабирования, заданный для каждого счетчика, для перерисовки графа, если источник данных является файлом журнала, или для построения диаграммы новых значений счетчиков, если источник данных имеет активность в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="1affb-116">SYSMON then uses the scale factor specified for each counter to redraw the graph if the data source is a log file, or begin graphing new counter values if the data source is real time activity.</span></span>

## <a name="requirements"></a><span data-ttu-id="1affb-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1affb-117">Requirements</span></span>



| <span data-ttu-id="1affb-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1affb-118">Requirement</span></span> | <span data-ttu-id="1affb-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1affb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1affb-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1affb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1affb-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1affb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1affb-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1affb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1affb-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1affb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1affb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1affb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1affb-125"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1affb-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1affb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1affb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1affb-127">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="1affb-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="1affb-128">**Каунтеритем. Скалефактор**</span><span class="sxs-lookup"><span data-stu-id="1affb-128">**CounterItem.ScaleFactor**</span></span>](counteritem-scalefactor.md)
</dt> <dt>

[<span data-ttu-id="1affb-129">**Каунтеритем. выбрано**</span><span class="sxs-lookup"><span data-stu-id="1affb-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





