---
title: Сообщение EM_SETPUNCTUATION (RichEdit. h)
description: Задает знаки пунктуации для элемента управления Rich Edit.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- Элементы управления Windows для EM_SETPUNCTUATION сообщений
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710392cee7f7a1fb04fce59d6549134255499172
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137158"
---
# <a name="em_setpunctuation-message"></a><span data-ttu-id="18bad-104">\_Сообщение СЕТПУНКТУАТИОН EM</span><span class="sxs-lookup"><span data-stu-id="18bad-104">EM\_SETPUNCTUATION message</span></span>

<span data-ttu-id="18bad-105">Задает знаки пунктуации для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="18bad-105">Sets the punctuation characters for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="18bad-106">Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки.</span><span class="sxs-lookup"><span data-stu-id="18bad-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="18bad-107">Он не поддерживается в каких-либо более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="18bad-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="18bad-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="18bad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18bad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18bad-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18bad-110">Указывает тип пунктуации, который может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="18bad-110">Specifies the punctuation type, which can be one of the following values.</span></span>



| <span data-ttu-id="18bad-111">Значение</span><span class="sxs-lookup"><span data-stu-id="18bad-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="18bad-112">Значение</span><span class="sxs-lookup"><span data-stu-id="18bad-112">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="18bad-113"><dt>**\_ведущий ПК**</dt></span><span class="sxs-lookup"><span data-stu-id="18bad-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="18bad-114">Начальные знаки пунктуации.</span><span class="sxs-lookup"><span data-stu-id="18bad-114">Leading punctuation characters.</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="18bad-115"><dt>**ПК \_ ниже**</dt></span><span class="sxs-lookup"><span data-stu-id="18bad-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="18bad-116">Следующие знаки пунктуации.</span><span class="sxs-lookup"><span data-stu-id="18bad-116">Following punctuation characters.</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="18bad-117"><dt>**\_Разделитель компьютеров**</dt></span><span class="sxs-lookup"><span data-stu-id="18bad-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="18bad-118">Разделитель.</span><span class="sxs-lookup"><span data-stu-id="18bad-118">Delimiter.</span></span><br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <span data-ttu-id="18bad-119"><dt>**ПК \_ ПЕРЕПОЛНЕНие**</dt></span><span class="sxs-lookup"><span data-stu-id="18bad-119"><dt>**PC\_OVERFLOW** </dt></span></span> </dl> | <span data-ttu-id="18bad-120">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="18bad-120">Not supported.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="18bad-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18bad-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18bad-122">Указатель на структуру [**пунктуации**](/windows/desktop/api/Richedit/ns-richedit-punctuation) , содержащую знаки препинания.</span><span class="sxs-lookup"><span data-stu-id="18bad-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that contains the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18bad-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18bad-123">Return value</span></span>

<span data-ttu-id="18bad-124">Если операция завершилась удачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="18bad-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="18bad-125">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="18bad-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="18bad-126">Требования</span><span class="sxs-lookup"><span data-stu-id="18bad-126">Requirements</span></span>



| <span data-ttu-id="18bad-127">Требование</span><span class="sxs-lookup"><span data-stu-id="18bad-127">Requirement</span></span> | <span data-ttu-id="18bad-128">Значение</span><span class="sxs-lookup"><span data-stu-id="18bad-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18bad-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18bad-129">Minimum supported client</span></span><br/> | <span data-ttu-id="18bad-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18bad-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18bad-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18bad-131">Minimum supported server</span></span><br/> | <span data-ttu-id="18bad-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="18bad-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18bad-133">Header</span><span class="sxs-lookup"><span data-stu-id="18bad-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="18bad-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="18bad-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18bad-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18bad-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="18bad-136">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="18bad-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18bad-137">**\_знаки EM**</span><span class="sxs-lookup"><span data-stu-id="18bad-137">**EM\_GETPUNCTUATION**</span></span>](em-getpunctuation.md)
</dt> <dt>

[<span data-ttu-id="18bad-138">**ЗНАКИ ПРЕПИНАНИЯ**</span><span class="sxs-lookup"><span data-stu-id="18bad-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





