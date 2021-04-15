---
title: Сообщение EM_GETFILELINE (Коммктрл. h)
description: Копирует строку текста из элемента управления "поле ввода" независимо от того, как линии отображаются на экране, и помещаются в указанный буфер.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Элементы управления Windows для EM_GETFILELINE сообщений
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491811"
---
# <a name="em_getfileline-message-commctrlh"></a><span data-ttu-id="5857f-104">Сообщение EM_GETFILELINE (Коммктрл. h)</span><span class="sxs-lookup"><span data-stu-id="5857f-104">EM_GETFILELINE message (CommCtrl.h)</span></span>

<span data-ttu-id="5857f-105">Копирует строку текста из элемента управления "поле ввода" независимо от того, как линии отображаются на экране, и помещаются в указанный буфер.</span><span class="sxs-lookup"><span data-stu-id="5857f-105">Copies a line of text from an edit control, independently of how lines are displayed on the screen, and places it in a specified buffer.</span></span>

## <a name="parameters"></a><span data-ttu-id="5857f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5857f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5857f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5857f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5857f-108">Отсчитываемый от нуля индекс строки, извлекаемой из многострочного элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="5857f-108">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="5857f-109">Нулевое значение задает верхнюю строку.</span><span class="sxs-lookup"><span data-stu-id="5857f-109">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="5857f-110">Этот параметр игнорируется с помощью однострочного элемента управления Edit.</span><span class="sxs-lookup"><span data-stu-id="5857f-110">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="5857f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5857f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5857f-112">Указатель на буфер, который получает копию строки.</span><span class="sxs-lookup"><span data-stu-id="5857f-112">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="5857f-113">Перед отправкой сообщения задайте для первого слова этого буфера размер буфера в **файле TCHAR**.</span><span class="sxs-lookup"><span data-stu-id="5857f-113">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="5857f-114">Для текста ANSI это число байтов; для текста в Юникоде это число символов.</span><span class="sxs-lookup"><span data-stu-id="5857f-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="5857f-115">Размер в первом слове перезаписывается скопированной строкой.</span><span class="sxs-lookup"><span data-stu-id="5857f-115">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5857f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5857f-116">Return value</span></span>

<span data-ttu-id="5857f-117">Возвращаемое значение — это число скопированных данных **TCHAR**.</span><span class="sxs-lookup"><span data-stu-id="5857f-117">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="5857f-118">Возвращаемое значение равно нулю, если номер строки, указанный параметром *wParam* , больше числа строк в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="5857f-118">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="5857f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5857f-119">Remarks</span></span>

<span data-ttu-id="5857f-120">Скопированная строка не содержит завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="5857f-120">The copied line does not contain a terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="5857f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5857f-121">Requirements</span></span>



| <span data-ttu-id="5857f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5857f-122">Requirement</span></span> | <span data-ttu-id="5857f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5857f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5857f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5857f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5857f-125">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="5857f-125">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5857f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5857f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5857f-127">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="5857f-127">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5857f-128">Header</span><span class="sxs-lookup"><span data-stu-id="5857f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5857f-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5857f-129"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5857f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5857f-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="5857f-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5857f-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5857f-132">**EM \_ филелинеленгс**</span><span class="sxs-lookup"><span data-stu-id="5857f-132">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="5857f-133">**Изменить \_ жетфилелине**</span><span class="sxs-lookup"><span data-stu-id="5857f-133">**Edit\_GetFileLine**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

<span data-ttu-id="5857f-134">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="5857f-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5857f-135">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="5857f-135">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

