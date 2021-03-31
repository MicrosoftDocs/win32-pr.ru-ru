---
title: Сообщение LB_GETSELCOUNT (Winuser. h)
description: Возвращает общее число выбранных элементов в списке с множественным выбором.
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- Элементы управления Windows для LB_GETSELCOUNT сообщений
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed73b387315d1b612241d41e47e6b613a3a75f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135602"
---
# <a name="lb_getselcount-message"></a><span data-ttu-id="4cf4b-104">Сообщение жетселкаунт балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="4cf4b-104">LB\_GETSELCOUNT message</span></span>

<span data-ttu-id="4cf4b-105">Возвращает общее число выбранных элементов в списке с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="4cf4b-105">Gets the total number of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cf4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cf4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf4b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cf4b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cf4b-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="4cf4b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4cf4b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cf4b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cf4b-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="4cf4b-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf4b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cf4b-111">Return value</span></span>

<span data-ttu-id="4cf4b-112">Возвращаемое значение — это количество выбранных элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="4cf4b-112">The return value is the count of selected items in the list box.</span></span> <span data-ttu-id="4cf4b-113">Если список является списком с одним выбором, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="4cf4b-113">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf4b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4cf4b-114">Requirements</span></span>



| <span data-ttu-id="4cf4b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4cf4b-115">Requirement</span></span> | <span data-ttu-id="4cf4b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4cf4b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf4b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cf4b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf4b-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cf4b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4cf4b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cf4b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf4b-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4cf4b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4cf4b-121">Header</span><span class="sxs-lookup"><span data-stu-id="4cf4b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cf4b-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cf4b-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cf4b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cf4b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf4b-124">**сетсел балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="4cf4b-124">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





