---
title: Код уведомления RBN_LAYOUTCHANGED (Коммктрл. h)
description: Посылается элементом управления "Главная панель", когда пользователь изменяет макет полос элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e937d151-bfaa-41c0-a134-e70ff2f75d07
keywords:
- RBN_LAYOUTCHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_LAYOUTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1fc14578435fc786ecc5496cec96eb2224b4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136626"
---
# <a name="rbn_layoutchanged-notification-code"></a><span data-ttu-id="2535b-105">\_Код уведомления РБН лайаутчанжед</span><span class="sxs-lookup"><span data-stu-id="2535b-105">RBN\_LAYOUTCHANGED notification code</span></span>

<span data-ttu-id="2535b-106">Посылается элементом управления "Главная панель", когда пользователь изменяет макет полос элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2535b-106">Sent by a rebar control when the user changes the layout of the control's bands.</span></span> <span data-ttu-id="2535b-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2535b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_LAYOUTCHANGED 

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2535b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2535b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2535b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2535b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2535b-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="2535b-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2535b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2535b-111">Return value</span></span>

<span data-ttu-id="2535b-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="2535b-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2535b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2535b-113">Requirements</span></span>



| <span data-ttu-id="2535b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2535b-114">Requirement</span></span> | <span data-ttu-id="2535b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2535b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2535b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2535b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2535b-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2535b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2535b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2535b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2535b-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2535b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2535b-120">Header</span><span class="sxs-lookup"><span data-stu-id="2535b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2535b-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2535b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





