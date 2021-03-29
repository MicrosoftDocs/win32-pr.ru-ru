---
title: Сообщение LB_FINDSTRING (Winuser. h)
description: Находит первую строку в списке, которая начинается с указанной строки.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- Элементы управления Windows для LB_FINDSTRING сообщений
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b528dbafbc386af05a091f24c8c28327739f5d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492858"
---
# <a name="lb_findstring-message"></a><span data-ttu-id="6cc0f-104">Сообщение FINDSTRING балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="6cc0f-104">LB\_FINDSTRING message</span></span>

<span data-ttu-id="6cc0f-105">Находит первую строку в списке, которая начинается с указанной строки.</span><span class="sxs-lookup"><span data-stu-id="6cc0f-105">Finds the first string in a list box that begins with the specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cc0f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cc0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc0f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cc0f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc0f-108">Индекс элемента перед первым искомым элементом (индексация ведется от нуля).</span><span class="sxs-lookup"><span data-stu-id="6cc0f-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="6cc0f-109">Когда поиск достигает нижнего края списка, он продолжит поиск в верхней части окна списка назад к элементу, указанному параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="6cc0f-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="6cc0f-110">Если параметр *wParam* имеет значение-1, поиск выполняется по всему списку с самого начала.</span><span class="sxs-lookup"><span data-stu-id="6cc0f-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="6cc0f-111">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="6cc0f-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="6cc0f-112">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="6cc0f-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="6cc0f-113">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="6cc0f-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="6cc0f-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cc0f-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc0f-115">Указатель на строку, завершающуюся нулем, которая содержит строку для поиска.</span><span class="sxs-lookup"><span data-stu-id="6cc0f-115">A pointer to the null-terminated string that contains the string for which to search.</span></span> <span data-ttu-id="6cc0f-116">Поиск не зависит от регистра, поэтому эта строка может содержать любое сочетание прописных и строчных букв.</span><span class="sxs-lookup"><span data-stu-id="6cc0f-116">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc0f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cc0f-117">Return value</span></span>

<span data-ttu-id="6cc0f-118">Возвращаемое значение — это индекс совпадающего элемента или ошибка балансировки нагрузки, \_ Если поиск завершился неудачно.</span><span class="sxs-lookup"><span data-stu-id="6cc0f-118">The return value is the index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cc0f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6cc0f-119">Remarks</span></span>

<span data-ttu-id="6cc0f-120">Если список имеет стиль, рисуемый владельцем, но не хасстрингс в [**стиле \_ фунта**](list-box-styles.md) , действие, выполняемое методом **балансировки нагрузки \_ FINDSTRING** , зависит от того, используется ли стиль [**\_ сортировки фунтов**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6cc0f-120">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="6cc0f-121">Если **используется \_ Сортировка фунтов** , система отправляет сообщения [**WM \_ компареитем**](wm-compareitem.md) владельцу списка, чтобы определить, какой элемент соответствует заданной строке.</span><span class="sxs-lookup"><span data-stu-id="6cc0f-121">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="6cc0f-122">В противном случае **Балансировка нагрузки \_ FINDSTRING** пытается найти элемент с длинным значением (предоставленным как параметр *lParam* сообщения [**\_ ADDSTRING**](lb-addstring.md) или [**\_ балансировки**](lb-insertstring.md) нагрузки), соответствующий параметру *lParam* .</span><span class="sxs-lookup"><span data-stu-id="6cc0f-122">Otherwise, **LB\_FINDSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc0f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6cc0f-123">Requirements</span></span>



| <span data-ttu-id="6cc0f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6cc0f-124">Requirement</span></span> | <span data-ttu-id="6cc0f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6cc0f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc0f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cc0f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc0f-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6cc0f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6cc0f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cc0f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc0f-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6cc0f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6cc0f-130">Header</span><span class="sxs-lookup"><span data-stu-id="6cc0f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cc0f-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cc0f-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cc0f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cc0f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc0f-133">**финдстринжексакт балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="6cc0f-133">**LB\_FINDSTRINGEXACT**</span></span>](lb-findstringexact.md)
</dt> </dl>

 

 





