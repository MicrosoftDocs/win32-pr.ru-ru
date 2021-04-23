---
title: Системмонитор. Онкаунтераддед, событие
description: Уведомляет о добавлении счетчика в коллекцию счетчиков.
ms.assetid: f798443f-e2f1-4d25-b142-d88d6e4fe12c
keywords:
- Сисмон события Онкаунтераддед
- Онкаунтераддед Event Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, событие Онкаунтераддед
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterAdded
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f150709114ae25da89b107c7de85e3c5eca2551f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661888"
---
# <a name="systemmonitoroncounteradded-event"></a><span data-ttu-id="3904e-106">Системмонитор. Онкаунтераддед, событие</span><span class="sxs-lookup"><span data-stu-id="3904e-106">SystemMonitor.OnCounterAdded event</span></span>

<span data-ttu-id="3904e-107">Уведомляет о добавлении счетчика в коллекцию [**счетчиков**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="3904e-107">Notifies you when a counter is added to the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3904e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3904e-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterAdded( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="3904e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3904e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3904e-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3904e-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3904e-111">Индекс счетчика, добавленного в объект коллекции [**Counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="3904e-111">Index of the counter added to the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3904e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3904e-112">Return value</span></span>

<span data-ttu-id="3904e-113">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3904e-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3904e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3904e-114">Requirements</span></span>



| <span data-ttu-id="3904e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3904e-115">Requirement</span></span> | <span data-ttu-id="3904e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3904e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3904e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3904e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3904e-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3904e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3904e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3904e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3904e-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3904e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3904e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3904e-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3904e-122"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3904e-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3904e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3904e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3904e-124">**Системмонитор. Онкаунтерделетед**</span><span class="sxs-lookup"><span data-stu-id="3904e-124">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> <dt>

[<span data-ttu-id="3904e-125">**Системмонитор. Онкаунтерселектед**</span><span class="sxs-lookup"><span data-stu-id="3904e-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





