---
title: Сообщение LB_FINDSTRINGEXACT (Winuser. h)
description: Находит первую строку списка, которая точно соответствует указанной строке, за исключением того, что поиск не учитывает регистр.
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- Элементы управления Windows для LB_FINDSTRINGEXACT сообщений
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071972"
---
# <a name="lb_findstringexact-message"></a><span data-ttu-id="b47c0-104">Сообщение финдстринжексакт балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="b47c0-104">LB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="b47c0-105">Находит первую строку списка, которая точно соответствует указанной строке, за исключением того, что поиск не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="b47c0-105">Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive.</span></span>

## <a name="parameters"></a><span data-ttu-id="b47c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b47c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b47c0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b47c0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b47c0-108">Индекс элемента перед первым искомым элементом (индексация ведется от нуля).</span><span class="sxs-lookup"><span data-stu-id="b47c0-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="b47c0-109">Когда поиск достигает нижнего края списка, он продолжит поиск в верхней части окна списка назад к элементу, указанному параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="b47c0-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="b47c0-110">Если параметр *wParam* имеет значение-1, поиск выполняется по всему списку с самого начала.</span><span class="sxs-lookup"><span data-stu-id="b47c0-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="b47c0-111">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="b47c0-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="b47c0-112">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="b47c0-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="b47c0-113">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="b47c0-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="b47c0-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b47c0-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b47c0-115">Указатель на строку, завершающуюся нулем, для которой требуется выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="b47c0-115">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="b47c0-116">При поиске регистр не учитывается, поэтому эта строка может содержать любое сочетание прописных и строчных букв.</span><span class="sxs-lookup"><span data-stu-id="b47c0-116">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b47c0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b47c0-117">Return value</span></span>

<span data-ttu-id="b47c0-118">Возвращаемое значение — это Отсчитываемый от нуля индекс совпадающего элемента или ошибка балансировки нагрузки, \_ Если поиск завершился неудачно.</span><span class="sxs-lookup"><span data-stu-id="b47c0-118">The return value is the zero-based index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b47c0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b47c0-119">Remarks</span></span>

<span data-ttu-id="b47c0-120">Эта функция является успешной только в том случае, если указанная строка и элемент списка имеют одинаковую длину (за исключением значения NULL в конце указанной строки) и имеют ровно одинаковые символы.</span><span class="sxs-lookup"><span data-stu-id="b47c0-120">This function is only successful if the specified string and a list box item have the same length (except for the null at the end of the specified string) and have exactly the same characters.</span></span>

<span data-ttu-id="b47c0-121">Если список имеет стиль, рисуемый владельцем, но не хасстрингс в [**стиле \_ фунта**](list-box-styles.md) , действие, выполняемое методом **балансировки нагрузки \_ финдстринжексакт** , зависит от того, используется ли стиль [**\_ сортировки фунтов**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b47c0-121">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRINGEXACT** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="b47c0-122">Если **используется \_ Сортировка фунтов** , система отправляет сообщения [**WM \_ компареитем**](wm-compareitem.md) владельцу списка, чтобы определить, какой элемент соответствует заданной строке.</span><span class="sxs-lookup"><span data-stu-id="b47c0-122">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="b47c0-123">В противном случае **Балансировка нагрузки \_ финдстринжексакт** пытается найти элемент с длинным значением (предоставленным как параметр *lParam* сообщения [**\_ ADDSTRING**](lb-addstring.md) или [**\_ балансировки**](lb-insertstring.md) нагрузки), соответствующий параметру *lParam* .</span><span class="sxs-lookup"><span data-stu-id="b47c0-123">Otherwise, **LB\_FINDSTRINGEXACT** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b47c0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b47c0-124">Requirements</span></span>



| <span data-ttu-id="b47c0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b47c0-125">Requirement</span></span> | <span data-ttu-id="b47c0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b47c0-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47c0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b47c0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b47c0-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b47c0-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b47c0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b47c0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b47c0-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b47c0-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b47c0-131">Header</span><span class="sxs-lookup"><span data-stu-id="b47c0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b47c0-132"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b47c0-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b47c0-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b47c0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b47c0-134">**FINDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="b47c0-134">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> </dl>

 

 





