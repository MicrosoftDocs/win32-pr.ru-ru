---
title: Сообщение CB_SELECTSTRING (Winuser. h)
description: Выполняет поиск элемента, который начинается с символов в указанной строке, в списке поля со списком. Если соответствующий элемент найден, он выбирается и копируется в элемент управления "поле ввода".
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- Элементы управления Windows для CB_SELECTSTRING сообщений
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071609"
---
# <a name="cb_selectstring-message"></a><span data-ttu-id="be7cc-105">\_Сообщение СЕЛЕКТСТРИНГ CB</span><span class="sxs-lookup"><span data-stu-id="be7cc-105">CB\_SELECTSTRING message</span></span>

<span data-ttu-id="be7cc-106">Выполняет поиск элемента, который начинается с символов в указанной строке, в списке поля со списком.</span><span class="sxs-lookup"><span data-stu-id="be7cc-106">Searches the list of a combo box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="be7cc-107">Если соответствующий элемент найден, он выбирается и копируется в элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="be7cc-107">If a matching item is found, it is selected and copied to the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="be7cc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="be7cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be7cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be7cc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be7cc-110">Отсчитываемый от нуля индекс элемента, предшествующего первому элементу для поиска.</span><span class="sxs-lookup"><span data-stu-id="be7cc-110">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="be7cc-111">Когда поиск достигает нижнего края списка, он переходит от верхней части списка к элементу, указанному параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="be7cc-111">When the search reaches the bottom of the list, it continues from the top of the list back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="be7cc-112">Если параметр *wParam* имеет значение-1, поиск выполняется по всему списку с самого начала.</span><span class="sxs-lookup"><span data-stu-id="be7cc-112">If *wParam* is -1, the entire list is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="be7cc-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be7cc-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be7cc-114">Указатель на строку, завершающуюся нулем, которая содержит символы для поиска.</span><span class="sxs-lookup"><span data-stu-id="be7cc-114">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="be7cc-115">При поиске регистр не учитывается, поэтому эта строка может содержать любое сочетание прописных и строчных букв.</span><span class="sxs-lookup"><span data-stu-id="be7cc-115">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be7cc-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be7cc-116">Return value</span></span>

<span data-ttu-id="be7cc-117">Если строка найдена, возвращаемое значение является индексом выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="be7cc-117">If the string is found, the return value is the index of the selected item.</span></span> <span data-ttu-id="be7cc-118">Если поиск завершается неудачно, возвращается значение CB \_ Err, а текущее выделение не изменяется.</span><span class="sxs-lookup"><span data-stu-id="be7cc-118">If the search is unsuccessful, the return value is CB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="be7cc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be7cc-119">Remarks</span></span>

<span data-ttu-id="be7cc-120">Строка выбирается только в том случае, если символы из начальной точки совпадают с символами в строке префикса.</span><span class="sxs-lookup"><span data-stu-id="be7cc-120">A string is selected only if the characters from the starting point match the characters in the prefix string.</span></span>

<span data-ttu-id="be7cc-121">Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , то то, что делает сообщение **\_ селектстринг CB** , зависит от того, используется ли стиль [**\_ сортировки CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="be7cc-121">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_SELECTSTRING** message does depends on whether you use the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="be7cc-122">Если используется **стиль \_ сортировки CBS** , система отправляет сообщения [**WM \_ компареитем**](wm-compareitem.md) владельцу поля со списком, чтобы определить, какой элемент соответствует заданной строке.</span><span class="sxs-lookup"><span data-stu-id="be7cc-122">If the **CBS\_SORT** style is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="be7cc-123">Если вы не используете стиль **\_ сортировки CBS** , **CB \_ Селектстринг** пытается сопоставить значение **DWORD** со значением параметра *lParam* .</span><span class="sxs-lookup"><span data-stu-id="be7cc-123">If you do not use the **CBS\_SORT** style, **CB\_SELECTSTRING** attempts to match the **DWORD** value against the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7cc-124">Требования</span><span class="sxs-lookup"><span data-stu-id="be7cc-124">Requirements</span></span>



| <span data-ttu-id="be7cc-125">Требование</span><span class="sxs-lookup"><span data-stu-id="be7cc-125">Requirement</span></span> | <span data-ttu-id="be7cc-126">Значение</span><span class="sxs-lookup"><span data-stu-id="be7cc-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be7cc-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be7cc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="be7cc-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be7cc-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="be7cc-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be7cc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="be7cc-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be7cc-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be7cc-131">Header</span><span class="sxs-lookup"><span data-stu-id="be7cc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="be7cc-132"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be7cc-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be7cc-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be7cc-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="be7cc-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="be7cc-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="be7cc-135">**\_FINDSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="be7cc-135">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="be7cc-136">**\_ФИНДСТРИНЖЕКСАКТ CB**</span><span class="sxs-lookup"><span data-stu-id="be7cc-136">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="be7cc-137">**\_СЕТКУРСЕЛ CB**</span><span class="sxs-lookup"><span data-stu-id="be7cc-137">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="be7cc-138">**WM \_ компареитем**</span><span class="sxs-lookup"><span data-stu-id="be7cc-138">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





