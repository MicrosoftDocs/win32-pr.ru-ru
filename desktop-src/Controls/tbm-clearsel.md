---
title: Сообщение TBM_CLEARSEL (Коммктрл. h)
description: Очищает текущий диапазон выбора в TrackBar.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- Элементы управления Windows для TBM_CLEARSEL сообщений
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d2474f3978dc80b2611bd6b454c45e515ee159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892790"
---
# <a name="tbm_clearsel-message"></a><span data-ttu-id="fcf22-104">\_Сообщение ТБМ клеарсел</span><span class="sxs-lookup"><span data-stu-id="fcf22-104">TBM\_CLEARSEL message</span></span>

<span data-ttu-id="fcf22-105">Очищает текущий диапазон выбора в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="fcf22-105">Clears the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcf22-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fcf22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcf22-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcf22-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcf22-108">Флаг перерисовки.</span><span class="sxs-lookup"><span data-stu-id="fcf22-108">Redraw flag.</span></span> <span data-ttu-id="fcf22-109">Если этот параметр имеет **значение true**, линейка перерисовывается после очистки выделения.</span><span class="sxs-lookup"><span data-stu-id="fcf22-109">If this parameter is **TRUE**, the trackbar is redrawn after the selection is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="fcf22-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcf22-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fcf22-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fcf22-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcf22-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fcf22-112">Return value</span></span>

<span data-ttu-id="fcf22-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fcf22-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcf22-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcf22-114">Remarks</span></span>

<span data-ttu-id="fcf22-115">Параметр TrackBar может иметь диапазон выбора, только если вы указали стиль [**TBS \_ енаблеселранже**](trackbar-control-styles.md) при его создании.</span><span class="sxs-lookup"><span data-stu-id="fcf22-115">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf22-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fcf22-116">Requirements</span></span>



| <span data-ttu-id="fcf22-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fcf22-117">Requirement</span></span> | <span data-ttu-id="fcf22-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fcf22-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf22-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcf22-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fcf22-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcf22-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcf22-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcf22-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fcf22-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fcf22-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcf22-123">Header</span><span class="sxs-lookup"><span data-stu-id="fcf22-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcf22-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcf22-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcf22-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcf22-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="fcf22-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fcf22-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fcf22-127">**ТБМ \_ сетсел**</span><span class="sxs-lookup"><span data-stu-id="fcf22-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="fcf22-128">**ТБМ \_ сетселенд**</span><span class="sxs-lookup"><span data-stu-id="fcf22-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="fcf22-129">**ТБМ \_ сетселстарт**</span><span class="sxs-lookup"><span data-stu-id="fcf22-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





