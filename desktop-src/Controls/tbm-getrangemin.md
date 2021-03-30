---
title: Сообщение TBM_GETRANGEMIN (Коммктрл. h)
description: Возвращает минимальное положение ползунка в TrackBar.
ms.assetid: 64334aed-0403-4785-829e-693292734d10
keywords:
- Элементы управления Windows для TBM_GETRANGEMIN сообщений
topic_type:
- apiref
api_name:
- TBM_GETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddef597f7b129f8334f75136f56404a8ef117fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988687"
---
# <a name="tbm_getrangemin-message"></a><span data-ttu-id="eead0-104">\_Сообщение ТБМ жетранжемин</span><span class="sxs-lookup"><span data-stu-id="eead0-104">TBM\_GETRANGEMIN message</span></span>

<span data-ttu-id="eead0-105">Возвращает минимальное положение ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="eead0-105">Retrieves the minimum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="eead0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eead0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eead0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eead0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eead0-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="eead0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eead0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eead0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eead0-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="eead0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eead0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eead0-111">Return value</span></span>

<span data-ttu-id="eead0-112">Возвращает 32-разрядное значение, которое указывает минимальное положение ползунка в диапазоне от минимума до максимального значения.</span><span class="sxs-lookup"><span data-stu-id="eead0-112">Returns a 32-bit value that specifies the minimum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="eead0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="eead0-113">Requirements</span></span>



| <span data-ttu-id="eead0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="eead0-114">Requirement</span></span> | <span data-ttu-id="eead0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="eead0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eead0-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eead0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eead0-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eead0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eead0-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eead0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eead0-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eead0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eead0-120">Header</span><span class="sxs-lookup"><span data-stu-id="eead0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eead0-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="eead0-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eead0-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eead0-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="eead0-123">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="eead0-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eead0-124">**ТБМ \_ жетранжемакс**</span><span class="sxs-lookup"><span data-stu-id="eead0-124">**TBM\_GETRANGEMAX**</span></span>](tbm-getrangemax.md)
</dt> <dt>

[<span data-ttu-id="eead0-125">**ТБМ \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="eead0-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="eead0-126">**ТБМ \_ сетранжемакс**</span><span class="sxs-lookup"><span data-stu-id="eead0-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





