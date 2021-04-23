---
title: Сообщение TBM_GETRANGEMAX (Коммктрл. h)
description: Получает максимальную положение ползунка в TrackBar.
ms.assetid: c0ae5f96-f4ce-46cd-84d0-9e7c473441a0
keywords:
- Элементы управления Windows для TBM_GETRANGEMAX сообщений
topic_type:
- apiref
api_name:
- TBM_GETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bdd9687b617759ab8b8fdea59ed06d7fcd78b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071652"
---
# <a name="tbm_getrangemax-message"></a><span data-ttu-id="7938d-104">\_Сообщение ТБМ жетранжемакс</span><span class="sxs-lookup"><span data-stu-id="7938d-104">TBM\_GETRANGEMAX message</span></span>

<span data-ttu-id="7938d-105">Получает максимальную положение ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="7938d-105">Retrieves the maximum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7938d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7938d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7938d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7938d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7938d-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7938d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7938d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7938d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7938d-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7938d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7938d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7938d-111">Return value</span></span>

<span data-ttu-id="7938d-112">Возвращает 32-разрядное значение, указывающее максимальную позицию ползунка в диапазоне от минимума до максимального значения.</span><span class="sxs-lookup"><span data-stu-id="7938d-112">Returns a 32-bit value that specifies the maximum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7938d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7938d-113">Requirements</span></span>



| <span data-ttu-id="7938d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7938d-114">Requirement</span></span> | <span data-ttu-id="7938d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7938d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7938d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7938d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7938d-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7938d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7938d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7938d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7938d-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7938d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7938d-120">Header</span><span class="sxs-lookup"><span data-stu-id="7938d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7938d-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7938d-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7938d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7938d-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="7938d-123">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7938d-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7938d-124">**ТБМ \_ жетранжемин**</span><span class="sxs-lookup"><span data-stu-id="7938d-124">**TBM\_GETRANGEMIN**</span></span>](tbm-getrangemin.md)
</dt> <dt>

[<span data-ttu-id="7938d-125">**ТБМ \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="7938d-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="7938d-126">**ТБМ \_ сетранжемакс**</span><span class="sxs-lookup"><span data-stu-id="7938d-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





