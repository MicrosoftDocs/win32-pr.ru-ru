---
title: Код уведомления EN_CORRECTTEXT (RichEdit. h)
description: Сообщает родительскому окну расширенного редактирования элемента управления, что Сив \_ правильный жест, давая родительскому окну возможность отменить исправление текста. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135215"
---
# <a name="en_correcttext-notification-code"></a><span data-ttu-id="fafe6-105">\_Код уведомления EN корректтекст</span><span class="sxs-lookup"><span data-stu-id="fafe6-105">EN\_CORRECTTEXT notification code</span></span>

<span data-ttu-id="fafe6-106">Сообщает родительскому окну расширенного редактирования элемента управления, что Сив \_ правильный жест, давая родительскому окну возможность отменить исправление текста.</span><span class="sxs-lookup"><span data-stu-id="fafe6-106">Notifies a rich edit control parent window that a SYV\_CORRECT gesture occurred, giving the parent window a chance to cancel correcting the text.</span></span> <span data-ttu-id="fafe6-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fafe6-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fafe6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fafe6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fafe6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fafe6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fafe6-110">Структура [**енкорректтекст**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) , указывающая выбор для исправления.</span><span class="sxs-lookup"><span data-stu-id="fafe6-110">An [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) structure specifying the selection to be corrected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fafe6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fafe6-111">Return value</span></span>

<span data-ttu-id="fafe6-112">Возвращает ноль, чтобы пропустить действие.</span><span class="sxs-lookup"><span data-stu-id="fafe6-112">Return zero to ignore the action.</span></span>

<span data-ttu-id="fafe6-113">Возвращает ненулевое значение для обработки действия.</span><span class="sxs-lookup"><span data-stu-id="fafe6-113">Returns a nonzero value to process the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="fafe6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fafe6-114">Remarks</span></span>

<span data-ttu-id="fafe6-115">Этот код уведомления отправляется, только если доступны возможности пера.</span><span class="sxs-lookup"><span data-stu-id="fafe6-115">This notification code is sent only if pen capabilities are available.</span></span>

<span data-ttu-id="fafe6-116">Чтобы получить \_ коды уведомлений EN корректтекст, укажите [**енм \_ корректтекст**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="fafe6-116">To receive EN\_CORRECTTEXT notification codes, specify [**ENM\_CORRECTTEXT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="fafe6-117">\_Код уведомления EN корректтекст поддерживается только в расширенном редактировании версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="fafe6-117">The EN\_CORRECTTEXT notification code is only supported in rich edit version 1.0.</span></span> <span data-ttu-id="fafe6-118">Он не поддерживается в более поздних версиях расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="fafe6-118">It is not supported in later versions of rich edit.</span></span> <span data-ttu-id="fafe6-119">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="fafe6-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fafe6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="fafe6-120">Requirements</span></span>



| <span data-ttu-id="fafe6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="fafe6-121">Requirement</span></span> | <span data-ttu-id="fafe6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="fafe6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fafe6-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fafe6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fafe6-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fafe6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fafe6-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fafe6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fafe6-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fafe6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fafe6-127">Header</span><span class="sxs-lookup"><span data-stu-id="fafe6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fafe6-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fafe6-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fafe6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fafe6-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="fafe6-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fafe6-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fafe6-131">**енкорректтекст**</span><span class="sxs-lookup"><span data-stu-id="fafe6-131">**ENCORRECTTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





