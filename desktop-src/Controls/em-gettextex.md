---
title: Сообщение EM_GETTEXTEX (RichEdit. h)
description: Возвращает текст из элемента управления Rich Edit.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- Элементы управления Windows для EM_GETTEXTEX сообщений
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490371"
---
# <a name="em_gettextex-message"></a><span data-ttu-id="80327-104">\_Сообщение ЖЕТТЕКСТЕКС EM</span><span class="sxs-lookup"><span data-stu-id="80327-104">EM\_GETTEXTEX message</span></span>

<span data-ttu-id="80327-105">Возвращает текст из элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="80327-105">Gets the text from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="80327-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80327-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80327-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80327-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80327-108">Указатель на структуру [**жеттекстекс**](/windows/desktop/api/Richedit/ns-richedit-gettextex) , которая указывает, как перевести текст перед помещением в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="80327-108">Pointer to a [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure, which indicates how to translate the text before putting it into the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="80327-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80327-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80327-110">Указатель на буфер для получения текста.</span><span class="sxs-lookup"><span data-stu-id="80327-110">Pointer to the buffer to receive the text.</span></span> <span data-ttu-id="80327-111">Размер этого буфера в байтах указывается членом **CB** структуры [**жеттекстекс**](/windows/desktop/api/Richedit/ns-richedit-gettextex) .</span><span class="sxs-lookup"><span data-stu-id="80327-111">The size of this buffer, in bytes, is specified by the **cb** member of the [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure.</span></span> <span data-ttu-id="80327-112">Чтобы получить требуемый размер буфера, используйте сообщение [**EM \_ жеттекстленгсекс**](em-gettextlengthex.md) .</span><span class="sxs-lookup"><span data-stu-id="80327-112">Use the [**EM\_GETTEXTLENGTHEX**](em-gettextlengthex.md) message to get the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80327-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80327-113">Return value</span></span>

<span data-ttu-id="80327-114">Возвращаемое значение — это число файлов **TCHAR**, скопированных в выходной буфер, включая знак завершения null.</span><span class="sxs-lookup"><span data-stu-id="80327-114">The return value is the number of **TCHAR** s copied into the output buffer, including the null terminator.</span></span>

## <a name="remarks"></a><span data-ttu-id="80327-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80327-115">Remarks</span></span>

<span data-ttu-id="80327-116">Если размер выходного буфера меньше размера текста в элементе управления, элемент управления "поле ввода" скопирует текст с начала и поместит его в буфер до заполнения буфера.</span><span class="sxs-lookup"><span data-stu-id="80327-116">If the size of the output buffer is less than the size of the text in the control, the edit control will copy text from its beginning and place it in the buffer until the buffer is full.</span></span> <span data-ttu-id="80327-117">Завершающий нуль-символ все равно будет помещен в конец буфера.</span><span class="sxs-lookup"><span data-stu-id="80327-117">A terminating null character will still be placed at the end of the buffer.</span></span>

<span data-ttu-id="80327-118">Если запрашивается текст ANSI, **EM \_ жеттекстекс** использует функцию [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) для преобразования символов Юникода в ANSI.</span><span class="sxs-lookup"><span data-stu-id="80327-118">If ANSI text is requested, **EM\_GETTEXTEX** uses the [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function to translate the Unicode characters to ANSI.</span></span> <span data-ttu-id="80327-119">Он позволяет переходить из Юникода в ANSI с помощью определенной кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="80327-119">It allows you to go from Unicode to ANSI using a particular code page.</span></span> <span data-ttu-id="80327-120">Структура [**жеттекстекс**](/windows/desktop/api/Richedit/ns-richedit-gettextex) содержит элементы (**лпдефаултчар** и **лпуседдефчар**), которые используются при переводе из Юникода в ANSI.</span><span class="sxs-lookup"><span data-stu-id="80327-120">The [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure contains members (**lpDefaultChar** and **lpUsedDefChar**) that are used in the translation from Unicode to ANSI.</span></span>

## <a name="requirements"></a><span data-ttu-id="80327-121">Требования</span><span class="sxs-lookup"><span data-stu-id="80327-121">Requirements</span></span>



| <span data-ttu-id="80327-122">Требование</span><span class="sxs-lookup"><span data-stu-id="80327-122">Requirement</span></span> | <span data-ttu-id="80327-123">Значение</span><span class="sxs-lookup"><span data-stu-id="80327-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80327-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80327-124">Minimum supported client</span></span><br/> | <span data-ttu-id="80327-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80327-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80327-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80327-126">Minimum supported server</span></span><br/> | <span data-ttu-id="80327-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="80327-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80327-128">Header</span><span class="sxs-lookup"><span data-stu-id="80327-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="80327-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="80327-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80327-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80327-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="80327-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="80327-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="80327-132">**EM \_ сеттекстекс**</span><span class="sxs-lookup"><span data-stu-id="80327-132">**EM\_SETTEXTEX**</span></span>](em-settextex.md)
</dt> <dt>

[<span data-ttu-id="80327-133">**жеттекстекс**</span><span class="sxs-lookup"><span data-stu-id="80327-133">**GETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

<span data-ttu-id="80327-134">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="80327-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="80327-135">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="80327-135">**WideCharToMultiByte**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[<span data-ttu-id="80327-136">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="80327-136">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

