---
title: Код уведомления NM_KILLFOCUS (Дата и время) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Выбор даты и времени", что элемент управления потерял фокус ввода. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 33d6b88b-9608-4227-a822-1dc7a77d3a3f
keywords:
- NM_KILLFOCUS (Дата и время) коды уведомлений элементы управления Windows
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af47dca130d1025341e2a3c625c1bf7a9c44c42a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988191"
---
# <a name="nm_killfocus-date-time-notification-code"></a><span data-ttu-id="fa494-105">\_Код уведомления NM киллфокус (Дата и время)</span><span class="sxs-lookup"><span data-stu-id="fa494-105">NM\_KILLFOCUS (date time) notification code</span></span>

<span data-ttu-id="fa494-106">Сообщает родительскому окну элемента управления "Выбор даты и времени", что элемент управления потерял фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="fa494-106">Notifies a date and time picker control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="fa494-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fa494-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fa494-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa494-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa494-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa494-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa494-110">Адрес структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащей дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="fa494-110">The address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa494-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa494-111">Return value</span></span>

<span data-ttu-id="fa494-112">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fa494-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa494-113">Требования</span><span class="sxs-lookup"><span data-stu-id="fa494-113">Requirements</span></span>



| <span data-ttu-id="fa494-114">Требование</span><span class="sxs-lookup"><span data-stu-id="fa494-114">Requirement</span></span> | <span data-ttu-id="fa494-115">Значение</span><span class="sxs-lookup"><span data-stu-id="fa494-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa494-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa494-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fa494-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa494-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa494-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa494-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fa494-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa494-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa494-120">Header</span><span class="sxs-lookup"><span data-stu-id="fa494-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa494-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa494-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





