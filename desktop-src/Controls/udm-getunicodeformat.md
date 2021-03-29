---
title: Сообщение UDM_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления.
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
ms.openlocfilehash: 4b2f9eef604af6cf5dfcefbf1e3e03dec561ac21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989399"
---
# <a name="udm_getunicodeformat-message"></a><span data-ttu-id="d413d-104">\_Сообщение ЖЕТУНИКОДЕФОРМАТ UDM</span><span class="sxs-lookup"><span data-stu-id="d413d-104">UDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="d413d-105">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d413d-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d413d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d413d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d413d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d413d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d413d-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d413d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d413d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d413d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d413d-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d413d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d413d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d413d-111">Return value</span></span>

<span data-ttu-id="d413d-112">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d413d-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="d413d-113">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="d413d-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="d413d-114">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="d413d-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d413d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d413d-115">Remarks</span></span>

<span data-ttu-id="d413d-116">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ жетуникодеформат**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="d413d-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d413d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d413d-117">Requirements</span></span>



| <span data-ttu-id="d413d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d413d-118">Requirement</span></span> | <span data-ttu-id="d413d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d413d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d413d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d413d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d413d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d413d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d413d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d413d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d413d-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d413d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d413d-124">Header</span><span class="sxs-lookup"><span data-stu-id="d413d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d413d-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d413d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d413d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d413d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d413d-127">**\_СЕТУНИКОДЕФОРМАТ UDM**</span><span class="sxs-lookup"><span data-stu-id="d413d-127">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md)
</dt> </dl>

 

 





