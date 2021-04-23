---
title: Сообщение LB_SELITEMRANGEEX (Winuser. h)
description: Выбирает один или несколько последовательных элементов в списке с множественным выбором.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- Элементы управления Windows для LB_SELITEMRANGEEX сообщений
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989186"
---
# <a name="lb_selitemrangeex-message"></a><span data-ttu-id="6655a-104">Сообщение селитемранжеекс балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="6655a-104">LB\_SELITEMRANGEEX message</span></span>

<span data-ttu-id="6655a-105">Выбирает один или несколько последовательных элементов в списке с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="6655a-105">Selects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6655a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6655a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6655a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6655a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6655a-108">Указывает отсчитываемый от нуля индекс первого выбираемого элемента.</span><span class="sxs-lookup"><span data-stu-id="6655a-108">Specifies the zero-based index of the first item to select.</span></span>

<span data-ttu-id="6655a-109">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="6655a-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="6655a-110">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="6655a-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="6655a-111">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="6655a-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="6655a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6655a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6655a-113">Указывает отсчитываемый от нуля индекс последнего выбираемого элемента.</span><span class="sxs-lookup"><span data-stu-id="6655a-113">Specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6655a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6655a-114">Return value</span></span>

<span data-ttu-id="6655a-115">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6655a-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="6655a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6655a-116">Remarks</span></span>

<span data-ttu-id="6655a-117">Если параметр *wParam* меньше, чем параметр *lParam* , выбирается указанный диапазон элементов.</span><span class="sxs-lookup"><span data-stu-id="6655a-117">If the *wParam* parameter is less than the *lParam* parameter, the specified range of items is selected.</span></span> <span data-ttu-id="6655a-118">Если параметр *wParam* больше или равен *lParam*, диапазон удаляется из указанного диапазона элементов.</span><span class="sxs-lookup"><span data-stu-id="6655a-118">If *wParam* is greater than or equal to *lParam*, the range is removed from the specified range of items.</span></span> <span data-ttu-id="6655a-119">Чтобы выбрать только один элемент, выберите два элемента и отмените выбор нежелательного элемента.</span><span class="sxs-lookup"><span data-stu-id="6655a-119">To select only one item, select two items and then deselect the unwanted item.</span></span>

<span data-ttu-id="6655a-120">Это сообщение следует использовать только в списках с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="6655a-120">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="6655a-121">Это сообщение может выбрать диапазон только в пределах первых 65 536 элементов.</span><span class="sxs-lookup"><span data-stu-id="6655a-121">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="6655a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6655a-122">Requirements</span></span>



| <span data-ttu-id="6655a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6655a-123">Requirement</span></span> | <span data-ttu-id="6655a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6655a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6655a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6655a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6655a-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6655a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6655a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6655a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6655a-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6655a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6655a-129">Header</span><span class="sxs-lookup"><span data-stu-id="6655a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6655a-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6655a-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6655a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6655a-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="6655a-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="6655a-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6655a-133">**селитемранже балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="6655a-133">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> <dt>

[<span data-ttu-id="6655a-134">**сетсел балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="6655a-134">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





