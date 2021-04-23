---
title: Системмонитор. Онкаунтерселектед, событие
description: Уведомляет вас о том, что выбран счетчик.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Сисмон события Онкаунтерселектед
- Онкаунтерселектед Event Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, событие Онкаунтерселектед
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661912"
---
# <a name="systemmonitoroncounterselected-event"></a><span data-ttu-id="ee779-106">Системмонитор. Онкаунтерселектед, событие</span><span class="sxs-lookup"><span data-stu-id="ee779-106">SystemMonitor.OnCounterSelected event</span></span>

<span data-ttu-id="ee779-107">Уведомляет вас о том, что выбран счетчик.</span><span class="sxs-lookup"><span data-stu-id="ee779-107">Notifies you when a counter is selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee779-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee779-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="ee779-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee779-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee779-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee779-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee779-111">Индекс выбранного счетчика в объекте коллекции [**счетчиков**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="ee779-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee779-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee779-112">Return value</span></span>

<span data-ttu-id="ee779-113">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ee779-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee779-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee779-114">Remarks</span></span>

<span data-ttu-id="ee779-115">Это событие можно получить, когда</span><span class="sxs-lookup"><span data-stu-id="ee779-115">You can receive this event when</span></span>

-   <span data-ttu-id="ee779-116">Вы устанавливаете [**каунтеритем. Selected**](counteritem-selected.md) в значение true.</span><span class="sxs-lookup"><span data-stu-id="ee779-116">You set [**CounterItem.Selected**](counteritem-selected.md) to True</span></span>
-   <span data-ttu-id="ee779-117">Пользователь выбирает счетчик в условных обозначениях</span><span class="sxs-lookup"><span data-stu-id="ee779-117">The user selects a counter in the Legend</span></span>
-   <span data-ttu-id="ee779-118">Пользователь дважды щелкает счетчик в условных обозначениях</span><span class="sxs-lookup"><span data-stu-id="ee779-118">The user double-clicks on a counter in the Legend</span></span>

## <a name="requirements"></a><span data-ttu-id="ee779-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ee779-119">Requirements</span></span>



| <span data-ttu-id="ee779-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ee779-120">Requirement</span></span> | <span data-ttu-id="ee779-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ee779-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee779-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee779-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ee779-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee779-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ee779-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee779-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ee779-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee779-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee779-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ee779-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee779-127"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ee779-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee779-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee779-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee779-129">**Системмонитор. Онкаунтераддед**</span><span class="sxs-lookup"><span data-stu-id="ee779-129">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="ee779-130">**Системмонитор. Онкаунтерделетед**</span><span class="sxs-lookup"><span data-stu-id="ee779-130">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





