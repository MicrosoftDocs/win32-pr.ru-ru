---
title: Сообщение EM_FINDTEXT (RichEdit. h)
description: Поиск текста в элементе управления Rich Edit.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- Элементы управления Windows для EM_FINDTEXT сообщений
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988831"
---
# <a name="em_findtext-message"></a><span data-ttu-id="06ca0-104">\_Сообщение строки FINDTEXT EM</span><span class="sxs-lookup"><span data-stu-id="06ca0-104">EM\_FINDTEXT message</span></span>

<span data-ttu-id="06ca0-105">Поиск текста в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="06ca0-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="06ca0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06ca0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06ca0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06ca0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06ca0-108">Укажите параметры операции поиска.</span><span class="sxs-lookup"><span data-stu-id="06ca0-108">Specify the parameters of the search operation.</span></span> <span data-ttu-id="06ca0-109">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="06ca0-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="06ca0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="06ca0-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="06ca0-111">Значение</span><span class="sxs-lookup"><span data-stu-id="06ca0-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="06ca0-112"><dt>**FR \_ вниз**</dt></span><span class="sxs-lookup"><span data-stu-id="06ca0-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="06ca0-113">Microsoft Rich Edit 2,0 и более поздние версии: Если задано, поиск производится от конца текущего выделения до конца документа.</span><span class="sxs-lookup"><span data-stu-id="06ca0-113">Microsoft Rich Edit 2.0 and later: If set, the search is from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="06ca0-114">Если значение не задано, поиск производится от конца текущего выделения до начала документа.</span><span class="sxs-lookup"><span data-stu-id="06ca0-114">If not set, the search is from the end of the current selection to the beginning of the document.</span></span> <br/> <span data-ttu-id="06ca0-115">Microsoft Rich Edit 1,0: флаг FR \_ Down не учитывается.</span><span class="sxs-lookup"><span data-stu-id="06ca0-115">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="06ca0-116">Поиск всегда производится от конца текущего выделения до конца документа.</span><span class="sxs-lookup"><span data-stu-id="06ca0-116">The search is always from the end of the current selection to the end of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="06ca0-117"><dt>**FR \_ матчалефхамза**</dt></span><span class="sxs-lookup"><span data-stu-id="06ca0-117"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="06ca0-118">Microsoft Rich Edit 3,0 и более поздние версии: Если задано, Поиск различает арабские Алиф с различными диакритическими знаками.</span><span class="sxs-lookup"><span data-stu-id="06ca0-118">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic alefs with different accents.</span></span> <span data-ttu-id="06ca0-119">Если значение не задано, все знаки Алиф будут сопоставляться только символом Алиф.</span><span class="sxs-lookup"><span data-stu-id="06ca0-119">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="06ca0-120"><dt>**FR \_ матчдиак**</dt></span><span class="sxs-lookup"><span data-stu-id="06ca0-120"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="06ca0-121">Microsoft Rich Edit 3,0 и более поздние версии: Если задано, операция поиска учитывает арабские и иврит диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="06ca0-121">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="06ca0-122">Если не задано, диакритические знаки игнорируются.</span><span class="sxs-lookup"><span data-stu-id="06ca0-122">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="06ca0-123"><dt>**FR \_ матчкашида**</dt></span><span class="sxs-lookup"><span data-stu-id="06ca0-123"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="06ca0-124">Microsoft Rich Edit 3,0 и более поздние версии: Если задано, операция поиска учитывает Арабский кашиды.</span><span class="sxs-lookup"><span data-stu-id="06ca0-124">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic kashidas.</span></span> <span data-ttu-id="06ca0-125">Если значение не задано, кашиды игнорируется.</span><span class="sxs-lookup"><span data-stu-id="06ca0-125">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <span data-ttu-id="06ca0-126"><dt>**FR \_ матчвидс**</dt></span><span class="sxs-lookup"><span data-stu-id="06ca0-126"><dt>**FR\_MATCHWIDTH**</dt></span></span> </dl>             | <span data-ttu-id="06ca0-127">Windows 8. Если задано значение, однобайтовые и двухбайтовые версии одного и того же символа считаются неравными.</span><span class="sxs-lookup"><span data-stu-id="06ca0-127">Windows 8: If set, single-byte and double-byte versions of the same character are considered to be not equal.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="06ca0-128"><dt>**FR \_ вхолеворд**</dt></span><span class="sxs-lookup"><span data-stu-id="06ca0-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="06ca0-129">Если задано значение, операция выполняет поиск только целых слов, соответствующих строке поиска.</span><span class="sxs-lookup"><span data-stu-id="06ca0-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="06ca0-130">Если значение не задано, операция также выполняет поиск фрагментов слов, соответствующих строке поиска.</span><span class="sxs-lookup"><span data-stu-id="06ca0-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="06ca0-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06ca0-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06ca0-132">Структура [**строки FindText**](/windows/win32/api/richedit/ns-richedit-findtexta) , содержащая сведения об операции Find.</span><span class="sxs-lookup"><span data-stu-id="06ca0-132">A [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06ca0-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06ca0-133">Return value</span></span>

<span data-ttu-id="06ca0-134">Если целевая строка найдена, возвращаемое значение является Отсчитываемая от нуля позицией первого символа совпадения.</span><span class="sxs-lookup"><span data-stu-id="06ca0-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="06ca0-135">Если целевой объект не найден, возвращается значение-1.</span><span class="sxs-lookup"><span data-stu-id="06ca0-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="06ca0-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06ca0-136">Remarks</span></span>

<span data-ttu-id="06ca0-137">Элемент **кпмин** в **строки FindText. чрг** всегда указывает начальную точку поиска, а **кпмакс** задает конечную точку.</span><span class="sxs-lookup"><span data-stu-id="06ca0-137">The **cpMin** member of **FINDTEXT.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="06ca0-138">При поиске в обратном направлении **кпмин** должно быть больше или равно **кпмакс**.</span><span class="sxs-lookup"><span data-stu-id="06ca0-138">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="06ca0-139">При поиске вперед значение-1 в **кпмакс** расширяет диапазон поиска до конца текста.</span><span class="sxs-lookup"><span data-stu-id="06ca0-139">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="06ca0-140">Требования</span><span class="sxs-lookup"><span data-stu-id="06ca0-140">Requirements</span></span>



| <span data-ttu-id="06ca0-141">Требование</span><span class="sxs-lookup"><span data-stu-id="06ca0-141">Requirement</span></span> | <span data-ttu-id="06ca0-142">Значение</span><span class="sxs-lookup"><span data-stu-id="06ca0-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06ca0-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06ca0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="06ca0-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06ca0-144">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06ca0-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06ca0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="06ca0-146">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06ca0-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06ca0-147">Header</span><span class="sxs-lookup"><span data-stu-id="06ca0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="06ca0-148"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="06ca0-148"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06ca0-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06ca0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06ca0-150">**СТРОКИ FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="06ca0-150">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





