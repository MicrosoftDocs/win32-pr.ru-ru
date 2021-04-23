---
title: Сообщение EM_FINDTEXTEX (RichEdit. h)
description: Поиск текста в элементе управления Rich Edit.
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- Элементы управления Windows для EM_FINDTEXTEX сообщений
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e52f7d51ee7a186a8a9e66f11884d6c2e9bca2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136262"
---
# <a name="em_findtextex-message"></a><span data-ttu-id="9d460-104">\_Сообщение ФИНДТЕКСТЕКС EM</span><span class="sxs-lookup"><span data-stu-id="9d460-104">EM\_FINDTEXTEX message</span></span>

<span data-ttu-id="9d460-105">Поиск текста в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9d460-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d460-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d460-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d460-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d460-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d460-108">Задает поведение операции поиска.</span><span class="sxs-lookup"><span data-stu-id="9d460-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="9d460-109">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9d460-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="9d460-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9d460-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="9d460-111">Значение</span><span class="sxs-lookup"><span data-stu-id="9d460-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="9d460-112"><dt>**FR \_ вниз**</dt></span><span class="sxs-lookup"><span data-stu-id="9d460-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="9d460-113">Microsoft Rich Edit 2,0 и более поздние версии: Если задано, поиск будет перенаправлен из **финдтекстекс. чрг. кпмин**; Если параметр не задан, поиск осуществляется в обратном направлении из **финдтекстекс. чрг. кпмин**.</span><span class="sxs-lookup"><span data-stu-id="9d460-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="9d460-114">Microsoft Rich Edit 1,0: флаг FR \_ Down не учитывается.</span><span class="sxs-lookup"><span data-stu-id="9d460-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="9d460-115">Поиск всегда перенаправлен.</span><span class="sxs-lookup"><span data-stu-id="9d460-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="9d460-116"><dt>**FR \_ матчалефхамза**</dt></span><span class="sxs-lookup"><span data-stu-id="9d460-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="9d460-117">Microsoft Rich Edit 3,0 и более поздние версии: Если задано, Поиск различает арабские и еврейские буквы с разными диакритическими знаками.</span><span class="sxs-lookup"><span data-stu-id="9d460-117">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic and Hebrew alefs with different accents.</span></span> <span data-ttu-id="9d460-118">Если значение не задано, все знаки Алиф будут сопоставляться только символом Алиф.</span><span class="sxs-lookup"><span data-stu-id="9d460-118">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="9d460-119"><dt>**FR \_ матчкасе**</dt></span><span class="sxs-lookup"><span data-stu-id="9d460-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="9d460-120">Если задано значение, операция поиска учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9d460-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="9d460-121">Если не задано, операция поиска не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9d460-121">If not set, the search operation is case-insensitive.</span></span> <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="9d460-122"><dt>**FR \_ матчдиак**</dt></span><span class="sxs-lookup"><span data-stu-id="9d460-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="9d460-123">Microsoft Rich Edit 3,0 и более поздние версии: Если задано, операция поиска учитывает арабские и иврит диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="9d460-123">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="9d460-124">Если не задано, диакритические знаки игнорируются.</span><span class="sxs-lookup"><span data-stu-id="9d460-124">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="9d460-125"><dt>**FR \_ матчкашида**</dt></span><span class="sxs-lookup"><span data-stu-id="9d460-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="9d460-126">Microsoft Rich Edit 3,0 и более поздние версии: Если задано, операция поиска учитывает арабский и Еврейский кашиды.</span><span class="sxs-lookup"><span data-stu-id="9d460-126">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew kashidas.</span></span> <span data-ttu-id="9d460-127">Если значение не задано, кашиды игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9d460-127">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="9d460-128"><dt>**FR \_ вхолеворд**</dt></span><span class="sxs-lookup"><span data-stu-id="9d460-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="9d460-129">Если задано значение, операция выполняет поиск только целых слов, соответствующих строке поиска.</span><span class="sxs-lookup"><span data-stu-id="9d460-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="9d460-130">Если значение не задано, операция также выполняет поиск фрагментов слов, соответствующих строке поиска.</span><span class="sxs-lookup"><span data-stu-id="9d460-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="9d460-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d460-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d460-132">Структура [**финдтекстекс**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , содержащая сведения об операции Find.</span><span class="sxs-lookup"><span data-stu-id="9d460-132">A [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d460-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d460-133">Return value</span></span>

<span data-ttu-id="9d460-134">Если целевая строка найдена, возвращаемое значение является Отсчитываемая от нуля позицией первого символа совпадения.</span><span class="sxs-lookup"><span data-stu-id="9d460-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="9d460-135">Если целевой объект не найден, возвращается значение-1.</span><span class="sxs-lookup"><span data-stu-id="9d460-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d460-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d460-136">Remarks</span></span>

<span data-ttu-id="9d460-137">Это сообщение используется для поиска строк ANSI.</span><span class="sxs-lookup"><span data-stu-id="9d460-137">Use this message to find ANSI strings.</span></span> <span data-ttu-id="9d460-138">Для Юникода используйте [**EM \_ финдтекстексв**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="9d460-138">For Unicode, use [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span>

<span data-ttu-id="9d460-139">Элемент **кпмин** в **финдтекстекс. чрг** всегда указывает начальную точку поиска, а **кпмакс** задает конечную точку.</span><span class="sxs-lookup"><span data-stu-id="9d460-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="9d460-140">При поиске в обратном направлении **кпмин** должно быть больше или равно **кпмакс**.</span><span class="sxs-lookup"><span data-stu-id="9d460-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="9d460-141">При поиске вперед значение-1 в **кпмакс** расширяет диапазон поиска до конца текста.</span><span class="sxs-lookup"><span data-stu-id="9d460-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="9d460-142">Если операция поиска находит совпадение, элемент **чргтекст** структуры [**финдтекстекс**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) возвращает диапазон позиций символов, содержащих соответствующий текст.</span><span class="sxs-lookup"><span data-stu-id="9d460-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d460-143">Требования</span><span class="sxs-lookup"><span data-stu-id="9d460-143">Requirements</span></span>



| <span data-ttu-id="9d460-144">Требование</span><span class="sxs-lookup"><span data-stu-id="9d460-144">Requirement</span></span> | <span data-ttu-id="9d460-145">Значение</span><span class="sxs-lookup"><span data-stu-id="9d460-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d460-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d460-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9d460-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d460-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d460-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d460-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9d460-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9d460-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d460-150">Header</span><span class="sxs-lookup"><span data-stu-id="9d460-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d460-151"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d460-151"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d460-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d460-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d460-153">**EM \_ строки FindText**</span><span class="sxs-lookup"><span data-stu-id="9d460-153">**EM\_FINDTEXT**</span></span>](em-findtext.md)
</dt> </dl>

 

 





