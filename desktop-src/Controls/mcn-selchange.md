---
title: Код уведомления MCN_SELCHANGE (Коммктрл. h)
description: Посылается элементом управления "месячный календарь" при изменении текущей выбранной даты или диапазона дат. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- MCN_SELCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071256"
---
# <a name="mcn_selchange-notification-code"></a><span data-ttu-id="68146-105">\_Код уведомления МКН селчанже</span><span class="sxs-lookup"><span data-stu-id="68146-105">MCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="68146-106">Посылается элементом управления "месячный календарь" при изменении текущей выбранной даты или диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="68146-106">Sent by a month calendar control when the currently selected date or range of dates changes.</span></span> <span data-ttu-id="68146-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="68146-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="68146-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="68146-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68146-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68146-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68146-110">Указатель на структуру [**нмселчанже**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) , содержащую сведения о выбранном в данный момент диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="68146-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68146-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68146-111">Return value</span></span>

<span data-ttu-id="68146-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="68146-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68146-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68146-113">Remarks</span></span>

<span data-ttu-id="68146-114">Например, элемент управления отправляет МКН \_ селчанже, когда пользователь явно изменяет выбор в течение текущего месяца или когда выбор изменяется неявно в ответ на переход на следующий или предыдущий месяц.</span><span class="sxs-lookup"><span data-stu-id="68146-114">For example, the control sends MCN\_SELCHANGE when the user explicitly changes the selection within the current month or when the selection is implicitly changed in response to next/previous month navigation.</span></span> <span data-ttu-id="68146-115">Этот код уведомления также отправляется системой через регулярные интервалы, чтобы элемент управления мог реагировать на изменения дат.</span><span class="sxs-lookup"><span data-stu-id="68146-115">This notification code is also sent by the system at regular intervals so that the control can respond to date changes.</span></span>

<span data-ttu-id="68146-116">Этот код уведомления аналогичен [МКН \_ SELECT](mcn-select.md), но отправляется в ответ на любое изменение выбора.</span><span class="sxs-lookup"><span data-stu-id="68146-116">This notification code is similar to [MCN\_SELECT](mcn-select.md), but it is sent in response to any selection change.</span></span> <span data-ttu-id="68146-117">МКН \_ SELECT отправляется только для явного выбора даты.</span><span class="sxs-lookup"><span data-stu-id="68146-117">MCN\_SELECT is sent only for an explicit date selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="68146-118">Требования</span><span class="sxs-lookup"><span data-stu-id="68146-118">Requirements</span></span>



| <span data-ttu-id="68146-119">Требование</span><span class="sxs-lookup"><span data-stu-id="68146-119">Requirement</span></span> | <span data-ttu-id="68146-120">Значение</span><span class="sxs-lookup"><span data-stu-id="68146-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68146-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68146-121">Minimum supported client</span></span><br/> | <span data-ttu-id="68146-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68146-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68146-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68146-123">Minimum supported server</span></span><br/> | <span data-ttu-id="68146-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68146-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68146-125">Header</span><span class="sxs-lookup"><span data-stu-id="68146-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="68146-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="68146-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





