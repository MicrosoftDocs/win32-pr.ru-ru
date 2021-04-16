---
title: Сообщение TBM_GETSELEND (Коммктрл. h)
description: Извлекает конечное расположение текущего диапазона выбора в TrackBar.
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- Элементы управления Windows для TBM_GETSELEND сообщений
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 486d66d3e7fc2dd4d23b89cb5e9406fa81b34638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490695"
---
# <a name="tbm_getselend-message"></a><span data-ttu-id="5a9f0-104">\_Сообщение ТБМ жетселенд</span><span class="sxs-lookup"><span data-stu-id="5a9f0-104">TBM\_GETSELEND message</span></span>

<span data-ttu-id="5a9f0-105">Извлекает конечное расположение текущего диапазона выбора в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5a9f0-105">Retrieves the ending position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a9f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a9f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a9f0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a9f0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5a9f0-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5a9f0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5a9f0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a9f0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5a9f0-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5a9f0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a9f0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a9f0-111">Return value</span></span>

<span data-ttu-id="5a9f0-112">Возвращает 32-разрядное значение, указывающее конечную точку текущего диапазона выбора.</span><span class="sxs-lookup"><span data-stu-id="5a9f0-112">Returns a 32-bit value that specifies the ending position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a9f0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a9f0-113">Remarks</span></span>

<span data-ttu-id="5a9f0-114">Параметр TrackBar может иметь диапазон выбора, только если вы указали стиль [**TBS \_ енаблеселранже**](trackbar-control-styles.md) при его создании.</span><span class="sxs-lookup"><span data-stu-id="5a9f0-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a9f0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5a9f0-115">Requirements</span></span>



| <span data-ttu-id="5a9f0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5a9f0-116">Requirement</span></span> | <span data-ttu-id="5a9f0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5a9f0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a9f0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a9f0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5a9f0-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a9f0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a9f0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a9f0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5a9f0-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a9f0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a9f0-122">Header</span><span class="sxs-lookup"><span data-stu-id="5a9f0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a9f0-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a9f0-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a9f0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a9f0-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="5a9f0-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5a9f0-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5a9f0-126">**ТБМ \_ жетселстарт**</span><span class="sxs-lookup"><span data-stu-id="5a9f0-126">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="5a9f0-127">**ТБМ \_ сетсел**</span><span class="sxs-lookup"><span data-stu-id="5a9f0-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="5a9f0-128">**ТБМ \_ сетселенд**</span><span class="sxs-lookup"><span data-stu-id="5a9f0-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="5a9f0-129">**ТБМ \_ сетселстарт**</span><span class="sxs-lookup"><span data-stu-id="5a9f0-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





