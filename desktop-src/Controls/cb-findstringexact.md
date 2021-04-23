---
title: Сообщение CB_FINDSTRINGEXACT (Winuser. h)
description: Находит первую строку списка в поле со списком, совпадающей со строкой, указанной в параметре lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- Элементы управления Windows для CB_FINDSTRINGEXACT сообщений
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f70c56a5f13fffa8dfedebd13f9830c62ef941cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535657"
---
# <a name="cb_findstringexact-message"></a><span data-ttu-id="d1307-104">\_Сообщение ФИНДСТРИНЖЕКСАКТ CB</span><span class="sxs-lookup"><span data-stu-id="d1307-104">CB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="d1307-105">Находит первую строку списка в поле со списком, совпадающей со строкой, указанной в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="d1307-105">Finds the first list box string in a combo box that matches the string specified in the *lParam* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1307-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1307-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1307-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1307-108">Отсчитываемый от нуля индекс элемента, предшествующего первому элементу для поиска.</span><span class="sxs-lookup"><span data-stu-id="d1307-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="d1307-109">Когда поиск достигает нижнего края списка, он переходит от верхней части окна списка к элементу, указанному параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="d1307-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="d1307-110">Если параметр *wParam* имеет значение 1, поиск выполняется по всему списку с самого начала.</span><span class="sxs-lookup"><span data-stu-id="d1307-110">If *wParam* is  1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="d1307-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1307-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1307-112">Указатель на строку, завершающуюся нулем, для которой требуется выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="d1307-112">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="d1307-113">При поиске регистр не учитывается, поэтому эта строка может содержать любое сочетание прописных и строчных букв.</span><span class="sxs-lookup"><span data-stu-id="d1307-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1307-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1307-114">Return value</span></span>

<span data-ttu-id="d1307-115">Возвращаемое значение — это Отсчитываемый от нуля индекс соответствующего элемента.</span><span class="sxs-lookup"><span data-stu-id="d1307-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="d1307-116">Если поиск завершился неудачно, это значит, что это \_ Ошибка CB.</span><span class="sxs-lookup"><span data-stu-id="d1307-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1307-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1307-117">Remarks</span></span>

<span data-ttu-id="d1307-118">Эта функция завершается успешно, только если указанная строка и элемент поля со списком имеют одинаковую длину (за исключением завершающего нуль-символа) и тех же символов.</span><span class="sxs-lookup"><span data-stu-id="d1307-118">This function is successful only if the specified string and a combo box item have the same length (except for the terminating null character) and the same characters.</span></span>

<span data-ttu-id="d1307-119">Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , функциональные возможности сообщения **CB \_ финдстринжексакт** зависят от того, использует ли ваше приложение стиль [**\_ сортировки CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d1307-119">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the functionality of **CB\_FINDSTRINGEXACT** message depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="d1307-120">При использовании стиля **\_ сортировки CBS** сообщения [**WM \_ компареитем**](wm-compareitem.md) отправляются владельцу поля со списком, чтобы определить, какой элемент соответствует заданной строке.</span><span class="sxs-lookup"><span data-stu-id="d1307-120">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="d1307-121">Если вы не используете стиль **\_ сортировки CBS** , в сообщении **CB \_ финдстринжексакт** выполняется поиск элемента списка, соответствующего значению параметра *lParam* .</span><span class="sxs-lookup"><span data-stu-id="d1307-121">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRINGEXACT** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1307-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d1307-122">Requirements</span></span>



| <span data-ttu-id="d1307-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d1307-123">Requirement</span></span> | <span data-ttu-id="d1307-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d1307-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1307-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1307-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d1307-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1307-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d1307-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1307-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d1307-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1307-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1307-129">Header</span><span class="sxs-lookup"><span data-stu-id="d1307-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1307-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1307-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1307-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1307-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1307-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d1307-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1307-133">**\_FINDSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="d1307-133">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="d1307-134">**\_СЕЛЕКТСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="d1307-134">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="d1307-135">**WM \_ компареитем**</span><span class="sxs-lookup"><span data-stu-id="d1307-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





