---
title: Код уведомления NM_KEYDOWN (Коммктрл. h)
description: NM_KEYDOWN код уведомления — отправляется элементом управления, когда элемент управления имеет фокус клавиатуры и пользователь нажимает клавишу. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- NM_KEYDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce595378995e41fd8a0f481d7470c8cf791f6379
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112352"
---
# <a name="nm_keydown-notification-code"></a><span data-ttu-id="d1ccc-105">\_Код уведомления NM KeyDown</span><span class="sxs-lookup"><span data-stu-id="d1ccc-105">NM\_KEYDOWN notification code</span></span>

<span data-ttu-id="d1ccc-106">Посылается элементом управления, когда элемент управления имеет фокус клавиатуры и пользователь нажимает клавишу.</span><span class="sxs-lookup"><span data-stu-id="d1ccc-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="d1ccc-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d1ccc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d1ccc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1ccc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1ccc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1ccc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1ccc-110">Указатель на структуру [**нмкэй**](/windows/win32/api/commctrl/ns-commctrl-nmkey) , которая содержит дополнительные сведения о ключе, вызвавшем код уведомления.</span><span class="sxs-lookup"><span data-stu-id="d1ccc-110">A pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1ccc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1ccc-111">Return value</span></span>

<span data-ttu-id="d1ccc-112">Возвращает ненулевое значение, чтобы элемент управления не обрабатывал ключ, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d1ccc-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1ccc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d1ccc-113">Requirements</span></span>



| <span data-ttu-id="d1ccc-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d1ccc-114">Requirement</span></span> | <span data-ttu-id="d1ccc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d1ccc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ccc-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1ccc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d1ccc-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1ccc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1ccc-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1ccc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d1ccc-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1ccc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1ccc-120">Header</span><span class="sxs-lookup"><span data-stu-id="d1ccc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1ccc-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ccc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





