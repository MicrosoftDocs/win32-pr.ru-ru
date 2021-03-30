---
title: Системмонитор. Упдатеинтервал, свойство
description: Возвращает или задает период времени, в течение которого СИСМОН ожидает до следующего сбора данных счетчика и обновления графика или отчета.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Сисмон свойство Упдатеинтервал
- Упдатеинтервал Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Упдатеинтервал
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988578"
---
# <a name="systemmonitorupdateinterval-property"></a><span data-ttu-id="da53b-106">Системмонитор. Упдатеинтервал, свойство</span><span class="sxs-lookup"><span data-stu-id="da53b-106">SystemMonitor.UpdateInterval property</span></span>

<span data-ttu-id="da53b-107">Возвращает или задает период времени, в течение которого СИСМОН ожидает до следующего сбора данных счетчика и обновления графика или отчета.</span><span class="sxs-lookup"><span data-stu-id="da53b-107">Retrieves or sets the length of time that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span>

<span data-ttu-id="da53b-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="da53b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="da53b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da53b-109">Syntax</span></span>


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a><span data-ttu-id="da53b-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="da53b-110">Property value</span></span>

<span data-ttu-id="da53b-111">Период времени в секундах, в течение которого СИСМОН ожидает до следующего сбора данных счетчика и обновления графика или отчета.</span><span class="sxs-lookup"><span data-stu-id="da53b-111">Length of time, in seconds, that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span> <span data-ttu-id="da53b-112">Минимальный интервал равен 1 секунде (это значение также используется по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="da53b-112">The minimum interval is 1 second (this is also the default value).</span></span> <span data-ttu-id="da53b-113">Максимальное значение — 1 000 000.</span><span class="sxs-lookup"><span data-stu-id="da53b-113">The maximum value is 1,000,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="da53b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da53b-114">Remarks</span></span>

<span data-ttu-id="da53b-115">Это свойство уместно, только если [**системмонитор. мануалупдате**](systemmonitor-manualupdate.md) имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="da53b-115">This property is relevant only when [**SystemMonitor.ManualUpdate**](systemmonitor-manualupdate.md) is set to False.</span></span>

## <a name="requirements"></a><span data-ttu-id="da53b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="da53b-116">Requirements</span></span>



| <span data-ttu-id="da53b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="da53b-117">Requirement</span></span> | <span data-ttu-id="da53b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="da53b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da53b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da53b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="da53b-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="da53b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="da53b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da53b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="da53b-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="da53b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da53b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="da53b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da53b-124"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="da53b-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da53b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da53b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da53b-126">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="da53b-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





