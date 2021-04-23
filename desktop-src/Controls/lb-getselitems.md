---
title: Сообщение LB_GETSELITEMS (Winuser. h)
description: Заполняет буфер массивом целых чисел, задающих номера элементов выбранных элементов в списке с множественным выбором.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- Элементы управления Windows для LB_GETSELITEMS сообщений
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988729"
---
# <a name="lb_getselitems-message"></a><span data-ttu-id="6de7f-104">Сообщение жетселитемс балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="6de7f-104">LB\_GETSELITEMS message</span></span>

<span data-ttu-id="6de7f-105">Заполняет буфер массивом целых чисел, задающих номера элементов выбранных элементов в списке с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="6de7f-105">Fills a buffer with an array of integers that specify the item numbers of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6de7f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6de7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6de7f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6de7f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6de7f-108">Максимальное число выбранных элементов, номера элементов которых должны быть помещены в буфер.</span><span class="sxs-lookup"><span data-stu-id="6de7f-108">The maximum number of selected items whose item numbers are to be placed in the buffer.</span></span>

<span data-ttu-id="6de7f-109">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="6de7f-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="6de7f-110">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="6de7f-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="6de7f-111">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="6de7f-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="6de7f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6de7f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6de7f-113">Указатель на буфер, достаточно большой для числа целых чисел, заданного параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="6de7f-113">A pointer to a buffer large enough for the number of integers specified by the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6de7f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6de7f-114">Return value</span></span>

<span data-ttu-id="6de7f-115">Возвращаемое значение — это число элементов, помещаемых в буфер.</span><span class="sxs-lookup"><span data-stu-id="6de7f-115">The return value is the number of items placed in the buffer.</span></span> <span data-ttu-id="6de7f-116">Если список является списком с одним выбором, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6de7f-116">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="6de7f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6de7f-117">Requirements</span></span>



| <span data-ttu-id="6de7f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6de7f-118">Requirement</span></span> | <span data-ttu-id="6de7f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6de7f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de7f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6de7f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6de7f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6de7f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6de7f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6de7f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6de7f-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6de7f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6de7f-124">Header</span><span class="sxs-lookup"><span data-stu-id="6de7f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6de7f-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6de7f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de7f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6de7f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de7f-127">**жетселкаунт балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="6de7f-127">**LB\_GETSELCOUNT**</span></span>](lb-getselcount.md)
</dt> </dl>

 

 





