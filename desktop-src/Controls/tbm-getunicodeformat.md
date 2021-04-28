---
title: Сообщение TBM_GETUNICODEFORMAT (Коммктрл. h)
description: TBM_GETUNICODEFORMAT сообщение — получает флаг формата символов Юникода для элемента управления.
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- Элементы управления Windows для TBM_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e7424a4e561ee8f8be79135309089fe4bb0bf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104092"
---
# <a name="tbm_getunicodeformat-message"></a><span data-ttu-id="84f8f-104">\_Сообщение ТБМ жетуникодеформат</span><span class="sxs-lookup"><span data-stu-id="84f8f-104">TBM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="84f8f-105">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="84f8f-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="84f8f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84f8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f8f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84f8f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="84f8f-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="84f8f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="84f8f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84f8f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="84f8f-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="84f8f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f8f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84f8f-111">Return value</span></span>

<span data-ttu-id="84f8f-112">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="84f8f-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="84f8f-113">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="84f8f-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="84f8f-114">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="84f8f-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="84f8f-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="84f8f-115">Remarks</span></span>

<span data-ttu-id="84f8f-116">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="84f8f-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f8f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="84f8f-117">Requirements</span></span>



| <span data-ttu-id="84f8f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="84f8f-118">Requirement</span></span> | <span data-ttu-id="84f8f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="84f8f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84f8f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84f8f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="84f8f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84f8f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84f8f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84f8f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="84f8f-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84f8f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84f8f-124">Header</span><span class="sxs-lookup"><span data-stu-id="84f8f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="84f8f-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="84f8f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f8f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="84f8f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f8f-127">**ТБМ \_ сетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="84f8f-127">**TBM\_SETUNICODEFORMAT**</span></span>](tbm-setunicodeformat.md)
</dt> </dl>

 

 





