---
title: Сообщение CBEM_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления.
ms.assetid: 854ff8d5-6e2f-4918-a6c5-91356a4454af
keywords:
- Элементы управления Windows для CBEM_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- CBEM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b77bb0daabe6ef14d4be1b5e2de6bb1dd63248d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892702"
---
# <a name="cbem_getunicodeformat-message"></a><span data-ttu-id="5dd06-104">\_Сообщение кбем жетуникодеформат</span><span class="sxs-lookup"><span data-stu-id="5dd06-104">CBEM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="5dd06-105">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5dd06-105">Gets the UNICODE character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5dd06-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dd06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd06-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5dd06-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5dd06-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5dd06-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5dd06-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5dd06-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5dd06-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5dd06-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dd06-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dd06-111">Return value</span></span>

<span data-ttu-id="5dd06-112">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5dd06-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="5dd06-113">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="5dd06-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="5dd06-114">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="5dd06-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dd06-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5dd06-115">Remarks</span></span>

<span data-ttu-id="5dd06-116">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd06-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dd06-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5dd06-117">Requirements</span></span>



| <span data-ttu-id="5dd06-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5dd06-118">Requirement</span></span> | <span data-ttu-id="5dd06-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5dd06-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd06-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5dd06-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5dd06-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5dd06-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5dd06-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5dd06-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5dd06-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5dd06-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5dd06-124">Header</span><span class="sxs-lookup"><span data-stu-id="5dd06-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dd06-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dd06-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dd06-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dd06-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd06-127">**КБЕМ \_ сетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="5dd06-127">**CBEM\_SETUNICODEFORMAT**</span></span>](cbem-setunicodeformat.md)
</dt> </dl>

 

 





