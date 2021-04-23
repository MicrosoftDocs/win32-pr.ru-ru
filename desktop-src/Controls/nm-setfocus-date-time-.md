---
title: Код уведомления NM_SETFOCUS (Дата и время) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Выбор даты и времени", что элемент управления получил фокус ввода. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 61c62fb2-bc79-404b-9958-7208d1c781fa
keywords:
- NM_SETFOCUS (Дата и время) коды уведомлений элементы управления Windows
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba80ea119056c131f1dd94cdf1f39a84371b7052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489960"
---
# <a name="nm_setfocus-date-time-notification-code"></a><span data-ttu-id="6a3f3-105">\_Код уведомления для NM (Дата и время)</span><span class="sxs-lookup"><span data-stu-id="6a3f3-105">NM\_SETFOCUS (date time) notification code</span></span>

<span data-ttu-id="6a3f3-106">Сообщает родительскому окну элемента управления "Выбор даты и времени", что элемент управления получил фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-106">Notifies a date and time picker control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="6a3f3-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6a3f3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6a3f3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a3f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a3f3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a3f3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a3f3-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a3f3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a3f3-111">Return value</span></span>

<span data-ttu-id="6a3f3-112">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6a3f3-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a3f3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6a3f3-113">Requirements</span></span>



| <span data-ttu-id="6a3f3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6a3f3-114">Requirement</span></span> | <span data-ttu-id="6a3f3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6a3f3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a3f3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a3f3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a3f3-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a3f3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a3f3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a3f3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a3f3-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a3f3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a3f3-120">Header</span><span class="sxs-lookup"><span data-stu-id="6a3f3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a3f3-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a3f3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





