---
title: Код уведомления MCN_SELECT (Коммктрл. h)
description: Посылается элементом управления "месячный календарь", когда пользователь делает явный выбор даты в элементе управления "месячный календарь". Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071255"
---
# <a name="mcn_select-notification-code"></a><span data-ttu-id="930e4-105">МКН \_ Выбор кода уведомления</span><span class="sxs-lookup"><span data-stu-id="930e4-105">MCN\_SELECT notification code</span></span>

<span data-ttu-id="930e4-106">Посылается элементом управления "месячный календарь", когда пользователь делает явный выбор даты в элементе управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="930e4-106">Sent by a month calendar control when the user makes an explicit date selection within a month calendar control.</span></span> <span data-ttu-id="930e4-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="930e4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="930e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="930e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="930e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="930e4-110">Указатель на структуру [**нмселчанже**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) , содержащую сведения о выбранном в данный момент диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="930e4-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930e4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="930e4-111">Return value</span></span>

<span data-ttu-id="930e4-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="930e4-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="930e4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="930e4-113">Remarks</span></span>

<span data-ttu-id="930e4-114">Код **МКН \_ SELECT** уведомления аналогичен [**МКН \_ селчанже**](mcn-selchange.md), но **МКН \_ SELECT** отправляется только в ответ на явно выбранные даты пользователя.</span><span class="sxs-lookup"><span data-stu-id="930e4-114">The **MCN\_SELECT** notification code is similar to [**MCN\_SELCHANGE**](mcn-selchange.md), but **MCN\_SELECT** is sent only in response to a user's explicit date selections.</span></span> <span data-ttu-id="930e4-115">**МКН \_ СЕЛЧАНЖЕ** применяется к любому изменению выбора.</span><span class="sxs-lookup"><span data-stu-id="930e4-115">**MCN\_SELCHANGE** applies to any selection change.</span></span>

## <a name="requirements"></a><span data-ttu-id="930e4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="930e4-116">Requirements</span></span>



| <span data-ttu-id="930e4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="930e4-117">Requirement</span></span> | <span data-ttu-id="930e4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="930e4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="930e4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="930e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="930e4-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="930e4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="930e4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="930e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="930e4-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="930e4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="930e4-123">Header</span><span class="sxs-lookup"><span data-stu-id="930e4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="930e4-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="930e4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





