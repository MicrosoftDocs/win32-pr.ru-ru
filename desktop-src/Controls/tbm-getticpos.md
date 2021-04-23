---
title: Сообщение TBM_GETTICPOS (Коммктрл. h)
description: Извлекает текущее физическое расположение деления в TrackBar.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- Элементы управления Windows для TBM_GETTICPOS сообщений
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654513"
---
# <a name="tbm_getticpos-message"></a><span data-ttu-id="40795-104">\_Сообщение ТБМ жеттикпос</span><span class="sxs-lookup"><span data-stu-id="40795-104">TBM\_GETTICPOS message</span></span>

<span data-ttu-id="40795-105">Извлекает текущее физическое расположение деления в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="40795-105">Retrieves the current physical position of a tick mark in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="40795-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="40795-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40795-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40795-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40795-108">Отсчитываемый от нуля индекс, указывающий деление.</span><span class="sxs-lookup"><span data-stu-id="40795-108">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="40795-109">Позиции первой и последней делений не доступны напрямую через это сообщение.</span><span class="sxs-lookup"><span data-stu-id="40795-109">The positions of the first and last tick marks are not directly available via this message.</span></span>

</dd> <dt>

<span data-ttu-id="40795-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40795-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40795-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="40795-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40795-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40795-112">Return value</span></span>

<span data-ttu-id="40795-113">Возвращает расстояние в клиентских координатах от левого или верхнего края клиентской области TrackBar до указанного деления.</span><span class="sxs-lookup"><span data-stu-id="40795-113">Returns the distance, in client coordinates, from the left or top of the trackbar's client area to the specified tick mark.</span></span> <span data-ttu-id="40795-114">Возвращаемое значение — это координата x деления горизонтальной линейки или координаты y для вертикальной линейки.</span><span class="sxs-lookup"><span data-stu-id="40795-114">The return value is the x-coordinate of the tick mark for a horizontal trackbar or the y-coordinate for a vertical trackbar.</span></span> <span data-ttu-id="40795-115">Если параметр *wParam* не является допустимым индексом, возвращается значение-1.</span><span class="sxs-lookup"><span data-stu-id="40795-115">If *wParam* is not a valid index, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="40795-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40795-116">Remarks</span></span>

<span data-ttu-id="40795-117">Поскольку первая и последняя деления недоступны через это сообщение, допустимые индексы смещаются относительно их позиции на TrackBar.</span><span class="sxs-lookup"><span data-stu-id="40795-117">Because the first and last tick marks are not available through this message, valid indexes are offset from their tick position on the trackbar.</span></span> <span data-ttu-id="40795-118">Если разница между [**ТБМ \_ Жетранжемин**](tbm-getrangemin.md) и [**ТБМ \_ жетранжемакс**](tbm-getrangemax.md) меньше двух, то допустимый индекс отсутствует, и это сообщение не будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="40795-118">If the difference between [**TBM\_GETRANGEMIN**](tbm-getrangemin.md) and [**TBM\_GETRANGEMAX**](tbm-getrangemax.md) is less than two, then there is no valid index and this message will fail.</span></span>

<span data-ttu-id="40795-119">Ниже показано отношение между тактами на TrackBar, тактами, доступными через это сообщение, и индексами, начинающимися с нуля.</span><span class="sxs-lookup"><span data-stu-id="40795-119">The following illustrates the relation between the ticks on a trackbar, the ticks available through this message, and their zero-based indexes.</span></span>

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a><span data-ttu-id="40795-120">Требования</span><span class="sxs-lookup"><span data-stu-id="40795-120">Requirements</span></span>



| <span data-ttu-id="40795-121">Требование</span><span class="sxs-lookup"><span data-stu-id="40795-121">Requirement</span></span> | <span data-ttu-id="40795-122">Значение</span><span class="sxs-lookup"><span data-stu-id="40795-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40795-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40795-123">Minimum supported client</span></span><br/> | <span data-ttu-id="40795-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="40795-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40795-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40795-125">Minimum supported server</span></span><br/> | <span data-ttu-id="40795-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="40795-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40795-127">Header</span><span class="sxs-lookup"><span data-stu-id="40795-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="40795-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="40795-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





