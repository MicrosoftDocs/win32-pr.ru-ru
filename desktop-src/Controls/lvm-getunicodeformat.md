---
title: Сообщение LVM_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления. Это сообщение можно отправить явным образом или использовать \_ макрос Жетуникодеформат ListView.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- Элементы управления Windows для LVM_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720a65baab8ec9c1ec3b311e49fe3672c97a0fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892441"
---
# <a name="lvm_getunicodeformat-message"></a><span data-ttu-id="2a00d-105">\_Сообщение LVM жетуникодеформат</span><span class="sxs-lookup"><span data-stu-id="2a00d-105">LVM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="2a00d-106">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2a00d-106">Retrieves the UNICODE character format flag for the control.</span></span> <span data-ttu-id="2a00d-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетуникодеформат ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="2a00d-107">You can send this message explicitly or use the [**ListView\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a00d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a00d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a00d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a00d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2a00d-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2a00d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2a00d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a00d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2a00d-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2a00d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a00d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a00d-113">Return value</span></span>

<span data-ttu-id="2a00d-114">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2a00d-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="2a00d-115">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="2a00d-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="2a00d-116">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="2a00d-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a00d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a00d-117">Remarks</span></span>

<span data-ttu-id="2a00d-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="2a00d-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a00d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2a00d-119">Requirements</span></span>



| <span data-ttu-id="2a00d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2a00d-120">Requirement</span></span> | <span data-ttu-id="2a00d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2a00d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a00d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a00d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2a00d-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a00d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a00d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a00d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2a00d-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a00d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a00d-126">Header</span><span class="sxs-lookup"><span data-stu-id="2a00d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a00d-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a00d-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a00d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a00d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a00d-129">**LVM \_ сетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="2a00d-129">**LVM\_SETUNICODEFORMAT**</span></span>](lvm-setunicodeformat.md)
</dt> </dl>

 

 





