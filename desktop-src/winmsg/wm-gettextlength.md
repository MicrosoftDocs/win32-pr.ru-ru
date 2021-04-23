---
description: Определяет длину текста, связанного с окном, в символах.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: Сообщение WM_GETTEXTLENGTH (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998931"
---
# <a name="wm_gettextlength-message"></a><span data-ttu-id="28b61-103">\_Сообщение ЖЕТТЕКСТЛЕНГС WM</span><span class="sxs-lookup"><span data-stu-id="28b61-103">WM\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="28b61-104">Определяет длину текста, связанного с окном, в символах.</span><span class="sxs-lookup"><span data-stu-id="28b61-104">Determines the length, in characters, of the text associated with a window.</span></span>


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a><span data-ttu-id="28b61-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="28b61-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28b61-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28b61-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28b61-107">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="28b61-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="28b61-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28b61-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28b61-109">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="28b61-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28b61-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28b61-110">Return value</span></span>

<span data-ttu-id="28b61-111">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="28b61-111">Type: **LRESULT**</span></span>

<span data-ttu-id="28b61-112">Возвращаемое значение — это длина текста в символах, не включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="28b61-112">The return value is the length of the text in characters, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="28b61-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28b61-113">Remarks</span></span>

<span data-ttu-id="28b61-114">Для элемента управления "поле ввода" копируемый текст является содержимым элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="28b61-114">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="28b61-115">Для поля со списком текст — это содержимое части элемента управления Edit (или статического текста) поля со списком.</span><span class="sxs-lookup"><span data-stu-id="28b61-115">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="28b61-116">Для кнопки текст — это имя кнопки.</span><span class="sxs-lookup"><span data-stu-id="28b61-116">For a button, the text is the button name.</span></span> <span data-ttu-id="28b61-117">Для других окон текст — это заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="28b61-117">For other windows, the text is the window title.</span></span> <span data-ttu-id="28b61-118">Чтобы определить длину элемента в поле со списком, приложение может использовать сообщение [**\_ жеттекстлен балансировки нагрузки**](../controls/lb-gettextlen.md) .</span><span class="sxs-lookup"><span data-stu-id="28b61-118">To determine the length of an item in a list box, an application can use the [**LB\_GETTEXTLEN**](../controls/lb-gettextlen.md) message.</span></span>

<span data-ttu-id="28b61-119">При отправке сообщения **WM \_ Жеттекстленгс** функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает длину текста в символах.</span><span class="sxs-lookup"><span data-stu-id="28b61-119">When the **WM\_GETTEXTLENGTH** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns the length, in characters, of the text.</span></span> <span data-ttu-id="28b61-120">При определенных условиях функция **дефвиндовпрок** возвращает значение, которое больше фактической длины текста.</span><span class="sxs-lookup"><span data-stu-id="28b61-120">Under certain conditions, the **DefWindowProc** function returns a value that is larger than the actual length of the text.</span></span> <span data-ttu-id="28b61-121">Это происходит с определенными сочетаниями ANSI и Unicode, и из-за системы, позволяющей обеспечить возможность существования символов двухбайтовой кодировки (DBCS) в тексте.</span><span class="sxs-lookup"><span data-stu-id="28b61-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="28b61-122">Однако возвращаемое значение всегда будет иметь размер по крайней мере такой же, как и фактическая длина текста. Таким же, вы всегда можете использовать его для выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="28b61-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="28b61-123">Такое поведение может возникать, если приложение использует как функции ANSI, так и общие диалоговые окна, использующие Юникод.</span><span class="sxs-lookup"><span data-stu-id="28b61-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="28b61-124">Чтобы получить точную длину текста, используйте сообщения [**WM \_**](wm-gettext.md)GetText, [**фунтового \_ текста**](../controls/lb-gettext.md)или [**CB \_ жетлбтекст**](../controls/cb-getlbtext.md) или функцию [**жетвиндовтекст**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="28b61-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](wm-gettext.md), [**LB\_GETTEXT**](../controls/lb-gettext.md), or [**CB\_GETLBTEXT**](../controls/cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="28b61-125">Отправка сообщения **WM \_ жеттекстленгс** в статический элемент управления, не являющийся текстовым, например статический точечный рисунок или статический значок контролк, не возвращает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="28b61-125">Sending a **WM\_GETTEXTLENGTH** message to a non-text static control, such as a static bitmap or static icon controlc, does not return a string value.</span></span> <span data-ttu-id="28b61-126">Вместо этого он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="28b61-126">Instead, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="28b61-127">Требования</span><span class="sxs-lookup"><span data-stu-id="28b61-127">Requirements</span></span>



| <span data-ttu-id="28b61-128">Требование</span><span class="sxs-lookup"><span data-stu-id="28b61-128">Requirement</span></span> | <span data-ttu-id="28b61-129">Значение</span><span class="sxs-lookup"><span data-stu-id="28b61-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28b61-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28b61-130">Minimum supported client</span></span><br/> | <span data-ttu-id="28b61-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28b61-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="28b61-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28b61-132">Minimum supported server</span></span><br/> | <span data-ttu-id="28b61-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28b61-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="28b61-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="28b61-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="28b61-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28b61-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28b61-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28b61-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="28b61-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="28b61-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="28b61-138">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="28b61-138">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="28b61-139">**жетвиндовтекст**</span><span class="sxs-lookup"><span data-stu-id="28b61-139">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="28b61-140">**жетвиндовтекстленгс**</span><span class="sxs-lookup"><span data-stu-id="28b61-140">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="28b61-141">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="28b61-141">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="28b61-142">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="28b61-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="28b61-143">Windows</span><span class="sxs-lookup"><span data-stu-id="28b61-143">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="28b61-144">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="28b61-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="28b61-145">**\_ЖЕТЛБТЕКСТ CB**</span><span class="sxs-lookup"><span data-stu-id="28b61-145">**CB\_GETLBTEXT**</span></span>](../controls/cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="28b61-146">**\_Балансировка нагрузки**</span><span class="sxs-lookup"><span data-stu-id="28b61-146">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> <dt>

[<span data-ttu-id="28b61-147">**жеттекстлен балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="28b61-147">**LB\_GETTEXTLEN**</span></span>](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
