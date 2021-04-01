---
title: Сообщение LB_GETLISTBOXINFO (Winuser. h)
description: Возвращает количество элементов на столбец в указанном списке.
ms.assetid: 925bebd9-2563-4892-a7d7-73d4ef012b42
keywords:
- Элементы управления Windows для LB_GETLISTBOXINFO сообщений
topic_type:
- apiref
api_name:
- LB_GETLISTBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f49f96e3f12b1c21e81e8b5358e174e576d07f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071521"
---
# <a name="lb_getlistboxinfo-message"></a><span data-ttu-id="06779-104">Сообщение жетлистбоксинфо балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="06779-104">LB\_GETLISTBOXINFO message</span></span>

<span data-ttu-id="06779-105">Возвращает количество элементов на столбец в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="06779-105">Gets the number of items per column in a specified list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="06779-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06779-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06779-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06779-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06779-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="06779-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="06779-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06779-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06779-110">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="06779-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06779-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06779-111">Return value</span></span>

<span data-ttu-id="06779-112">Возвращаемое значение — это количество элементов на столбец.</span><span class="sxs-lookup"><span data-stu-id="06779-112">The return value is the number of items per column.</span></span>

## <a name="remarks"></a><span data-ttu-id="06779-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06779-113">Remarks</span></span>

<span data-ttu-id="06779-114">Это сообщение эквивалентно [**жетлистбоксинфо**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).</span><span class="sxs-lookup"><span data-stu-id="06779-114">This message is equivalent to [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="06779-115">Требования</span><span class="sxs-lookup"><span data-stu-id="06779-115">Requirements</span></span>



| <span data-ttu-id="06779-116">Требование</span><span class="sxs-lookup"><span data-stu-id="06779-116">Requirement</span></span> | <span data-ttu-id="06779-117">Значение</span><span class="sxs-lookup"><span data-stu-id="06779-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06779-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06779-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06779-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06779-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="06779-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06779-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06779-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06779-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="06779-122">Header</span><span class="sxs-lookup"><span data-stu-id="06779-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="06779-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06779-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06779-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06779-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06779-125">**жетлистбоксинфо**</span><span class="sxs-lookup"><span data-stu-id="06779-125">**GetListBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo)
</dt> </dl>

 

 





