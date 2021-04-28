---
title: Сообщение UDM_GETUNICODEFORMAT (Коммктрл. h)
description: UDM_GETUNICODEFORMAT сообщение — получает флаг формата символов Юникода для элемента управления.
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- Элементы управления Windows для UDM_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- UDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273164df7f7021f39ec26a22eb637e8b9969fc24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113593"
---
# <a name="udm_getunicodeformat-message"></a><span data-ttu-id="59a84-104">\_Сообщение ЖЕТУНИКОДЕФОРМАТ UDM</span><span class="sxs-lookup"><span data-stu-id="59a84-104">UDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="59a84-105">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="59a84-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="59a84-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59a84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59a84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59a84-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="59a84-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="59a84-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="59a84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59a84-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="59a84-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="59a84-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59a84-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59a84-111">Return value</span></span>

<span data-ttu-id="59a84-112">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="59a84-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="59a84-113">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="59a84-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="59a84-114">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="59a84-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="59a84-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="59a84-115">Remarks</span></span>

<span data-ttu-id="59a84-116">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="59a84-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="59a84-117">Требования</span><span class="sxs-lookup"><span data-stu-id="59a84-117">Requirements</span></span>



| <span data-ttu-id="59a84-118">Требование</span><span class="sxs-lookup"><span data-stu-id="59a84-118">Requirement</span></span> | <span data-ttu-id="59a84-119">Значение</span><span class="sxs-lookup"><span data-stu-id="59a84-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59a84-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59a84-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59a84-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59a84-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59a84-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59a84-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59a84-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59a84-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59a84-124">Header</span><span class="sxs-lookup"><span data-stu-id="59a84-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="59a84-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="59a84-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59a84-126">См. также</span><span class="sxs-lookup"><span data-stu-id="59a84-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a84-127">**\_СЕТУНИКОДЕФОРМАТ UDM**</span><span class="sxs-lookup"><span data-stu-id="59a84-127">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md)
</dt> </dl>

 

 





