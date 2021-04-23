---
title: Системмонитор. Онкаунтерделетед, событие
description: Уведомляет вас перед удалением счетчика из коллекции счетчиков.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Сисмон события Онкаунтерделетед
- Онкаунтерделетед Event Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, событие Онкаунтерделетед
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988708"
---
# <a name="systemmonitoroncounterdeleted-event"></a><span data-ttu-id="c7fc6-106">Системмонитор. Онкаунтерделетед, событие</span><span class="sxs-lookup"><span data-stu-id="c7fc6-106">SystemMonitor.OnCounterDeleted event</span></span>

<span data-ttu-id="c7fc6-107">Уведомляет вас перед удалением счетчика из коллекции [**счетчиков**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="c7fc6-107">Notifies you before a counter is deleted from the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fc6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7fc6-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="c7fc6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7fc6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7fc6-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7fc6-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fc6-111">Индекс удаляемого счетчика из объекта коллекции [**счетчиков**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="c7fc6-111">Index of the counter to be deleted from the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7fc6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7fc6-112">Return value</span></span>

<span data-ttu-id="c7fc6-113">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c7fc6-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fc6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c7fc6-114">Requirements</span></span>



| <span data-ttu-id="c7fc6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c7fc6-115">Requirement</span></span> | <span data-ttu-id="c7fc6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c7fc6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fc6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7fc6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c7fc6-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c7fc6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c7fc6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7fc6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c7fc6-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c7fc6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7fc6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c7fc6-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7fc6-122"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc6-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fc6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7fc6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fc6-124">**Системмонитор. Онкаунтераддед**</span><span class="sxs-lookup"><span data-stu-id="c7fc6-124">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="c7fc6-125">**Системмонитор. Онкаунтерселектед**</span><span class="sxs-lookup"><span data-stu-id="c7fc6-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





