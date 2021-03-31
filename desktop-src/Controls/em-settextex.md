---
title: Сообщение EM_SETTEXTEX (RichEdit. h)
description: Объединяет функциональные возможности \_ сообщений WM SETTEXT и EM \_ реплацесел и добавляет возможность задать текст с помощью кодовой страницы и использовать форматированный текст или обычный текст.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- Элементы управления Windows для EM_SETTEXTEX сообщений
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491202"
---
# <a name="em_settextex-message"></a><span data-ttu-id="4b82d-104">\_Сообщение СЕТТЕКСТЕКС EM</span><span class="sxs-lookup"><span data-stu-id="4b82d-104">EM\_SETTEXTEX message</span></span>

<span data-ttu-id="4b82d-105">Объединяет функциональные возможности сообщений [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) и [**EM \_ реплацесел**](em-replacesel.md) и добавляет возможность задать текст с помощью кодовой страницы и использовать форматированный текст или обычный текст.</span><span class="sxs-lookup"><span data-stu-id="4b82d-105">Combines the functionality of the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) and [**EM\_REPLACESEL**](em-replacesel.md) messages, and adds the ability to set text using a code page and to use either rich text or plain text.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b82d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b82d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b82d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b82d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b82d-108">Указатель на структуру [**сеттекстекс**](/windows/desktop/api/Richedit/ns-richedit-settextex) , которая указывает флаги и дополнительную кодовую страницу для использования при преобразовании в Юникод.</span><span class="sxs-lookup"><span data-stu-id="4b82d-108">Pointer to a [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) structure that specifies flags and an optional code page to use in translating to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="4b82d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b82d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b82d-110">Указатель на текст, заканчивающийся нулем, для вставки.</span><span class="sxs-lookup"><span data-stu-id="4b82d-110">Pointer to the null-terminated text to insert.</span></span> <span data-ttu-id="4b82d-111">Этот текст является строкой ANSI, если только кодовая страница не 1200 (Unicode).</span><span class="sxs-lookup"><span data-stu-id="4b82d-111">This text is an ANSI string, unless the code page is 1200 (Unicode).</span></span> <span data-ttu-id="4b82d-112">Если параметр *lParam* начинается с допустимой ASCII-последовательности RTF (например, "{ \\ RTF" или "{уртф"), текст считывается в с помощью средства чтения RTF.</span><span class="sxs-lookup"><span data-stu-id="4b82d-112">If *lParam* starts with a valid RTF ASCII sequence for example, "{\\rtf" or "{urtf" the text is read in using the RTF reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b82d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b82d-113">Return value</span></span>

<span data-ttu-id="4b82d-114">Если операция устанавливает весь текст и выполняется удачно, возвращается значение 1.</span><span class="sxs-lookup"><span data-stu-id="4b82d-114">If the operation is setting all of the text and succeeds, the return value is 1.</span></span>

<span data-ttu-id="4b82d-115">Если операция устанавливает выделение и выполняется, возвращаемое значение представляет собой число скопированных байтов или символов.</span><span class="sxs-lookup"><span data-stu-id="4b82d-115">If the operation is setting the selection and succeeds, the return value is the number of bytes or characters copied.</span></span>

<span data-ttu-id="4b82d-116">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="4b82d-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b82d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4b82d-117">Requirements</span></span>



| <span data-ttu-id="4b82d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4b82d-118">Requirement</span></span> | <span data-ttu-id="4b82d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4b82d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b82d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b82d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4b82d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b82d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b82d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b82d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4b82d-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b82d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b82d-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4b82d-124">Redistributable</span></span><br/>          | <span data-ttu-id="4b82d-125">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="4b82d-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="4b82d-126">Header</span><span class="sxs-lookup"><span data-stu-id="4b82d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b82d-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b82d-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b82d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b82d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b82d-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="4b82d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4b82d-130">**EM \_ жеттекстекс**</span><span class="sxs-lookup"><span data-stu-id="4b82d-130">**EM\_GETTEXTEX**</span></span>](em-gettextex.md)
</dt> <dt>

[<span data-ttu-id="4b82d-131">**сеттекстекс**</span><span class="sxs-lookup"><span data-stu-id="4b82d-131">**SETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

