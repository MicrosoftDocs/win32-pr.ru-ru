---
title: Код уведомления EN_DRAGDROPDONE (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что операция перетаскивания завершена. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- EN_DRAGDROPDONE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10b6718122791bcc862866fbaf17ed43e8bfd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988242"
---
# <a name="en_dragdropdone-notification-code"></a><span data-ttu-id="3adcf-105">\_Код уведомления EN драгдропдоне</span><span class="sxs-lookup"><span data-stu-id="3adcf-105">EN\_DRAGDROPDONE notification code</span></span>

<span data-ttu-id="3adcf-106">Сообщает родительскому окну элемента управления Rich Edit, что операция перетаскивания завершена.</span><span class="sxs-lookup"><span data-stu-id="3adcf-106">Notifies a rich edit control's parent window that the drag-and-drop operation has completed.</span></span> <span data-ttu-id="3adcf-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3adcf-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3adcf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3adcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3adcf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3adcf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3adcf-110">Структура [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="3adcf-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3adcf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3adcf-111">Return value</span></span>

<span data-ttu-id="3adcf-112">Этот код уведомления не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3adcf-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3adcf-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3adcf-113">Remarks</span></span>

<span data-ttu-id="3adcf-114">Чтобы получить \_ код уведомления EN драгдропдоне, укажите флаг [**енм \_ драгдропдоне**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="3adcf-114">To receive an EN\_DRAGDROPDONE notification code, specify the [**ENM\_DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3adcf-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3adcf-115">Requirements</span></span>



| <span data-ttu-id="3adcf-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3adcf-116">Requirement</span></span> | <span data-ttu-id="3adcf-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3adcf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3adcf-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3adcf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3adcf-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3adcf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3adcf-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3adcf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3adcf-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3adcf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3adcf-122">Header</span><span class="sxs-lookup"><span data-stu-id="3adcf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3adcf-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3adcf-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3adcf-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3adcf-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="3adcf-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3adcf-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3adcf-126">**EM \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="3adcf-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> </dl>

 

 





