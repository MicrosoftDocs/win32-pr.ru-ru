---
title: Код уведомления EN_SAVECLIPBOARD (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что элемент управления закрывается, а буфер обмена содержит сведения. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- EN_SAVECLIPBOARD кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891789"
---
# <a name="en_saveclipboard-notification-code"></a><span data-ttu-id="7785b-105">\_Код уведомления EN савеклипбоард</span><span class="sxs-lookup"><span data-stu-id="7785b-105">EN\_SAVECLIPBOARD notification code</span></span>

<span data-ttu-id="7785b-106">Сообщает родительскому окну элемента управления Rich Edit, что элемент управления закрывается, а буфер обмена содержит сведения.</span><span class="sxs-lookup"><span data-stu-id="7785b-106">Notifies the rich edit control's parent window that the control is closing and the clipboard contains information.</span></span> <span data-ttu-id="7785b-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7785b-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7785b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7785b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7785b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7785b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7785b-110">Структура [**енсавеклипбоард**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) , содержащая сведения о содержимом буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="7785b-110">An [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) structure that contains information about clipboard information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7785b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7785b-111">Return value</span></span>

<span data-ttu-id="7785b-112">Возвращает нуль, если буфер обмена должен быть доступен другим приложениям.</span><span class="sxs-lookup"><span data-stu-id="7785b-112">Return zero if the clipboard should be made available to other applications.</span></span>

<span data-ttu-id="7785b-113">Если буфер обмена не должен сохраняться, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7785b-113">Return a nonzero value if the clipboard should not be saved.</span></span>

## <a name="remarks"></a><span data-ttu-id="7785b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7785b-114">Remarks</span></span>

<span data-ttu-id="7785b-115">Родительское окно всегда будет получать сообщение [**WM \_ Notify**](wm-notify.md) для этого события, оно не требует отправки маски уведомления с [**\_ SETEVENTMASK EM**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="7785b-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7785b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7785b-116">Requirements</span></span>



| <span data-ttu-id="7785b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7785b-117">Requirement</span></span> | <span data-ttu-id="7785b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7785b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7785b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7785b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7785b-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7785b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7785b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7785b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7785b-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7785b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7785b-123">Header</span><span class="sxs-lookup"><span data-stu-id="7785b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7785b-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7785b-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7785b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7785b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="7785b-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7785b-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7785b-127">**енсавеклипбоард**</span><span class="sxs-lookup"><span data-stu-id="7785b-127">**ENSAVECLIPBOARD**</span></span>](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





