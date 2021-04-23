---
title: Сообщение TBM_GETSELSTART (Коммктрл. h)
description: Получает начальную точку текущего диапазона выбора в TrackBar.
ms.assetid: 0000df2a-c40d-40c2-b120-e5d4fe6c5016
keywords:
- Элементы управления Windows для TBM_GETSELSTART сообщений
topic_type:
- apiref
api_name:
- TBM_GETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af796c57adb3615241a8f5b702ff58062468509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654514"
---
# <a name="tbm_getselstart-message"></a><span data-ttu-id="dd843-104">\_Сообщение ТБМ жетселстарт</span><span class="sxs-lookup"><span data-stu-id="dd843-104">TBM\_GETSELSTART message</span></span>

<span data-ttu-id="dd843-105">Получает начальную точку текущего диапазона выбора в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="dd843-105">Retrieves the starting position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd843-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd843-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd843-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd843-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dd843-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="dd843-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dd843-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd843-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dd843-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="dd843-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd843-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd843-111">Return value</span></span>

<span data-ttu-id="dd843-112">Возвращает 32-разрядное значение, указывающее начальную точку диапазона текущего выбора.</span><span class="sxs-lookup"><span data-stu-id="dd843-112">Returns a 32-bit value that specifies the starting position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd843-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd843-113">Remarks</span></span>

<span data-ttu-id="dd843-114">Параметр TrackBar может иметь диапазон выбора, только если вы указали стиль [**TBS \_ енаблеселранже**](trackbar-control-styles.md) при его создании.</span><span class="sxs-lookup"><span data-stu-id="dd843-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd843-115">Требования</span><span class="sxs-lookup"><span data-stu-id="dd843-115">Requirements</span></span>



| <span data-ttu-id="dd843-116">Требование</span><span class="sxs-lookup"><span data-stu-id="dd843-116">Requirement</span></span> | <span data-ttu-id="dd843-117">Значение</span><span class="sxs-lookup"><span data-stu-id="dd843-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd843-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd843-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dd843-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd843-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd843-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd843-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dd843-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd843-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd843-122">Header</span><span class="sxs-lookup"><span data-stu-id="dd843-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd843-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd843-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd843-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd843-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="dd843-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="dd843-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dd843-126">**ТБМ \_ жетселенд**</span><span class="sxs-lookup"><span data-stu-id="dd843-126">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="dd843-127">**ТБМ \_ сетсел**</span><span class="sxs-lookup"><span data-stu-id="dd843-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="dd843-128">**ТБМ \_ сетселенд**</span><span class="sxs-lookup"><span data-stu-id="dd843-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="dd843-129">**ТБМ \_ сетселстарт**</span><span class="sxs-lookup"><span data-stu-id="dd843-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





