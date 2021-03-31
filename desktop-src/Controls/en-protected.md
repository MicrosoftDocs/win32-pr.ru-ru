---
title: Код уведомления EN_PROTECTED (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что пользователь предпринимает действие, которое изменит защищенный диапазон текста. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- EN_PROTECTED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490869"
---
# <a name="en_protected-notification-code"></a><span data-ttu-id="f2582-105">\_Код уведомления, защищенного коротким кодом</span><span class="sxs-lookup"><span data-stu-id="f2582-105">EN\_PROTECTED notification code</span></span>

<span data-ttu-id="f2582-106">Сообщает родительскому окну элемента управления Rich Edit, что пользователь предпринимает действие, которое изменит защищенный диапазон текста.</span><span class="sxs-lookup"><span data-stu-id="f2582-106">Notifies a rich edit control's parent window that the user is taking an action that would change a protected range of text.</span></span> <span data-ttu-id="f2582-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f2582-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f2582-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2582-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2582-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2582-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2582-110">Структура [**енпротектед**](/windows/desktop/api/Richedit/ns-richedit-enprotected) , содержащая сведения о сообщении, вызвавшем код уведомления.</span><span class="sxs-lookup"><span data-stu-id="f2582-110">An [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure containing information about the message that triggered the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2582-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2582-111">Return value</span></span>

<span data-ttu-id="f2582-112">Возвращает ноль, чтобы разрешить операцию.</span><span class="sxs-lookup"><span data-stu-id="f2582-112">Return zero to allow the operation.</span></span>

<span data-ttu-id="f2582-113">Чтобы предотвратить операцию, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f2582-113">Return a nonzero value to prevent the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2582-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2582-114">Remarks</span></span>

<span data-ttu-id="f2582-115">Если возвращается ноль и члены **MSG**, **wParam** и **lParam** структуры [**енпротектед**](/windows/desktop/api/Richedit/ns-richedit-enprotected) изменяются, элемент управления обрабатывает измененное сообщение, а не исходное сообщение.</span><span class="sxs-lookup"><span data-stu-id="f2582-115">If zero is returned and the **msg**, **wParam**, and **lParam** members of the [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure are changed, the control processes the revised message instead of the original message.</span></span>

<span data-ttu-id="f2582-116">Чтобы получить \_ коды уведомлений, защищенные с помощью короткого стандарта, укажите [**енм, \_ защищенный**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="f2582-116">To receive EN\_PROTECTED notification codes, specify [**ENM\_PROTECTED**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2582-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f2582-117">Requirements</span></span>



| <span data-ttu-id="f2582-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f2582-118">Requirement</span></span> | <span data-ttu-id="f2582-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f2582-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2582-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2582-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f2582-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2582-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2582-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2582-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f2582-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2582-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2582-124">Header</span><span class="sxs-lookup"><span data-stu-id="f2582-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2582-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2582-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2582-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2582-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2582-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f2582-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f2582-128">**енпротектед**</span><span class="sxs-lookup"><span data-stu-id="f2582-128">**ENPROTECTED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[<span data-ttu-id="f2582-129">**\_уведомление WM**</span><span class="sxs-lookup"><span data-stu-id="f2582-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





