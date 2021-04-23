---
title: Сообщение TBM_GETLINESIZE (Коммктрл. h)
description: Возвращает число логических позиций, на которое ползунок TrackBar перемещается в ответ на ввод с клавиатуры клавиш со стрелками, например клавиши или. Логическое положение — это целое число, увеличивающееся в диапазоне значений TrackBar от минимума до максимальной позиции ползунка.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- Элементы управления Windows для TBM_GETLINESIZE сообщений
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86eb103f34461e545f5a9f56148c48364d880dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989431"
---
# <a name="tbm_getlinesize-message"></a><span data-ttu-id="a8b48-105">\_Сообщение ТБМ жетлинесизе</span><span class="sxs-lookup"><span data-stu-id="a8b48-105">TBM\_GETLINESIZE message</span></span>

<span data-ttu-id="a8b48-106">Возвращает число логических позиций, на которое ползунок TrackBar перемещается в ответ на ввод с клавиатуры клавиш со стрелками, например клавиши или.</span><span class="sxs-lookup"><span data-stu-id="a8b48-106">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="a8b48-107">Логическое положение — это целое число, увеличивающееся в диапазоне значений TrackBar от минимума до максимальной позиции ползунка.</span><span class="sxs-lookup"><span data-stu-id="a8b48-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8b48-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8b48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b48-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8b48-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a8b48-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a8b48-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a8b48-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8b48-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a8b48-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a8b48-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b48-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8b48-113">Return value</span></span>

<span data-ttu-id="a8b48-114">Возвращает 32-разрядное значение, указывающее размер строки для TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a8b48-114">Returns a 32-bit value that specifies the line size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8b48-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8b48-115">Remarks</span></span>

<span data-ttu-id="a8b48-116">Значение по умолчанию для параметра Размер линии равно 1.</span><span class="sxs-lookup"><span data-stu-id="a8b48-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="a8b48-117">Эта линейка также отправляет сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) с \_ кодами уведомлений ТБ и ТБ \_ линедовн в родительское окно, когда пользователь нажимает клавиши со стрелками.</span><span class="sxs-lookup"><span data-stu-id="a8b48-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b48-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a8b48-118">Requirements</span></span>



| <span data-ttu-id="a8b48-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a8b48-119">Requirement</span></span> | <span data-ttu-id="a8b48-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a8b48-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b48-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8b48-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b48-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8b48-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8b48-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8b48-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b48-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8b48-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8b48-125">Header</span><span class="sxs-lookup"><span data-stu-id="a8b48-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b48-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b48-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





