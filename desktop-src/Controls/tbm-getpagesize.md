---
title: Сообщение TBM_GETPAGESIZE (Коммктрл. h)
description: Возвращает число логических позиций, на которое ползунок TrackBar перемещается в ответ на ввод с клавиатуры, например клавиши или, или ввод с помощью мыши, например щелчки в канале TrackBar.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- Элементы управления Windows для TBM_GETPAGESIZE сообщений
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac58c0b935b468cf8af565fba2db67c88418ee4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135950"
---
# <a name="tbm_getpagesize-message"></a><span data-ttu-id="7276c-104">Сообщение ТБМа \_ pageSize</span><span class="sxs-lookup"><span data-stu-id="7276c-104">TBM\_GETPAGESIZE message</span></span>

<span data-ttu-id="7276c-105">Возвращает число логических позиций, на которое ползунок TrackBar перемещается в ответ на ввод с клавиатуры, например клавиши или, или ввод с помощью мыши, например щелчки в канале TrackBar.</span><span class="sxs-lookup"><span data-stu-id="7276c-105">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="7276c-106">Логическое положение — это целое число, увеличивающееся в диапазоне значений TrackBar от минимума до максимальной позиции ползунка.</span><span class="sxs-lookup"><span data-stu-id="7276c-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="7276c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7276c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7276c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7276c-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7276c-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7276c-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7276c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7276c-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7276c-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7276c-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7276c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7276c-112">Return value</span></span>

<span data-ttu-id="7276c-113">Возвращает 32-разрядное значение, указывающее размер страницы для TrackBar.</span><span class="sxs-lookup"><span data-stu-id="7276c-113">Returns a 32-bit value that specifies the page size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="7276c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7276c-114">Remarks</span></span>

<span data-ttu-id="7276c-115">Эта линейка также отправляет сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) с \_ кодами уведомлений ТБ PageUp и ТБ \_ PageDown в родительское окно, когда оно получает ввод с клавиатуры или с помощью мыши для прокрутки страницы.</span><span class="sxs-lookup"><span data-stu-id="7276c-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="7276c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7276c-116">Requirements</span></span>



| <span data-ttu-id="7276c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7276c-117">Requirement</span></span> | <span data-ttu-id="7276c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7276c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7276c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7276c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7276c-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7276c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7276c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7276c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7276c-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7276c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7276c-123">Header</span><span class="sxs-lookup"><span data-stu-id="7276c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7276c-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7276c-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7276c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7276c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7276c-126">**ТБМ \_ SETPAGESIZE**</span><span class="sxs-lookup"><span data-stu-id="7276c-126">**TBM\_SETPAGESIZE**</span></span>](tbm-setpagesize.md)
</dt> </dl>

 

 





