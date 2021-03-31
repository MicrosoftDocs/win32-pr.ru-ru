---
title: Сообщение TCM_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления. Это сообщение можно отправить явным образом или использовать макрос Табктрл \_ жетуникодеформат.
ms.assetid: 720e0325-500b-436c-8713-38ed780735bf
keywords:
- Элементы управления Windows для TCM_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- TCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b497f1b2c2b5ac55ee949b498602b50b267fef3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892526"
---
# <a name="tcm_getunicodeformat-message"></a><span data-ttu-id="849b7-105">\_Сообщение ЖЕТУНИКОДЕФОРМАТ TCM</span><span class="sxs-lookup"><span data-stu-id="849b7-105">TCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="849b7-106">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="849b7-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="849b7-107">Это сообщение можно отправить явным образом или использовать макрос [**табктрл \_ жетуникодеформат**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="849b7-107">You can send this message explicitly or use the [**TabCtrl\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="849b7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="849b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="849b7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="849b7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="849b7-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="849b7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="849b7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="849b7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="849b7-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="849b7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="849b7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="849b7-113">Return value</span></span>

<span data-ttu-id="849b7-114">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="849b7-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="849b7-115">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="849b7-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="849b7-116">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="849b7-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="849b7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="849b7-117">Remarks</span></span>

<span data-ttu-id="849b7-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="849b7-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="849b7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="849b7-119">Requirements</span></span>



| <span data-ttu-id="849b7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="849b7-120">Requirement</span></span> | <span data-ttu-id="849b7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="849b7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="849b7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="849b7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="849b7-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="849b7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="849b7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="849b7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="849b7-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="849b7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="849b7-126">Header</span><span class="sxs-lookup"><span data-stu-id="849b7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="849b7-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="849b7-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="849b7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="849b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="849b7-129">**\_СЕТУНИКОДЕФОРМАТ TCM**</span><span class="sxs-lookup"><span data-stu-id="849b7-129">**TCM\_SETUNICODEFORMAT**</span></span>](tcm-setunicodeformat.md)
</dt> </dl>

 

 





