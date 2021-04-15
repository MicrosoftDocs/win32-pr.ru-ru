---
title: Код уведомления RBN_SPLITTERDRAG (Коммктрл. h)
description: Посылается элементом управления "Главная панель", когда пользователь перетаскивает разделитель. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- RBN_SPLITTERDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_SPLITTERDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b2d3fc00433be9cd3011f2f2b24d515b8cbd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534655"
---
# <a name="rbn_splitterdrag-notification-code"></a><span data-ttu-id="50aa3-105">\_Код уведомления РБН сплиттердраг</span><span class="sxs-lookup"><span data-stu-id="50aa3-105">RBN\_SPLITTERDRAG notification code</span></span>

<span data-ttu-id="50aa3-106">Посылается элементом управления "Главная панель", когда пользователь перетаскивает разделитель.</span><span class="sxs-lookup"><span data-stu-id="50aa3-106">Sent by a rebar control when the user drags a splitter.</span></span> <span data-ttu-id="50aa3-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="50aa3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_SPLITTERDRAG

    lpnmrbspltr = (LPNMREBARSPLITTER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="50aa3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50aa3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50aa3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50aa3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50aa3-110">Указатель на структуру [**нмребарсплиттер**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="50aa3-110">Pointer to an [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50aa3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50aa3-111">Return value</span></span>

<span data-ttu-id="50aa3-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="50aa3-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="50aa3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="50aa3-113">Requirements</span></span>



| <span data-ttu-id="50aa3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="50aa3-114">Requirement</span></span> | <span data-ttu-id="50aa3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="50aa3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50aa3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50aa3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="50aa3-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50aa3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50aa3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50aa3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="50aa3-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50aa3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50aa3-120">Header</span><span class="sxs-lookup"><span data-stu-id="50aa3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="50aa3-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="50aa3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





