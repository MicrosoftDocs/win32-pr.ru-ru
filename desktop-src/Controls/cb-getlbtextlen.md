---
title: Сообщение CB_GETLBTEXTLEN (Winuser. h)
description: Возвращает длину строки (в символах) в списке поля со списком.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- Элементы управления Windows для CB_GETLBTEXTLEN сообщений
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988640"
---
# <a name="cb_getlbtextlen-message"></a><span data-ttu-id="0626e-104">\_Сообщение ЖЕТЛБТЕКСТЛЕН CB</span><span class="sxs-lookup"><span data-stu-id="0626e-104">CB\_GETLBTEXTLEN message</span></span>

<span data-ttu-id="0626e-105">Возвращает длину строки (в символах) в списке поля со списком.</span><span class="sxs-lookup"><span data-stu-id="0626e-105">Gets the length, in characters, of a string in the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="0626e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0626e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0626e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0626e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0626e-108">Отсчитываемый от нуля индекс строки.</span><span class="sxs-lookup"><span data-stu-id="0626e-108">The zero-based index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="0626e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0626e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0626e-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="0626e-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0626e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0626e-111">Return value</span></span>

<span data-ttu-id="0626e-112">Возвращаемое значение — это длина строки в **файле TCHAR** s, исключая завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="0626e-112">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="0626e-113">Если строка ANSI имеет значение, равное количеству байтов, и если это строка в Юникоде, то это число символов.</span><span class="sxs-lookup"><span data-stu-id="0626e-113">If an ANSI string this is the number of bytes, and if it is a Unicode string this is the number of characters.</span></span> <span data-ttu-id="0626e-114">При определенных условиях это значение может фактически превышать длину текста.</span><span class="sxs-lookup"><span data-stu-id="0626e-114">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="0626e-115">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="0626e-115">For more information, see the Remarks section.</span></span>

<span data-ttu-id="0626e-116">Если параметр *wParam* не указывает допустимый индекс, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="0626e-116">If the *wParam* parameter does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="0626e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0626e-117">Remarks</span></span>

<span data-ttu-id="0626e-118">При определенных условиях возвращаемое значение больше фактической длины текста.</span><span class="sxs-lookup"><span data-stu-id="0626e-118">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="0626e-119">Это происходит с определенными сочетаниями ANSI и Unicode и связано с тем, что операционная система допускает наличие в тексте символов двухбайтовой кодировки (DBCS).</span><span class="sxs-lookup"><span data-stu-id="0626e-119">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="0626e-120">Однако возвращаемое значение всегда будет иметь размер по крайней мере такой же, как и фактическая длина текста. Поэтому его всегда можно использовать для выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="0626e-120">The return value, however, will always be at least as large as the actual length of the text; so you can always use it to guide buffer allocation.</span></span> <span data-ttu-id="0626e-121">Такое поведение может возникать, если приложение использует как функции ANSI, так и общие диалоговые окна, использующие Юникод.</span><span class="sxs-lookup"><span data-stu-id="0626e-121">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="0626e-122">Чтобы получить точную длину текста, используйте сообщения [**WM \_**](/windows/desktop/winmsg/wm-gettext)GetText, [**фунтового \_ текста**](lb-gettext.md)или [**CB \_ жетлбтекст**](cb-getlbtext.md) или функцию [**жетвиндовтекст**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="0626e-122">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0626e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0626e-123">Requirements</span></span>



| <span data-ttu-id="0626e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0626e-124">Requirement</span></span> | <span data-ttu-id="0626e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0626e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0626e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0626e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0626e-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0626e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0626e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0626e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0626e-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0626e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0626e-130">Header</span><span class="sxs-lookup"><span data-stu-id="0626e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0626e-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0626e-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0626e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0626e-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="0626e-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="0626e-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0626e-134">**\_ЖЕТЛБТЕКСТ CB**</span><span class="sxs-lookup"><span data-stu-id="0626e-134">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="0626e-135">**\_Балансировка нагрузки**</span><span class="sxs-lookup"><span data-stu-id="0626e-135">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="0626e-136">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="0626e-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0626e-137">**жетвиндовтекст**</span><span class="sxs-lookup"><span data-stu-id="0626e-137">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="0626e-138">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="0626e-138">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

