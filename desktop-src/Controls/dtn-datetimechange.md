---
title: Код уведомления DTN_DATETIMECHANGE (Коммктрл. h)
description: Отправляется элементом управления "Выбор даты и времени" каждый раз, когда происходит изменение. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- DTN_DATETIMECHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892290"
---
# <a name="dtn_datetimechange-notification-code"></a><span data-ttu-id="aeb73-105">\_Код уведомления ДТН датетимечанже</span><span class="sxs-lookup"><span data-stu-id="aeb73-105">DTN\_DATETIMECHANGE notification code</span></span>

<span data-ttu-id="aeb73-106">Отправляется элементом управления "Выбор даты и времени" каждый раз, когда происходит изменение.</span><span class="sxs-lookup"><span data-stu-id="aeb73-106">Sent by a date and time picker (DTP) control whenever a change occurs.</span></span> <span data-ttu-id="aeb73-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="aeb73-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="aeb73-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aeb73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb73-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aeb73-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb73-110">Указатель на структуру [**нмдатетимечанже**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) , содержащую сведения об изменении, которое произошло в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="aeb73-110">A pointer to an [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) structure containing information about the change that took place in the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb73-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aeb73-111">Return value</span></span>

<span data-ttu-id="aeb73-112">Владелец элемента управления должен возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="aeb73-112">The owner of the control must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb73-113">Требования</span><span class="sxs-lookup"><span data-stu-id="aeb73-113">Requirements</span></span>



| <span data-ttu-id="aeb73-114">Требование</span><span class="sxs-lookup"><span data-stu-id="aeb73-114">Requirement</span></span> | <span data-ttu-id="aeb73-115">Значение</span><span class="sxs-lookup"><span data-stu-id="aeb73-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb73-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aeb73-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb73-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aeb73-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aeb73-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aeb73-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb73-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aeb73-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aeb73-120">Header</span><span class="sxs-lookup"><span data-stu-id="aeb73-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeb73-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeb73-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





