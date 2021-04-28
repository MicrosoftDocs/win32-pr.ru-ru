---
title: Сообщение TBM_SETPOSNOTIFY (Коммктрл. h)
description: TBM_SETPOSNOTIFY сообщение — задает текущую логическую точку ползунка в TrackBar.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- Элементы управления Windows для TBM_SETPOSNOTIFY сообщений
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7201f3056ed05e6321ab9d9bd726edc3b4470f0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104082"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="ac5cc-104">\_Сообщение ТБМ сетпоснотифи</span><span class="sxs-lookup"><span data-stu-id="ac5cc-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="ac5cc-105">Задает текущую логическую точку ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac5cc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac5cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac5cc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac5cc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac5cc-108">wParam не используется.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="ac5cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac5cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac5cc-110">Новое логическое положение ползунка.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-110">New logical position of the slider.</span></span> <span data-ttu-id="ac5cc-111">Допустимыми логическими позициями являются целочисленные значения в диапазоне значений TrackBar от минимума до максимальных позиций ползунка.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="ac5cc-112">Если это значение находится за пределами максимального и минимального значений элемента управления, то для этой должности устанавливается максимальное или минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac5cc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac5cc-113">Return value</span></span>

<span data-ttu-id="ac5cc-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac5cc-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="ac5cc-115">Remarks</span></span>

<span data-ttu-id="ac5cc-116">Вызов **ТБМ \_ сетпоснотифи** установит положение ползунка TrackBar, например [**ТБМ \_ сетпос**](tbm-setpos.md) , но также приведет к тому, что свойство TrackBar будет уведомлять его родителя перемещения через сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="ac5cc-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac5cc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ac5cc-117">Requirements</span></span>



| <span data-ttu-id="ac5cc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ac5cc-118">Requirement</span></span> | <span data-ttu-id="ac5cc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ac5cc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5cc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac5cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ac5cc-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ac5cc-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ac5cc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac5cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ac5cc-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac5cc-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ac5cc-124">Header</span><span class="sxs-lookup"><span data-stu-id="ac5cc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac5cc-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac5cc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





