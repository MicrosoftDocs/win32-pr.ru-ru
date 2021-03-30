---
title: Сообщение MCM_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления. Это сообщение можно отправить явным образом или использовать макрос Монскал \_ жетуникодеформат.
ms.assetid: 28261e11-0fd0-407e-9f62-446536d62460
keywords:
- Элементы управления Windows для MCM_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- MCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4be573923f154958e1defd0be2adb02068076950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803832"
---
# <a name="mcm_getunicodeformat-message"></a><span data-ttu-id="50795-105">\_Сообщение MCM жетуникодеформат</span><span class="sxs-lookup"><span data-stu-id="50795-105">MCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="50795-106">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="50795-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="50795-107">Это сообщение можно отправить явным образом или использовать макрос [**монскал \_ жетуникодеформат**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="50795-107">You can send this message explicitly or use the [**MonthCal\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="50795-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50795-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50795-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50795-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="50795-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="50795-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="50795-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50795-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="50795-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="50795-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50795-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50795-113">Return value</span></span>

<span data-ttu-id="50795-114">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="50795-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="50795-115">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="50795-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="50795-116">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="50795-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="50795-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50795-117">Remarks</span></span>

<span data-ttu-id="50795-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="50795-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="50795-119">Требования</span><span class="sxs-lookup"><span data-stu-id="50795-119">Requirements</span></span>



| <span data-ttu-id="50795-120">Требование</span><span class="sxs-lookup"><span data-stu-id="50795-120">Requirement</span></span> | <span data-ttu-id="50795-121">Значение</span><span class="sxs-lookup"><span data-stu-id="50795-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50795-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50795-122">Minimum supported client</span></span><br/> | <span data-ttu-id="50795-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50795-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50795-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50795-124">Minimum supported server</span></span><br/> | <span data-ttu-id="50795-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50795-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50795-126">Header</span><span class="sxs-lookup"><span data-stu-id="50795-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="50795-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="50795-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50795-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50795-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50795-129">**MCM \_ сетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="50795-129">**MCM\_SETUNICODEFORMAT**</span></span>](mcm-setunicodeformat.md)
</dt> </dl>

 

 





