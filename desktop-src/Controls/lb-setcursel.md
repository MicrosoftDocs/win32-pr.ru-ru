---
title: Сообщение LB_SETCURSEL (Winuser. h)
description: Выбирает строку и прокручивает ее на представление при необходимости. При выборе новой строки список удаляет выделение из ранее выбранной строки.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- Элементы управления Windows для LB_SETCURSEL сообщений
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105647135"
---
# <a name="lb_setcursel-message"></a><span data-ttu-id="ea1dd-105">Сообщение сеткурсел балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="ea1dd-105">LB\_SETCURSEL message</span></span>

<span data-ttu-id="ea1dd-106">Выбирает строку и прокручивает ее на представление при необходимости.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-106">Selects a string and scrolls it into view, if necessary.</span></span> <span data-ttu-id="ea1dd-107">При выборе новой строки список удаляет выделение из ранее выбранной строки.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-107">When the new string is selected, the list box removes the highlight from the previously selected string.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea1dd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea1dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea1dd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea1dd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea1dd-110">Указывает отсчитываемый от нуля индекс выбранной строки.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-110">Specifies the zero-based index of the string that is selected.</span></span> <span data-ttu-id="ea1dd-111">Если этот параметр имеет значение-1, то список не будет выбран.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-111">If this parameter is -1, the list box is set to have no selection.</span></span>

<span data-ttu-id="ea1dd-112">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="ea1dd-113">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-113">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="ea1dd-114">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-114">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="ea1dd-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea1dd-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea1dd-116">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea1dd-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea1dd-117">Return value</span></span>

<span data-ttu-id="ea1dd-118">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="ea1dd-119">Если параметр *wParam* равен-1, то возвращаемое значение — это ошибка балансировки нагрузки, хотя при этом \_ не возникает ошибок.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-119">If the *wParam* parameter is -1, the return value is LB\_ERR even though no error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea1dd-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea1dd-120">Remarks</span></span>

<span data-ttu-id="ea1dd-121">Используйте это сообщение только в списках с одним выбором.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-121">Use this message only with single-selection list boxes.</span></span> <span data-ttu-id="ea1dd-122">Его нельзя использовать для установки или удаления выделения в списке с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="ea1dd-122">You cannot use it to set or remove a selection in a multiple-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea1dd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ea1dd-123">Requirements</span></span>



| <span data-ttu-id="ea1dd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ea1dd-124">Requirement</span></span> | <span data-ttu-id="ea1dd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ea1dd-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea1dd-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea1dd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea1dd-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea1dd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ea1dd-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea1dd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea1dd-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea1dd-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ea1dd-130">Header</span><span class="sxs-lookup"><span data-stu-id="ea1dd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea1dd-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea1dd-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea1dd-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea1dd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea1dd-133">**нерекурсивная балансировка нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="ea1dd-133">**LB\_GETCURSEL**</span></span>](lb-getcursel.md)
</dt> </dl>

 

 





