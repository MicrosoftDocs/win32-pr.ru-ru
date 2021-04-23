---
title: Код уведомления EN_LOWFIRTF (RichEdit. h)
description: Сообщает родительскому окну элемента управления Microsoft Rich Edit, что было получено Неподдерживаемое ключевое слово формата RTF. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74a6e5dada471fdd8364b34bf2ed1b4da7f2314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535048"
---
# <a name="en_lowfirtf-notification-code"></a><span data-ttu-id="ce8bc-105">\_Код уведомления EN ловфиртф</span><span class="sxs-lookup"><span data-stu-id="ce8bc-105">EN\_LOWFIRTF notification code</span></span>

<span data-ttu-id="ce8bc-106">Сообщает родительскому окну элемента управления Microsoft Rich Edit, что было получено Неподдерживаемое ключевое слово формата RTF.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-106">Notifies the parent window of a Microsoft Rich Edit control that an unsupported Rich Text Format (RTF) keyword was received.</span></span> <span data-ttu-id="ce8bc-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ce8bc-107">A Rich Edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ce8bc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce8bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce8bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce8bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce8bc-110">Структура [**енловфиртф**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) .</span><span class="sxs-lookup"><span data-stu-id="ce8bc-110">The [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce8bc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce8bc-111">Return value</span></span>

<span data-ttu-id="ce8bc-112">Этот код уведомления не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ce8bc-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce8bc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce8bc-113">Remarks</span></span>

<span data-ttu-id="ce8bc-114">Чтобы получить уведомление EN \_ ловфиртф, укажите \_ флаг енм ловфиртф в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="ce8bc-114">To receive an EN\_LOWFIRTF notification, specify the ENM\_LOWFIRTF flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce8bc-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ce8bc-115">Requirements</span></span>



| <span data-ttu-id="ce8bc-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ce8bc-116">Requirement</span></span> | <span data-ttu-id="ce8bc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ce8bc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce8bc-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce8bc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ce8bc-119">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce8bc-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce8bc-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce8bc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ce8bc-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce8bc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce8bc-122">Header</span><span class="sxs-lookup"><span data-stu-id="ce8bc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce8bc-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce8bc-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce8bc-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce8bc-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce8bc-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ce8bc-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ce8bc-126">**енловфиртф**</span><span class="sxs-lookup"><span data-stu-id="ce8bc-126">**ENLOWFIRTF**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[<span data-ttu-id="ce8bc-127">**\_уведомление WM**</span><span class="sxs-lookup"><span data-stu-id="ce8bc-127">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





