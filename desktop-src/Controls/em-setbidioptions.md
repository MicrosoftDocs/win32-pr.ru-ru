---
title: Сообщение EM_SETBIDIOPTIONS (RichEdit. h)
description: В \_ сообщении EM сетбидиоптионс задается текущее состояние двунаправленных параметров в элементе управления Rich Edit.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- Элементы управления Windows для EM_SETBIDIOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137174"
---
# <a name="em_setbidioptions-message"></a><span data-ttu-id="388e0-104">\_Сообщение СЕТБИДИОПТИОНС EM</span><span class="sxs-lookup"><span data-stu-id="388e0-104">EM\_SETBIDIOPTIONS message</span></span>

<span data-ttu-id="388e0-105">В сообщении **EM \_ сетбидиоптионс** задается текущее состояние двунаправленных параметров в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="388e0-105">The **EM\_SETBIDIOPTIONS** message sets the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="388e0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="388e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="388e0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="388e0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="388e0-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="388e0-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="388e0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="388e0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="388e0-110">Указатель на структуру [**бидиоптионс**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) , которая указывает, как задать состояние двунаправленных параметров в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="388e0-110">Pointer to a [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that indicates how to set the state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="388e0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="388e0-111">Return value</span></span>

<span data-ttu-id="388e0-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="388e0-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="388e0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="388e0-113">Remarks</span></span>

<span data-ttu-id="388e0-114">Элемент управления "форматированный текст" должен быть в режиме обычного текста или **EM \_ сетбидиоптионс** не будет выполнять никаких действий.</span><span class="sxs-lookup"><span data-stu-id="388e0-114">The rich edit control must be in plain text mode or **EM\_SETBIDIOPTIONS** will not do anything.</span></span>

<span data-ttu-id="388e0-115">В обычных текстовых элементах управления **EM \_ сетбидиоптионс** автоматически определяет направление абзаца и (или) выравнивание на основе правил контекста.</span><span class="sxs-lookup"><span data-stu-id="388e0-115">In plain text controls, **EM\_SETBIDIOPTIONS** automatically determines the paragraph direction and/or alignment based on the context rules.</span></span> <span data-ttu-id="388e0-116">Эти правила определяют, что направление и (или) выравнивание являются производными от первого строгого символа в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="388e0-116">These rules state that the direction and/or alignment is derived from the first strong character in the control.</span></span> <span data-ttu-id="388e0-117">Надежный символ — это тот, от которого может быть определено направление текста (см. Стандарт Юникод версии 2,0).</span><span class="sxs-lookup"><span data-stu-id="388e0-117">A strong character is one from which text direction can be determined (see Unicode Standard version 2.0).</span></span> <span data-ttu-id="388e0-118">Направление абзаца и (или) выравнивание применяются к формату по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="388e0-118">The paragraph direction and/or alignment is applied to the default format.</span></span>

<span data-ttu-id="388e0-119">**EM \_ СЕТБИДИОПТИОНС** только переключает формат абзаца по умолчанию в RTL (справа налево), если находит символ RTL,</span><span class="sxs-lookup"><span data-stu-id="388e0-119">**EM\_SETBIDIOPTIONS** only switches the default paragraph format to RTL (right to left) if it finds an RTL character,</span></span>

## <a name="requirements"></a><span data-ttu-id="388e0-120">Требования</span><span class="sxs-lookup"><span data-stu-id="388e0-120">Requirements</span></span>



| <span data-ttu-id="388e0-121">Требование</span><span class="sxs-lookup"><span data-stu-id="388e0-121">Requirement</span></span> | <span data-ttu-id="388e0-122">Значение</span><span class="sxs-lookup"><span data-stu-id="388e0-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="388e0-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="388e0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="388e0-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="388e0-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="388e0-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="388e0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="388e0-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="388e0-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="388e0-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="388e0-127">Redistributable</span></span><br/>          | <span data-ttu-id="388e0-128">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="388e0-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="388e0-129">Header</span><span class="sxs-lookup"><span data-stu-id="388e0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="388e0-130"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="388e0-130"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="388e0-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="388e0-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="388e0-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="388e0-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="388e0-133">**бидиоптионс**</span><span class="sxs-lookup"><span data-stu-id="388e0-133">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="388e0-134">**EM \_ жетбидиоптионс**</span><span class="sxs-lookup"><span data-stu-id="388e0-134">**EM\_GETBIDIOPTIONS**</span></span>](em-getbidioptions.md)
</dt> </dl>

 

 





