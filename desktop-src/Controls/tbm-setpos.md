---
title: Сообщение TBM_SETPOS (Коммктрл. h)
description: TBM_SETPOS сообщение — задает текущую логическую точку ползунка в TrackBar.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- Элементы управления Windows для TBM_SETPOS сообщений
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f10e05a677119f18489d0eb9eebc4528d3ad115
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085872"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="b12c3-104">\_Сообщение ТБМ сетпос</span><span class="sxs-lookup"><span data-stu-id="b12c3-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="b12c3-105">Задает текущую логическую точку ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b12c3-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b12c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b12c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b12c3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b12c3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b12c3-108">Флаг перерисовки.</span><span class="sxs-lookup"><span data-stu-id="b12c3-108">Redraw flag.</span></span> <span data-ttu-id="b12c3-109">Если этот параметр имеет **значение true**, сообщение перерисовывается ползунком в позиции, заданной аргументом *lParam*.</span><span class="sxs-lookup"><span data-stu-id="b12c3-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="b12c3-110">Если этот параметр имеет **значение false**, сообщение не перерисовывает ползунок в новой позиции.</span><span class="sxs-lookup"><span data-stu-id="b12c3-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="b12c3-111">Обратите внимание, что сообщение задает значение положения ползунка (как оно возвращается в сообщении [**ТБМ \_ жетпос**](tbm-getpos.md) ) независимо от параметра *wParam* .</span><span class="sxs-lookup"><span data-stu-id="b12c3-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b12c3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b12c3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b12c3-113">Новое логическое положение ползунка.</span><span class="sxs-lookup"><span data-stu-id="b12c3-113">New logical position of the slider.</span></span> <span data-ttu-id="b12c3-114">Допустимыми логическими позициями являются целочисленные значения в диапазоне значений TrackBar от минимума до максимальных позиций ползунка.</span><span class="sxs-lookup"><span data-stu-id="b12c3-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="b12c3-115">Если это значение находится за пределами максимального и минимального значений элемента управления, то для этой должности устанавливается максимальное или минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="b12c3-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b12c3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b12c3-116">Return value</span></span>

<span data-ttu-id="b12c3-117">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="b12c3-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b12c3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b12c3-118">Requirements</span></span>



| <span data-ttu-id="b12c3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b12c3-119">Requirement</span></span> | <span data-ttu-id="b12c3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b12c3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b12c3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b12c3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b12c3-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b12c3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b12c3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b12c3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b12c3-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b12c3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b12c3-125">Header</span><span class="sxs-lookup"><span data-stu-id="b12c3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b12c3-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b12c3-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





