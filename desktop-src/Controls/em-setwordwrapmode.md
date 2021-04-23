---
title: Сообщение EM_SETWORDWRAPMODE (RichEdit. h)
description: Задает параметры разбиения по словам и переноса слов для элемента управления расширенного редактирования.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- Элементы управления Windows для EM_SETWORDWRAPMODE сообщений
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071737"
---
# <a name="em_setwordwrapmode-message"></a><span data-ttu-id="f3818-104">\_Сообщение СЕТВОРДВРАПМОДЕ EM</span><span class="sxs-lookup"><span data-stu-id="f3818-104">EM\_SETWORDWRAPMODE message</span></span>

<span data-ttu-id="f3818-105">Задает параметры разбиения по словам и переноса слов для элемента управления расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="f3818-105">Sets the word-wrapping and word-breaking options for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="f3818-106">Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки.</span><span class="sxs-lookup"><span data-stu-id="f3818-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="f3818-107">Он не поддерживается в каких-либо более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="f3818-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="f3818-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3818-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3818-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3818-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3818-110">Задает одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f3818-110">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="f3818-111">Значение</span><span class="sxs-lookup"><span data-stu-id="f3818-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="f3818-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f3818-112">Meaning</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <span data-ttu-id="f3818-113"><dt>**ВБФ переносить по \_ словам**</dt></span><span class="sxs-lookup"><span data-stu-id="f3818-113"><dt>**WBF\_WORDWRAP**</dt></span></span> </dl>    | <span data-ttu-id="f3818-114">Включает операции переноса по словам для восточноазиатских языков, например кинсоку на японском языке.</span><span class="sxs-lookup"><span data-stu-id="f3818-114">Enables Asian-specific word wrap operations, such as kinsoku in Japanese.</span></span> <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <span data-ttu-id="f3818-115"><dt>**ВБФ \_ специализированные**</dt></span><span class="sxs-lookup"><span data-stu-id="f3818-115"><dt>**WBF\_WORDBREAK**</dt></span></span> </dl> | <span data-ttu-id="f3818-116">Включает операции разбиения по словам на английском языке в японском и китайском языках.</span><span class="sxs-lookup"><span data-stu-id="f3818-116">Enables English word-breaking operations in Japanese and Chinese.</span></span> <span data-ttu-id="f3818-117">Включает Ханжеул операцию разбиения на слова.</span><span class="sxs-lookup"><span data-stu-id="f3818-117">Enables Hangeul word-breaking operation.</span></span><br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <span data-ttu-id="f3818-118"><dt>**\_переполнение ВБФ**</dt></span><span class="sxs-lookup"><span data-stu-id="f3818-118"><dt>**WBF\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="f3818-119">Распознает знаки пунктуации переполнения.</span><span class="sxs-lookup"><span data-stu-id="f3818-119">Recognizes overflow punctuation.</span></span> <span data-ttu-id="f3818-120">(В настоящее время не поддерживается.)</span><span class="sxs-lookup"><span data-stu-id="f3818-120">(Not currently supported.)</span></span><br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <span data-ttu-id="f3818-121"><dt>**ВБФ \_ level1**</dt></span><span class="sxs-lookup"><span data-stu-id="f3818-121"><dt>**WBF\_LEVEL1**</dt></span></span> </dl>          | <span data-ttu-id="f3818-122">Устанавливает таблицу пунктуации уровня 1 в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3818-122">Sets the Level 1 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <span data-ttu-id="f3818-123"><dt>**ВБФ \_ level2**</dt></span><span class="sxs-lookup"><span data-stu-id="f3818-123"><dt>**WBF\_LEVEL2**</dt></span></span> </dl>          | <span data-ttu-id="f3818-124">Устанавливает таблицу пунктуации уровня 2 в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3818-124">Sets the Level 2 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <span data-ttu-id="f3818-125"><dt>**ВБФ \_ настраиваемый**</dt></span><span class="sxs-lookup"><span data-stu-id="f3818-125"><dt>**WBF\_CUSTOM**</dt></span></span> </dl>          | <span data-ttu-id="f3818-126">Задает определяемую приложением таблицу пунктуации.</span><span class="sxs-lookup"><span data-stu-id="f3818-126">Sets the application-defined punctuation table.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="f3818-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3818-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3818-128">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f3818-128">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3818-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3818-129">Return value</span></span>

<span data-ttu-id="f3818-130">Это сообщение возвращает текущие параметры переноса слов и разбиения на слова.</span><span class="sxs-lookup"><span data-stu-id="f3818-130">This message returns the current word-wrapping and word-breaking options.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3818-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3818-131">Remarks</span></span>

<span data-ttu-id="f3818-132">Это сообщение не должно отправляться приложением, заданным процедурой разбиения по словам.</span><span class="sxs-lookup"><span data-stu-id="f3818-132">This message must not be sent by the application defined word breaking procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3818-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f3818-133">Requirements</span></span>



| <span data-ttu-id="f3818-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f3818-134">Requirement</span></span> | <span data-ttu-id="f3818-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f3818-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3818-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3818-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f3818-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3818-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3818-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3818-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f3818-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f3818-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3818-140">Header</span><span class="sxs-lookup"><span data-stu-id="f3818-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3818-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3818-141"><dt>Richedit.h</dt></span></span> </dl> |



 

 





