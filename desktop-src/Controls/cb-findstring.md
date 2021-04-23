---
title: Сообщение CB_FINDSTRING (Winuser. h)
description: Выполняет поиск элемента в списке в поле со списком, начиная с символов в указанной строке.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- Элементы управления Windows для CB_FINDSTRING сообщений
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135866"
---
# <a name="cb_findstring-message"></a><span data-ttu-id="b813b-104">\_Сообщение FINDSTRING CB</span><span class="sxs-lookup"><span data-stu-id="b813b-104">CB\_FINDSTRING message</span></span>

<span data-ttu-id="b813b-105">Выполняет поиск элемента в списке в поле со списком, начиная с символов в указанной строке.</span><span class="sxs-lookup"><span data-stu-id="b813b-105">Searches the list box of a combo box for an item beginning with the characters in a specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="b813b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b813b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b813b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b813b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b813b-108">Отсчитываемый от нуля индекс элемента, предшествующего первому элементу для поиска.</span><span class="sxs-lookup"><span data-stu-id="b813b-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="b813b-109">Когда поиск достигает нижнего края списка, он переходит от верхней части окна списка к элементу, указанному параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="b813b-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="b813b-110">Если параметр *wParam* имеет значение-1, поиск выполняется по всему списку с самого начала.</span><span class="sxs-lookup"><span data-stu-id="b813b-110">If *wParam* is  -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="b813b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b813b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b813b-112">Указатель на строку, завершающуюся нулем, которая содержит символы для поиска.</span><span class="sxs-lookup"><span data-stu-id="b813b-112">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="b813b-113">При поиске регистр не учитывается, поэтому эта строка может содержать любое сочетание прописных и строчных букв.</span><span class="sxs-lookup"><span data-stu-id="b813b-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b813b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b813b-114">Return value</span></span>

<span data-ttu-id="b813b-115">Возвращаемое значение — это Отсчитываемый от нуля индекс соответствующего элемента.</span><span class="sxs-lookup"><span data-stu-id="b813b-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="b813b-116">Если поиск завершился неудачно, это значит, что это \_ Ошибка CB.</span><span class="sxs-lookup"><span data-stu-id="b813b-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="b813b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b813b-117">Remarks</span></span>

<span data-ttu-id="b813b-118">Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , то то, что делает сообщение **\_ FINDSTRING CB** , зависит от того, использует ли ваше приложение стиль [**\_ сортировки CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b813b-118">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_FINDSTRING** message does depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="b813b-119">При использовании стиля **\_ сортировки CBS** сообщения [**WM \_ компареитем**](wm-compareitem.md) отправляются владельцу поля со списком, чтобы определить, какой элемент соответствует заданной строке.</span><span class="sxs-lookup"><span data-stu-id="b813b-119">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="b813b-120">Если вы не используете стиль **\_ сортировки CBS** , в сообщении **CB \_ FINDSTRING** выполняется поиск элемента списка, соответствующего значению параметра *lParam* .</span><span class="sxs-lookup"><span data-stu-id="b813b-120">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRING** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b813b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b813b-121">Requirements</span></span>



| <span data-ttu-id="b813b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b813b-122">Requirement</span></span> | <span data-ttu-id="b813b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b813b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b813b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b813b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b813b-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b813b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b813b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b813b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b813b-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b813b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b813b-128">Header</span><span class="sxs-lookup"><span data-stu-id="b813b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b813b-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b813b-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b813b-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b813b-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="b813b-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b813b-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b813b-132">**\_ФИНДСТРИНЖЕКСАКТ CB**</span><span class="sxs-lookup"><span data-stu-id="b813b-132">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="b813b-133">**\_СЕЛЕКТСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="b813b-133">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="b813b-134">**\_СЕТКУРСЕЛ CB**</span><span class="sxs-lookup"><span data-stu-id="b813b-134">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="b813b-135">**WM \_ компареитем**</span><span class="sxs-lookup"><span data-stu-id="b813b-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





