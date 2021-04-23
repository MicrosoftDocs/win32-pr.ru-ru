---
title: Сообщение LB_GETTEXTLEN (Winuser. h)
description: Возвращает длину строки в поле со списком.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- Элементы управления Windows для LB_GETTEXTLEN сообщений
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135718"
---
# <a name="lb_gettextlen-message"></a><span data-ttu-id="c2e8d-104">Сообщение жеттекстлен балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="c2e8d-104">LB\_GETTEXTLEN message</span></span>

<span data-ttu-id="c2e8d-105">Возвращает длину строки в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-105">Gets the length of a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2e8d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2e8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e8d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2e8d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2e8d-108">Отсчитываемый от нуля индекс строки.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-108">The zero-based index of the string.</span></span>

<span data-ttu-id="c2e8d-109">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="c2e8d-110">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="c2e8d-111">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="c2e8d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2e8d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2e8d-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e8d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2e8d-114">Return value</span></span>

<span data-ttu-id="c2e8d-115">Возвращаемое значение — это длина строки в **файле TCHAR** s, исключая завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="c2e8d-116">При определенных условиях это значение может фактически превышать длину текста.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-116">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="c2e8d-117">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="c2e8d-117">For more information, see the following Remarks section.</span></span>

<span data-ttu-id="c2e8d-118">Если параметр *wParam* не указывает допустимый индекс, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-118">If the *wParam* parameter does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2e8d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2e8d-119">Remarks</span></span>

<span data-ttu-id="c2e8d-120">При определенных условиях возвращаемое значение больше фактической длины текста.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-120">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="c2e8d-121">Это происходит с определенными сочетаниями ANSI и Unicode и связано с тем, что операционная система допускает наличие в тексте символов двухбайтовой кодировки (DBCS).</span><span class="sxs-lookup"><span data-stu-id="c2e8d-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="c2e8d-122">Однако возвращаемое значение всегда будет иметь размер по крайней мере такой же, как и фактическая длина текста. Таким же, вы всегда можете использовать его для выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="c2e8d-123">Такое поведение может возникать, если приложение использует как функции ANSI, так и общие диалоговые окна, использующие Юникод.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="c2e8d-124">Чтобы получить точную длину текста, используйте сообщения [**WM \_**](/windows/desktop/winmsg/wm-gettext)GetText, [**фунтового \_ текста**](lb-gettext.md)или [**CB \_ жетлбтекст**](cb-getlbtext.md) или функцию [**жетвиндовтекст**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="c2e8d-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="c2e8d-125">Если список имеет стиль, рисуемый владельцем, но не хасстрингс в стиле [**фунта \_**](list-box-styles.md) , то возвращаемое значение всегда будет иметь размер в байтах типа **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-125">If the list box has an owner-drawn style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the return value is always the size, in bytes, of a **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e8d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c2e8d-126">Requirements</span></span>



| <span data-ttu-id="c2e8d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c2e8d-127">Requirement</span></span> | <span data-ttu-id="c2e8d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c2e8d-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e8d-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2e8d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e8d-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2e8d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c2e8d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2e8d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e8d-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2e8d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c2e8d-133">Header</span><span class="sxs-lookup"><span data-stu-id="c2e8d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2e8d-134"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2e8d-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e8d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2e8d-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2e8d-136">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c2e8d-137">**\_ЖЕТЛБТЕКСТ CB**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-137">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="c2e8d-138">**\_Балансировка нагрузки**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-138">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="c2e8d-139">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c2e8d-140">**жетвиндовтекст**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-140">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="c2e8d-141">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

