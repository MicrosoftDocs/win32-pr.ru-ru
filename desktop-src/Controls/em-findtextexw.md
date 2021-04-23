---
title: Сообщение EM_FINDTEXTEXW (RichEdit. h)
description: Находит текст в Юникоде в элементе управления Rich Edit.
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- Элементы управления Windows для EM_FINDTEXTEXW сообщений
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf0857e47c6e98f4be6867ca66baef3472766a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989193"
---
# <a name="em_findtextexw-message"></a><span data-ttu-id="8c295-104">\_Сообщение ФИНДТЕКСТЕКСВ EM</span><span class="sxs-lookup"><span data-stu-id="8c295-104">EM\_FINDTEXTEXW message</span></span>

<span data-ttu-id="8c295-105">Находит текст в Юникоде в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8c295-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c295-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c295-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c295-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c295-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c295-108">Задает поведение операции поиска.</span><span class="sxs-lookup"><span data-stu-id="8c295-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="8c295-109">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8c295-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="8c295-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8c295-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="8c295-111">Значение</span><span class="sxs-lookup"><span data-stu-id="8c295-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="8c295-112"><dt>**FR \_ вниз**</dt></span><span class="sxs-lookup"><span data-stu-id="8c295-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="8c295-113">Microsoft Rich Edit 2,0 и более поздние версии: Если задано, поиск будет перенаправлен из **финдтекстекс. чрг. кпмин**; Если параметр не задан, поиск осуществляется в обратном направлении из **финдтекстекс. чрг. кпмин**.</span><span class="sxs-lookup"><span data-stu-id="8c295-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="8c295-114">Microsoft Rich Edit 1,0: флаг FR \_ Down не учитывается.</span><span class="sxs-lookup"><span data-stu-id="8c295-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="8c295-115">Поиск всегда перенаправлен.</span><span class="sxs-lookup"><span data-stu-id="8c295-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="8c295-116"><dt>**FR \_ матчалефхамза**</dt></span><span class="sxs-lookup"><span data-stu-id="8c295-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="8c295-117">Если задано значение, Поиск различается по знакам ударения с разными диакритическими линиями.</span><span class="sxs-lookup"><span data-stu-id="8c295-117">If set, the search differentiates between alefs with different accents.</span></span> <span data-ttu-id="8c295-118">Если не задано, Арабская и еврейская кавычки с разными диакритическими знаками совпадают с символом Алиф.</span><span class="sxs-lookup"><span data-stu-id="8c295-118">If not set, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="8c295-119"><dt>**FR \_ матчкасе**</dt></span><span class="sxs-lookup"><span data-stu-id="8c295-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="8c295-120">Если задано значение, операция поиска учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="8c295-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="8c295-121">Если не задано, операция поиска не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="8c295-121">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="8c295-122"><dt>**FR \_ матчдиак**</dt></span><span class="sxs-lookup"><span data-stu-id="8c295-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="8c295-123">Если задано, операция поиска считает диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="8c295-123">If set, the search operation considers diacritical marks.</span></span> <span data-ttu-id="8c295-124">Если не задано, арабские и иврит диакритические знаки игнорируются.</span><span class="sxs-lookup"><span data-stu-id="8c295-124">If not set, Arabic and Hebrew diacritical marks are ignored.</span></span> <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="8c295-125"><dt>**FR \_ матчкашида**</dt></span><span class="sxs-lookup"><span data-stu-id="8c295-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="8c295-126">Если задано, операция поиска считает кашиды.</span><span class="sxs-lookup"><span data-stu-id="8c295-126">If set, the search operation considers kashidas.</span></span> <span data-ttu-id="8c295-127">Если значение не задано, то Арабский и Еврейский кашиду игнорируются.</span><span class="sxs-lookup"><span data-stu-id="8c295-127">If not set, Arabic and Hebrew kashidas are ignored.</span></span> <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="8c295-128"><dt>**FR \_ вхолеворд**</dt></span><span class="sxs-lookup"><span data-stu-id="8c295-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="8c295-129">Если задано значение, операция выполняет поиск только целых слов, соответствующих строке поиска.</span><span class="sxs-lookup"><span data-stu-id="8c295-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="8c295-130">Если значение не задано, операция также выполняет поиск фрагментов слов, соответствующих строке поиска.</span><span class="sxs-lookup"><span data-stu-id="8c295-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="8c295-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c295-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c295-132">Структура [**финдтекстексв**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , содержащая сведения об операции Find.</span><span class="sxs-lookup"><span data-stu-id="8c295-132">A [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c295-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c295-133">Return value</span></span>

<span data-ttu-id="8c295-134">Если целевая строка найдена, возвращаемое значение является Отсчитываемая от нуля позицией первого символа совпадения.</span><span class="sxs-lookup"><span data-stu-id="8c295-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="8c295-135">Если целевой объект не найден, возвращается значение-1.</span><span class="sxs-lookup"><span data-stu-id="8c295-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c295-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c295-136">Remarks</span></span>

<span data-ttu-id="8c295-137">Это сообщение используется для поиска строк в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="8c295-137">Use this message to find Unicode strings.</span></span> <span data-ttu-id="8c295-138">Для ANSI; используйте [**EM \_ финдтекстекс**](em-findtextex.md).</span><span class="sxs-lookup"><span data-stu-id="8c295-138">For ANSI;, use [**EM\_FINDTEXTEX**](em-findtextex.md).</span></span>

<span data-ttu-id="8c295-139">Элемент **кпмин** в **финдтекстекс. чрг** всегда указывает начальную точку поиска, а **кпмакс** задает конечную точку.</span><span class="sxs-lookup"><span data-stu-id="8c295-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="8c295-140">При поиске в обратном направлении **кпмин** должно быть больше или равно **кпмакс**.</span><span class="sxs-lookup"><span data-stu-id="8c295-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="8c295-141">При поиске вперед значение-1 в **кпмакс** расширяет диапазон поиска до конца текста.</span><span class="sxs-lookup"><span data-stu-id="8c295-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="8c295-142">Если операция поиска находит совпадение, элемент **чргтекст** структуры [**финдтекстекс**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) возвращает диапазон позиций символов, содержащих соответствующий текст.</span><span class="sxs-lookup"><span data-stu-id="8c295-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

<span data-ttu-id="8c295-143">**EM \_ ФИНДТЕКСТЕКСВ** использует структуру [**финдтекстексв**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , а [**EM \_ финдтекств**](em-findtextw.md) использует структуру [**финдтекств**](/windows/win32/api/richedit/ns-richedit-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="8c295-143">**EM\_FINDTEXTEXW** uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, while [**EM\_FINDTEXTW**](em-findtextw.md) uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure.</span></span> <span data-ttu-id="8c295-144">Разница заключается в том, что **EM \_ финдтекстексв** сообщает диапазон найденного текста.</span><span class="sxs-lookup"><span data-stu-id="8c295-144">The difference is that **EM\_FINDTEXTEXW** reports the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c295-145">Требования</span><span class="sxs-lookup"><span data-stu-id="8c295-145">Requirements</span></span>



| <span data-ttu-id="8c295-146">Требование</span><span class="sxs-lookup"><span data-stu-id="8c295-146">Requirement</span></span> | <span data-ttu-id="8c295-147">Значение</span><span class="sxs-lookup"><span data-stu-id="8c295-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c295-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c295-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8c295-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c295-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c295-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c295-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8c295-151">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8c295-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c295-152">Header</span><span class="sxs-lookup"><span data-stu-id="8c295-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c295-153"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c295-153"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c295-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c295-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c295-155">**EM \_ финдтекств**</span><span class="sxs-lookup"><span data-stu-id="8c295-155">**EM\_FINDTEXTW**</span></span>](em-findtextw.md)
</dt> </dl>

 

 





