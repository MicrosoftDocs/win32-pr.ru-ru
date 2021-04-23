---
title: Сообщение LB_SELECTSTRING (Winuser. h)
description: Выполняет поиск элемента, который начинается с символов в указанной строке, в поле со списком. Если найден соответствующий элемент, элемент выбирается.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- Элементы управления Windows для LB_SELECTSTRING сообщений
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492441"
---
# <a name="lb_selectstring-message"></a><span data-ttu-id="44218-105">Сообщение селектстринг балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="44218-105">LB\_SELECTSTRING message</span></span>

<span data-ttu-id="44218-106">Выполняет поиск элемента, который начинается с символов в указанной строке, в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="44218-106">Searches a list box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="44218-107">Если найден соответствующий элемент, элемент выбирается.</span><span class="sxs-lookup"><span data-stu-id="44218-107">If a matching item is found, the item is selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="44218-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="44218-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44218-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44218-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44218-110">Индекс элемента перед первым искомым элементом (индексация ведется от нуля).</span><span class="sxs-lookup"><span data-stu-id="44218-110">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="44218-111">Когда поиск достигает нижнего края списка, он переходит от верхней части окна списка к элементу, указанному параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="44218-111">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="44218-112">Если параметр *wParam* имеет значение-1, поиск выполняется по всему списку с самого начала.</span><span class="sxs-lookup"><span data-stu-id="44218-112">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="44218-113">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="44218-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="44218-114">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="44218-114">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="44218-115">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="44218-115">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="44218-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44218-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44218-117">Указатель на строку, завершающуюся нулем, которая содержит префикс для поиска.</span><span class="sxs-lookup"><span data-stu-id="44218-117">A pointer to the null-terminated string that contains the prefix for which to search.</span></span> <span data-ttu-id="44218-118">Поиск не зависит от регистра, поэтому эта строка может содержать любое сочетание прописных и строчных букв.</span><span class="sxs-lookup"><span data-stu-id="44218-118">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44218-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44218-119">Return value</span></span>

<span data-ttu-id="44218-120">Если поиск выполнен успешно, возвращается значение индекса выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="44218-120">If the search is successful, the return value is the index of the selected item.</span></span> <span data-ttu-id="44218-121">Если поиск завершается неудачно, возвращается значение фунтов \_ Err, а текущее выделение не изменяется.</span><span class="sxs-lookup"><span data-stu-id="44218-121">If the search is unsuccessful, the return value is LB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="44218-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44218-122">Remarks</span></span>

<span data-ttu-id="44218-123">При необходимости список будет прокручиваться, чтобы отобразить выбранный элемент.</span><span class="sxs-lookup"><span data-stu-id="44218-123">The list box is scrolled, if necessary, to bring the selected item into view.</span></span>

<span data-ttu-id="44218-124">Не используйте это сообщение со списком, имеющим стили [**фунта \_ Мултиплесел**](list-box-styles.md) или [**фунты \_ екстендедсел**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="44218-124">Do not use this message with a list box that has the [**LBS\_MULTIPLESEL**](list-box-styles.md) or the [**LBS\_EXTENDEDSEL**](list-box-styles.md) styles.</span></span>

<span data-ttu-id="44218-125">Элемент выбирается только в том случае, если его начальные символы из начальной точки соответствуют символам в строке, указанной параметром *lParam* .</span><span class="sxs-lookup"><span data-stu-id="44218-125">An item is selected only if its initial characters from the starting point match the characters in the string specified by the *lParam* parameter.</span></span>

<span data-ttu-id="44218-126">Если список имеет стиль, рисуемый владельцем, но не хасстрингс в [**стиле \_ фунта**](list-box-styles.md) , действие, выполняемое методом **балансировки нагрузки \_ селектстринг** , зависит от того, используется ли стиль [**\_ сортировки фунтов**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="44218-126">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_SELECTSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="44218-127">Если **используется \_ Сортировка фунтов** , система отправляет сообщения [**WM \_ компареитем**](wm-compareitem.md) владельцу списка, чтобы определить, какой элемент соответствует заданной строке.</span><span class="sxs-lookup"><span data-stu-id="44218-127">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="44218-128">В противном случае **Балансировка нагрузки \_ селектстринг** пытается найти элемент с длинным значением (предоставленным как параметр *lParam* сообщения [**\_ ADDSTRING**](lb-addstring.md) или [**\_ балансировки**](lb-insertstring.md) нагрузки), соответствующий параметру *lParam* .</span><span class="sxs-lookup"><span data-stu-id="44218-128">Otherwise, **LB\_SELECTSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="44218-129">Требования</span><span class="sxs-lookup"><span data-stu-id="44218-129">Requirements</span></span>



| <span data-ttu-id="44218-130">Требование</span><span class="sxs-lookup"><span data-stu-id="44218-130">Requirement</span></span> | <span data-ttu-id="44218-131">Значение</span><span class="sxs-lookup"><span data-stu-id="44218-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44218-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44218-132">Minimum supported client</span></span><br/> | <span data-ttu-id="44218-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44218-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44218-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44218-134">Minimum supported server</span></span><br/> | <span data-ttu-id="44218-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="44218-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44218-136">Header</span><span class="sxs-lookup"><span data-stu-id="44218-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="44218-137"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44218-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44218-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44218-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="44218-139">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="44218-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="44218-140">**ADDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="44218-140">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="44218-141">**FINDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="44218-141">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> <dt>

[<span data-ttu-id="44218-142">**инсертстринг балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="44218-142">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





