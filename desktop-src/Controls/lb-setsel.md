---
title: Сообщение LB_SETSEL (Winuser. h)
description: Выбирает элемент в списке с множественным выбором и при необходимости прокручивает его до представления.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- Элементы управления Windows для LB_SETSEL сообщений
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492429"
---
# <a name="lb_setsel-message"></a><span data-ttu-id="f3b01-104">Сообщение сетсел балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="f3b01-104">LB\_SETSEL message</span></span>

<span data-ttu-id="f3b01-105">Выбирает элемент в списке с множественным выбором и при необходимости прокручивает его до представления.</span><span class="sxs-lookup"><span data-stu-id="f3b01-105">Selects an item in a multiple-selection list box and, if necessary, scrolls the item into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3b01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3b01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3b01-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3b01-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3b01-108">Указывает, как задать выбор.</span><span class="sxs-lookup"><span data-stu-id="f3b01-108">Specifies how to set the selection.</span></span> <span data-ttu-id="f3b01-109">Если этот параметр имеет **значение true**, элемент выделяется и выделяется; Если значение равно **false**, выделение удаляется и элемент больше не выбирается.</span><span class="sxs-lookup"><span data-stu-id="f3b01-109">If this parameter is **TRUE**, the item is selected and highlighted; if it is **FALSE**, the highlight is removed and the item is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="f3b01-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3b01-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3b01-111">Задает отсчитываемый от нуля индекс элемента, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="f3b01-111">Specifies the zero-based index of the item to set.</span></span> <span data-ttu-id="f3b01-112">Если этот параметр имеет значение-1, выбор добавляется или удаляется из всех элементов, в зависимости от значения *wParam*, и прокрутка не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3b01-112">If this parameter is -1, the selection is added to or removed from all items, depending on the value of *wParam*, and no scrolling occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3b01-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3b01-113">Return value</span></span>

<span data-ttu-id="f3b01-114">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="f3b01-114">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3b01-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3b01-115">Remarks</span></span>

<span data-ttu-id="f3b01-116">Это сообщение следует использовать только в списках с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="f3b01-116">Use this message only with multiple-selection list boxes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b01-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f3b01-117">Requirements</span></span>



| <span data-ttu-id="f3b01-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f3b01-118">Requirement</span></span> | <span data-ttu-id="f3b01-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f3b01-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b01-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3b01-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b01-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3b01-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f3b01-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3b01-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b01-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f3b01-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f3b01-124">Header</span><span class="sxs-lookup"><span data-stu-id="f3b01-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3b01-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3b01-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b01-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3b01-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3b01-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f3b01-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f3b01-128">**жетсел балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="f3b01-128">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="f3b01-129">**селитемранже балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="f3b01-129">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> </dl>

 

 





