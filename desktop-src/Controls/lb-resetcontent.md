---
title: Сообщение LB_RESETCONTENT (Winuser. h)
description: Удаляет все элементы из списка.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- Элементы управления Windows для LB_RESETCONTENT сообщений
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0091871df045812dcaa7a159cc456a1350d20f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892473"
---
# <a name="lb_resetcontent-message"></a><span data-ttu-id="f9cee-104">Сообщение ресетконтент балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="f9cee-104">LB\_RESETCONTENT message</span></span>

<span data-ttu-id="f9cee-105">Удаляет все элементы из списка.</span><span class="sxs-lookup"><span data-stu-id="f9cee-105">Removes all items from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9cee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9cee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9cee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9cee-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9cee-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f9cee-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f9cee-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9cee-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9cee-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f9cee-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9cee-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9cee-111">Return value</span></span>

<span data-ttu-id="f9cee-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f9cee-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9cee-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9cee-113">Remarks</span></span>

<span data-ttu-id="f9cee-114">Если список имеет стиль, рисуемый владельцем, но не хасстрингс в [**стиле \_ фунта**](list-box-styles.md) , владелец списка получает сообщение [**WM \_ DELETEITEM**](wm-deleteitem.md) для каждого элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="f9cee-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the owner of the list box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9cee-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f9cee-115">Requirements</span></span>



| <span data-ttu-id="f9cee-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f9cee-116">Requirement</span></span> | <span data-ttu-id="f9cee-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f9cee-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9cee-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9cee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9cee-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9cee-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f9cee-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9cee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9cee-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9cee-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f9cee-122">Header</span><span class="sxs-lookup"><span data-stu-id="f9cee-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9cee-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9cee-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9cee-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9cee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9cee-125">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="f9cee-125">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





