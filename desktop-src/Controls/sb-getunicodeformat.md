---
title: Сообщение SB_GETUNICODEFORMAT (Коммктрл. h)
description: SB_GETUNICODEFORMAT сообщение — получает флаг формата символов Юникода для элемента управления.
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- Элементы управления Windows для SB_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- SB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857af43911a01ffc58b1a878be6e1875a44c76cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085902"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="a41da-104">\_Сообщение SB жетуникодеформат</span><span class="sxs-lookup"><span data-stu-id="a41da-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="a41da-105">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a41da-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a41da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a41da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a41da-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a41da-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a41da-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a41da-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a41da-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a41da-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a41da-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a41da-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a41da-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a41da-111">Return value</span></span>

<span data-ttu-id="a41da-112">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a41da-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="a41da-113">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="a41da-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="a41da-114">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="a41da-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a41da-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="a41da-115">Remarks</span></span>

<span data-ttu-id="a41da-116">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="a41da-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a41da-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a41da-117">Requirements</span></span>



| <span data-ttu-id="a41da-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a41da-118">Requirement</span></span> | <span data-ttu-id="a41da-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a41da-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a41da-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a41da-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a41da-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a41da-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a41da-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a41da-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a41da-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a41da-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a41da-124">Header</span><span class="sxs-lookup"><span data-stu-id="a41da-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a41da-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a41da-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a41da-126">См. также</span><span class="sxs-lookup"><span data-stu-id="a41da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a41da-127">**SB \_ сетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="a41da-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





