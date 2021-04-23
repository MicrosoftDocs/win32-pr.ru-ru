---
title: Сообщение TBM_SETPOSNOTIFY (Коммктрл. h)
description: Задает текущую логическую точку ползунка в TrackBar.
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
ms.openlocfilehash: 636a2add9f13470a89b312450f1a3dcbc185be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489804"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="106cf-104">\_Сообщение ТБМ сетпоснотифи</span><span class="sxs-lookup"><span data-stu-id="106cf-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="106cf-105">Задает текущую логическую точку ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="106cf-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="106cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="106cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="106cf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="106cf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="106cf-108">wParam не используется.</span><span class="sxs-lookup"><span data-stu-id="106cf-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="106cf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="106cf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="106cf-110">Новое логическое положение ползунка.</span><span class="sxs-lookup"><span data-stu-id="106cf-110">New logical position of the slider.</span></span> <span data-ttu-id="106cf-111">Допустимыми логическими позициями являются целочисленные значения в диапазоне значений TrackBar от минимума до максимальных позиций ползунка.</span><span class="sxs-lookup"><span data-stu-id="106cf-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="106cf-112">Если это значение находится за пределами максимального и минимального значений элемента управления, то для этой должности устанавливается максимальное или минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="106cf-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="106cf-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="106cf-113">Return value</span></span>

<span data-ttu-id="106cf-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="106cf-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="106cf-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="106cf-115">Remarks</span></span>

<span data-ttu-id="106cf-116">Вызов **ТБМ \_ сетпоснотифи** установит положение ползунка TrackBar, например [**ТБМ \_ сетпос**](tbm-setpos.md) , но также приведет к тому, что свойство TrackBar будет уведомлять его родителя перемещения через сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="106cf-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="106cf-117">Требования</span><span class="sxs-lookup"><span data-stu-id="106cf-117">Requirements</span></span>



| <span data-ttu-id="106cf-118">Требование</span><span class="sxs-lookup"><span data-stu-id="106cf-118">Requirement</span></span> | <span data-ttu-id="106cf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="106cf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="106cf-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="106cf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="106cf-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="106cf-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="106cf-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="106cf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="106cf-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="106cf-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="106cf-124">Header</span><span class="sxs-lookup"><span data-stu-id="106cf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="106cf-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="106cf-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





