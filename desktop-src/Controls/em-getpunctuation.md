---
title: Сообщение EM_GETPUNCTUATION (RichEdit. h)
description: Возвращает текущие знаки пунктуации для элемента управления Rich Edit.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- Элементы управления Windows для EM_GETPUNCTUATION сообщений
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136978"
---
# <a name="em_getpunctuation-message"></a><span data-ttu-id="3c6b2-104">\_Сообщение EM</span><span class="sxs-lookup"><span data-stu-id="3c6b2-104">EM\_GETPUNCTUATION message</span></span>

<span data-ttu-id="3c6b2-105">Возвращает текущие знаки пунктуации для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3c6b2-105">Gets the current punctuation characters for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="3c6b2-106">Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки.</span><span class="sxs-lookup"><span data-stu-id="3c6b2-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="3c6b2-107">Он не поддерживается в каких-либо более поздних версиях расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="3c6b2-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="3c6b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c6b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c6b2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c6b2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6b2-110">Тип пунктуации может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3c6b2-110">The punctuation type can be one of the following values.</span></span>



| <span data-ttu-id="3c6b2-111">Значение</span><span class="sxs-lookup"><span data-stu-id="3c6b2-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="3c6b2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3c6b2-112">Meaning</span></span>                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="3c6b2-113"><dt>**\_ведущий ПК**</dt></span><span class="sxs-lookup"><span data-stu-id="3c6b2-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="3c6b2-114">Начальные знаки пунктуации</span><span class="sxs-lookup"><span data-stu-id="3c6b2-114">Leading punctuation characters</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="3c6b2-115"><dt>**ПК \_ ниже**</dt></span><span class="sxs-lookup"><span data-stu-id="3c6b2-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="3c6b2-116">Следующие знаки пунктуации</span><span class="sxs-lookup"><span data-stu-id="3c6b2-116">Following punctuation characters</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="3c6b2-117"><dt>**\_Разделитель компьютеров**</dt></span><span class="sxs-lookup"><span data-stu-id="3c6b2-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="3c6b2-118">Разделитель</span><span class="sxs-lookup"><span data-stu-id="3c6b2-118">Delimiter</span></span><br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <span data-ttu-id="3c6b2-119"><dt>**\_переполнение ПК**</dt></span><span class="sxs-lookup"><span data-stu-id="3c6b2-119"><dt>**PC\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="3c6b2-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3c6b2-120">Not supported</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="3c6b2-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c6b2-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6b2-122">Указатель на структуру [**пунктуации**](/windows/desktop/api/Richedit/ns-richedit-punctuation) , которая получает символы пунктуации.</span><span class="sxs-lookup"><span data-stu-id="3c6b2-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that receives the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c6b2-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c6b2-123">Return value</span></span>

<span data-ttu-id="3c6b2-124">Если операция завершилась удачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="3c6b2-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3c6b2-125">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="3c6b2-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c6b2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3c6b2-126">Requirements</span></span>



| <span data-ttu-id="3c6b2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3c6b2-127">Requirement</span></span> | <span data-ttu-id="3c6b2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3c6b2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c6b2-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c6b2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3c6b2-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c6b2-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c6b2-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c6b2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3c6b2-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c6b2-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c6b2-133">Header</span><span class="sxs-lookup"><span data-stu-id="3c6b2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c6b2-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c6b2-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c6b2-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c6b2-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c6b2-136">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3c6b2-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3c6b2-137">**EM \_ сетпунктуатион**</span><span class="sxs-lookup"><span data-stu-id="3c6b2-137">**EM\_SETPUNCTUATION**</span></span>](em-setpunctuation.md)
</dt> <dt>

[<span data-ttu-id="3c6b2-138">**ЗНАКИ ПРЕПИНАНИЯ**</span><span class="sxs-lookup"><span data-stu-id="3c6b2-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





