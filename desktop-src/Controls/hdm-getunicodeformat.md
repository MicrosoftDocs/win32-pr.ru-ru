---
title: Сообщение HDM_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса жетуникодеформат.
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- Элементы управления Windows для HDM_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce625cc9d4c0ede0c4ce9b54dc852025b22d4870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135958"
---
# <a name="hdm_getunicodeformat-message"></a><span data-ttu-id="79c0e-105">\_Сообщение ЖЕТУНИКОДЕФОРМАТ HDM</span><span class="sxs-lookup"><span data-stu-id="79c0e-105">HDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="79c0e-106">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="79c0e-106">Gets the Unicode character format flag for the control.</span></span> <span data-ttu-id="79c0e-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ жетуникодеформат**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="79c0e-107">You can send this message explicitly or use the [**Header\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="79c0e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="79c0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79c0e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79c0e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="79c0e-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="79c0e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="79c0e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79c0e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="79c0e-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="79c0e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79c0e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79c0e-113">Return value</span></span>

<span data-ttu-id="79c0e-114">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="79c0e-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="79c0e-115">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="79c0e-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="79c0e-116">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="79c0e-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="79c0e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79c0e-117">Remarks</span></span>

<span data-ttu-id="79c0e-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="79c0e-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c0e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="79c0e-119">Requirements</span></span>



| <span data-ttu-id="79c0e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="79c0e-120">Requirement</span></span> | <span data-ttu-id="79c0e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="79c0e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79c0e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79c0e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="79c0e-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79c0e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79c0e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79c0e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="79c0e-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="79c0e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79c0e-126">Header</span><span class="sxs-lookup"><span data-stu-id="79c0e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="79c0e-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="79c0e-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79c0e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79c0e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c0e-129">**\_СЕТУНИКОДЕФОРМАТ HDM**</span><span class="sxs-lookup"><span data-stu-id="79c0e-129">**HDM\_SETUNICODEFORMAT**</span></span>](hdm-setunicodeformat.md)
</dt> </dl>

 

 





