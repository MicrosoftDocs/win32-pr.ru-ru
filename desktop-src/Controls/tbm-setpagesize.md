---
title: Сообщение TBM_SETPAGESIZE (Коммктрл. h)
description: Задает число логических позиций, на которое ползунок TrackBar перемещается в ответ на ввод с клавиатуры, например клавиши или, или ввод с помощью мыши, например щелчки в канале TrackBar.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- Элементы управления Windows для TBM_SETPAGESIZE сообщений
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071854"
---
# <a name="tbm_setpagesize-message"></a><span data-ttu-id="24a50-104">\_Сообщение ТБМ SETPAGESIZE</span><span class="sxs-lookup"><span data-stu-id="24a50-104">TBM\_SETPAGESIZE message</span></span>

<span data-ttu-id="24a50-105">Задает число логических позиций, на которое ползунок TrackBar перемещается в ответ на ввод с клавиатуры, например клавиши или, или ввод с помощью мыши, например щелчки в канале TrackBar.</span><span class="sxs-lookup"><span data-stu-id="24a50-105">Sets the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="24a50-106">Логическое положение — это целое число, увеличивающееся в диапазоне значений TrackBar от минимума до максимальной позиции ползунка.</span><span class="sxs-lookup"><span data-stu-id="24a50-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="24a50-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="24a50-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a50-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24a50-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="24a50-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="24a50-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="24a50-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24a50-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24a50-111">Новый размер страницы.</span><span class="sxs-lookup"><span data-stu-id="24a50-111">New page size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a50-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24a50-112">Return value</span></span>

<span data-ttu-id="24a50-113">Возвращает 32-разрядное значение, указывающее размер предыдущей страницы.</span><span class="sxs-lookup"><span data-stu-id="24a50-113">Returns a 32-bit value that specifies the previous page size.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a50-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24a50-114">Remarks</span></span>

<span data-ttu-id="24a50-115">Эта линейка также отправляет сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) с \_ кодами уведомлений ТБ PageUp и ТБ \_ PageDown в родительское окно, когда оно получает ввод с клавиатуры или с помощью мыши для прокрутки страницы.</span><span class="sxs-lookup"><span data-stu-id="24a50-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a50-116">Требования</span><span class="sxs-lookup"><span data-stu-id="24a50-116">Requirements</span></span>



| <span data-ttu-id="24a50-117">Требование</span><span class="sxs-lookup"><span data-stu-id="24a50-117">Requirement</span></span> | <span data-ttu-id="24a50-118">Значение</span><span class="sxs-lookup"><span data-stu-id="24a50-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24a50-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24a50-119">Minimum supported client</span></span><br/> | <span data-ttu-id="24a50-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24a50-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24a50-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24a50-121">Minimum supported server</span></span><br/> | <span data-ttu-id="24a50-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24a50-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24a50-123">Header</span><span class="sxs-lookup"><span data-stu-id="24a50-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="24a50-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="24a50-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a50-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24a50-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a50-126">**ТБМая \_ pageSize**</span><span class="sxs-lookup"><span data-stu-id="24a50-126">**TBM\_GETPAGESIZE**</span></span>](tbm-getpagesize.md)
</dt> </dl>

 

 





