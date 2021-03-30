---
title: Сообщение TB_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления.
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- Элементы управления Windows для TB_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- TB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a44b1f65647953702deae5bee6cdd9acc8186e3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802507"
---
# <a name="tb_getunicodeformat-message"></a><span data-ttu-id="ffe2d-104">\_Сообщение ЖЕТУНИКОДЕФОРМАТ ТБ</span><span class="sxs-lookup"><span data-stu-id="ffe2d-104">TB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="ffe2d-105">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ffe2d-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ffe2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffe2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffe2d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ffe2d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ffe2d-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ffe2d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ffe2d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ffe2d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ffe2d-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ffe2d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffe2d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffe2d-111">Return value</span></span>

<span data-ttu-id="ffe2d-112">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ffe2d-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="ffe2d-113">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="ffe2d-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="ffe2d-114">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="ffe2d-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffe2d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffe2d-115">Remarks</span></span>

<span data-ttu-id="ffe2d-116">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="ffe2d-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe2d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ffe2d-117">Requirements</span></span>



| <span data-ttu-id="ffe2d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ffe2d-118">Requirement</span></span> | <span data-ttu-id="ffe2d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ffe2d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe2d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffe2d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ffe2d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ffe2d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ffe2d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffe2d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ffe2d-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ffe2d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ffe2d-124">Header</span><span class="sxs-lookup"><span data-stu-id="ffe2d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffe2d-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffe2d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffe2d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffe2d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe2d-127">**\_СЕТУНИКОДЕФОРМАТ ТБ**</span><span class="sxs-lookup"><span data-stu-id="ffe2d-127">**TB\_SETUNICODEFORMAT**</span></span>](tb-setunicodeformat.md)
</dt> </dl>

 

 





