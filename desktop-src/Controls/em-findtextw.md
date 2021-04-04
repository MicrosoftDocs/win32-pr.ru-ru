---
title: Сообщение EM_FINDTEXTW (RichEdit. h)
description: Находит текст в Юникоде в элементе управления Rich Edit.
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- Элементы управления Windows для EM_FINDTEXTW сообщений
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803269"
---
# <a name="em_findtextw-message"></a><span data-ttu-id="97100-104">\_Сообщение ФИНДТЕКСТВ EM</span><span class="sxs-lookup"><span data-stu-id="97100-104">EM\_FINDTEXTW message</span></span>

<span data-ttu-id="97100-105">Находит текст в Юникоде в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="97100-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="97100-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97100-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97100-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97100-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97100-108">Задает параметры операции поиска.</span><span class="sxs-lookup"><span data-stu-id="97100-108">Specifies the parameters of the search operation.</span></span> <span data-ttu-id="97100-109">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="97100-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="97100-110">Значение</span><span class="sxs-lookup"><span data-stu-id="97100-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="97100-111">Значение</span><span class="sxs-lookup"><span data-stu-id="97100-111">Meaning</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="97100-112"><dt>**FR \_ вниз**</dt></span><span class="sxs-lookup"><span data-stu-id="97100-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="97100-113">Если задано значение, операция выполняет поиск с конца текущего выделения до конца документа.</span><span class="sxs-lookup"><span data-stu-id="97100-113">If set, the operation searches from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="97100-114">Если значение не задано, операция выполняет поиск с конца текущего выделения до начала документа.</span><span class="sxs-lookup"><span data-stu-id="97100-114">If not set, the operation searches from the end of the current selection to the beginning of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="97100-115"><dt>**FR \_ матчалефхамза**</dt></span><span class="sxs-lookup"><span data-stu-id="97100-115"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="97100-116">По умолчанию символы арабского и иврита с разными диакритическими знаками совпадают с символом Алиф.</span><span class="sxs-lookup"><span data-stu-id="97100-116">By default, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <span data-ttu-id="97100-117">Установите этот флажок, если необходимо, чтобы поиск отличался от Алеф с различными диакритическими знаками.</span><span class="sxs-lookup"><span data-stu-id="97100-117">Set this flag if you want the search to differentiate between alefs with different accents.</span></span><br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="97100-118"><dt>**FR \_ матчкасе**</dt></span><span class="sxs-lookup"><span data-stu-id="97100-118"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="97100-119">Если задано значение, операция поиска учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="97100-119">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="97100-120">Если не задано, операция поиска не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="97100-120">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="97100-121"><dt>**FR \_ матчдиак**</dt></span><span class="sxs-lookup"><span data-stu-id="97100-121"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="97100-122">По умолчанию арабские и иврит диакритические знаки игнорируются.</span><span class="sxs-lookup"><span data-stu-id="97100-122">By default, Arabic and Hebrew diacritical marks are ignored.</span></span> <span data-ttu-id="97100-123">Установите этот флаг, если необходимо, чтобы операция поиска рассматривала диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="97100-123">Set this flag if you want the search operation to consider diacritical marks.</span></span><br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="97100-124"><dt>**FR \_ матчкашида**</dt></span><span class="sxs-lookup"><span data-stu-id="97100-124"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="97100-125">По умолчанию арабский и Еврейский кашиды игнорируются.</span><span class="sxs-lookup"><span data-stu-id="97100-125">By default, Arabic and Hebrew kashidas are ignored.</span></span> <span data-ttu-id="97100-126">Установите этот флаг, если необходимо, чтобы операция поиска рассматривала кашиду.</span><span class="sxs-lookup"><span data-stu-id="97100-126">Set this flag if you want the search operation to consider kashidas.</span></span><br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="97100-127"><dt>**FR \_ вхолеворд**</dt></span><span class="sxs-lookup"><span data-stu-id="97100-127"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="97100-128">Если задано значение, операция выполняет поиск только целых слов, соответствующих строке поиска.</span><span class="sxs-lookup"><span data-stu-id="97100-128">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="97100-129">Если значение не задано, операция также выполняет поиск фрагментов слов, соответствующих строке поиска.</span><span class="sxs-lookup"><span data-stu-id="97100-129">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                  |



 

</dd> <dt>

<span data-ttu-id="97100-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97100-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97100-131">Структура [**финдтекств**](/windows/win32/api/richedit/ns-richedit-findtexta) , содержащая сведения об операции Find.</span><span class="sxs-lookup"><span data-stu-id="97100-131">A [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97100-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97100-132">Return value</span></span>

<span data-ttu-id="97100-133">Если целевая строка найдена, возвращаемое значение является Отсчитываемая от нуля позицией первого символа совпадения.</span><span class="sxs-lookup"><span data-stu-id="97100-133">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="97100-134">Если целевой объект не найден, возвращается значение-1.</span><span class="sxs-lookup"><span data-stu-id="97100-134">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="97100-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97100-135">Remarks</span></span>

<span data-ttu-id="97100-136">**EM \_ ФИНДТЕКСТВ** использует структуру [**финдтекств**](/windows/win32/api/richedit/ns-richedit-findtexta) , а [**EM \_ финдтекстексв**](em-findtextexw.md) использует структуру [**финдтекстексв**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) .</span><span class="sxs-lookup"><span data-stu-id="97100-136">**EM\_FINDTEXTW** uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure, while [**EM\_FINDTEXTEXW**](em-findtextexw.md) uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure.</span></span> <span data-ttu-id="97100-137">Разница заключается в том, что **финдтекстексв** сообщает о найденном диапазоне текста.</span><span class="sxs-lookup"><span data-stu-id="97100-137">The difference is that **FINDTEXTEXW** reports back the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="97100-138">Требования</span><span class="sxs-lookup"><span data-stu-id="97100-138">Requirements</span></span>



| <span data-ttu-id="97100-139">Требование</span><span class="sxs-lookup"><span data-stu-id="97100-139">Requirement</span></span> | <span data-ttu-id="97100-140">Значение</span><span class="sxs-lookup"><span data-stu-id="97100-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97100-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97100-141">Minimum supported client</span></span><br/> | <span data-ttu-id="97100-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97100-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97100-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97100-143">Minimum supported server</span></span><br/> | <span data-ttu-id="97100-144">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97100-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97100-145">Header</span><span class="sxs-lookup"><span data-stu-id="97100-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="97100-146"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="97100-146"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97100-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97100-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97100-148">**EM \_ финдтекстексв**</span><span class="sxs-lookup"><span data-stu-id="97100-148">**EM\_FINDTEXTEXW**</span></span>](em-findtextexw.md)
</dt> </dl>

 

 





