---
title: Сообщение RB_GETUNICODEFORMAT (Коммктрл. h)
description: RB_GETUNICODEFORMAT сообщение — получает флаг формата символов Юникода для элемента управления.
ms.assetid: 48a4472b-dda4-41a2-b5bc-6f74b1cdc70b
keywords:
- Элементы управления Windows для RB_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- RB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e1a4546c9c33e87943d305c85939ab280fa122
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085982"
---
# <a name="rb_getunicodeformat-message"></a><span data-ttu-id="bb92f-104">\_Сообщение ЖЕТУНИКОДЕФОРМАТ RB</span><span class="sxs-lookup"><span data-stu-id="bb92f-104">RB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="bb92f-105">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="bb92f-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb92f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb92f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb92f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb92f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bb92f-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bb92f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bb92f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb92f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bb92f-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bb92f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb92f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb92f-111">Return value</span></span>

<span data-ttu-id="bb92f-112">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="bb92f-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="bb92f-113">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="bb92f-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="bb92f-114">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="bb92f-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb92f-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="bb92f-115">Remarks</span></span>

<span data-ttu-id="bb92f-116">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="bb92f-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb92f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bb92f-117">Requirements</span></span>



| <span data-ttu-id="bb92f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bb92f-118">Requirement</span></span> | <span data-ttu-id="bb92f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bb92f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb92f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb92f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb92f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb92f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb92f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb92f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb92f-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb92f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb92f-124">Header</span><span class="sxs-lookup"><span data-stu-id="bb92f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb92f-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb92f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb92f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="bb92f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb92f-127">**\_СЕТУНИКОДЕФОРМАТ RB**</span><span class="sxs-lookup"><span data-stu-id="bb92f-127">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
</dt> </dl>

 

 





