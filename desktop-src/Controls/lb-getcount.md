---
title: Сообщение LB_GETCOUNT (Winuser. h)
description: Возвращает число элементов в поле со списком.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- Элементы управления Windows для LB_GETCOUNT сообщений
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddedbd7b9165e00e722edbadbb8806a68417551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492855"
---
# <a name="lb_getcount-message"></a><span data-ttu-id="7d109-104">\_Сообщение счетчика нагрузки</span><span class="sxs-lookup"><span data-stu-id="7d109-104">LB\_GETCOUNT message</span></span>

<span data-ttu-id="7d109-105">Возвращает число элементов в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="7d109-105">Gets the number of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d109-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d109-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d109-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d109-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d109-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7d109-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7d109-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d109-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d109-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7d109-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d109-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d109-111">Return value</span></span>

<span data-ttu-id="7d109-112">Возвращаемое значение — это число элементов в списке или ошибка балансировки нагрузки \_ при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="7d109-112">The return value is the number of items in the list box, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d109-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d109-113">Remarks</span></span>

<span data-ttu-id="7d109-114">Возвращаемое значение счетчика больше значения индекса последнего элемента (индекс отсчитывается от нуля).</span><span class="sxs-lookup"><span data-stu-id="7d109-114">The returned count is one greater than the index value of the last item (the index is zero-based).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d109-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7d109-115">Requirements</span></span>



| <span data-ttu-id="7d109-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7d109-116">Requirement</span></span> | <span data-ttu-id="7d109-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7d109-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d109-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d109-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7d109-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d109-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7d109-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d109-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7d109-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d109-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7d109-122">Header</span><span class="sxs-lookup"><span data-stu-id="7d109-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d109-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d109-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d109-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d109-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d109-125">**сеткаунт балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="7d109-125">**LB\_SETCOUNT**</span></span>](lb-setcount.md)
</dt> </dl>

 

 





