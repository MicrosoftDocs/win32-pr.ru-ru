---
title: Сообщение TTM_TRACKACTIVATE (Коммктрл. h)
description: Активирует или деактивирует подсказку отслеживания.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- Элементы управления Windows для TTM_TRACKACTIVATE сообщений
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988901"
---
# <a name="ttm_trackactivate-message"></a><span data-ttu-id="ddd8b-104">\_Сообщение ТТМ траккактивате</span><span class="sxs-lookup"><span data-stu-id="ddd8b-104">TTM\_TRACKACTIVATE message</span></span>

<span data-ttu-id="ddd8b-105">Активирует или деактивирует подсказку отслеживания.</span><span class="sxs-lookup"><span data-stu-id="ddd8b-105">Activates or deactivates a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="ddd8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddd8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddd8b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ddd8b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddd8b-108">Значение, указывающее, активируется или деактивируется отслеживание.</span><span class="sxs-lookup"><span data-stu-id="ddd8b-108">Value specifying whether tracking is being activated or deactivated.</span></span> <span data-ttu-id="ddd8b-109">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="ddd8b-109">This value can be one of the following:</span></span>



| <span data-ttu-id="ddd8b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd8b-110">Value</span></span>                                                                                                                                | <span data-ttu-id="ddd8b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd8b-111">Meaning</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="ddd8b-112"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="ddd8b-112"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="ddd8b-113">Активация отслеживания.</span><span class="sxs-lookup"><span data-stu-id="ddd8b-113">Activate tracking.</span></span><br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="ddd8b-114"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="ddd8b-114"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="ddd8b-115">Отключить отслеживание.</span><span class="sxs-lookup"><span data-stu-id="ddd8b-115">Deactivate tracking.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ddd8b-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ddd8b-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddd8b-117">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , определяющую инструмент, к которому применяется это сообщение.</span><span class="sxs-lookup"><span data-stu-id="ddd8b-117">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that identifies the tool to which this message applies.</span></span> <span data-ttu-id="ddd8b-118">Элементы **HWND** и **uId** определяют средство, а член **кбсизе** задает размер структуры.</span><span class="sxs-lookup"><span data-stu-id="ddd8b-118">The **hwnd** and **uId** members identify the tool, and the **cbSize** member specifies the size of the structure.</span></span> <span data-ttu-id="ddd8b-119">Все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="ddd8b-119">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddd8b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddd8b-120">Return value</span></span>

<span data-ttu-id="ddd8b-121">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="ddd8b-121">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddd8b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ddd8b-122">Requirements</span></span>



| <span data-ttu-id="ddd8b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ddd8b-123">Requirement</span></span> | <span data-ttu-id="ddd8b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd8b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd8b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddd8b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd8b-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ddd8b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ddd8b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddd8b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd8b-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ddd8b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ddd8b-129">Header</span><span class="sxs-lookup"><span data-stu-id="ddd8b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddd8b-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddd8b-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddd8b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddd8b-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="ddd8b-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ddd8b-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ddd8b-133">**ТТМ \_ траккпоситион**</span><span class="sxs-lookup"><span data-stu-id="ddd8b-133">**TTM\_TRACKPOSITION**</span></span>](ttm-trackposition.md)
</dt> <dt>

<span data-ttu-id="ddd8b-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ddd8b-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ddd8b-135">Использование элементов управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="ddd8b-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 





