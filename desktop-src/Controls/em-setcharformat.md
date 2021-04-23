---
title: Сообщение EM_SETCHARFORMAT (RichEdit. h)
description: Задает форматирование символов в элементе управления Rich Edit.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- Элементы управления Windows для EM_SETCHARFORMAT сообщений
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137170"
---
# <a name="em_setcharformat-message"></a><span data-ttu-id="01960-104">\_Сообщение СЕТЧАРФОРМАТ EM</span><span class="sxs-lookup"><span data-stu-id="01960-104">EM\_SETCHARFORMAT message</span></span>

<span data-ttu-id="01960-105">Задает форматирование символов в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="01960-105">Sets character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="01960-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01960-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01960-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01960-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01960-108">Форматирование символов, которое применяется к элементу управления.</span><span class="sxs-lookup"><span data-stu-id="01960-108">Character formatting that applies to the control.</span></span> <span data-ttu-id="01960-109">Если этот параметр равен нулю, задается символьный формат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="01960-109">If this parameter is zero, the default character format is set.</span></span> <span data-ttu-id="01960-110">В противном случае может быть одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="01960-110">Otherwise, it can be one of the following values.</span></span>



| <span data-ttu-id="01960-111">Значение</span><span class="sxs-lookup"><span data-stu-id="01960-111">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="01960-112">Значение</span><span class="sxs-lookup"><span data-stu-id="01960-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <span data-ttu-id="01960-113"><dt>**SCF \_ все**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-113"><dt>**SCF\_ALL**</dt></span></span> </dl>                                     | <span data-ttu-id="01960-114">Применяет форматирование ко всему тексту в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="01960-114">Applies the formatting to all text in the control.</span></span> <span data-ttu-id="01960-115">Недопустимо при **\_ выборе SCF** или **в \_ слове SCF**.</span><span class="sxs-lookup"><span data-stu-id="01960-115">Not valid with **SCF\_SELECTION** or **SCF\_WORD**.</span></span><br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <span data-ttu-id="01960-116"><dt>**\_АССОЦИАТЕФОНТ SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-116"><dt>**SCF\_ASSOCIATEFONT**</dt></span></span> </dl>       | <span data-ttu-id="01960-117">**RichEdit 4,1:** Связывает шрифт с заданным сценарием, тем самым изменяя шрифт по умолчанию для этого скрипта.</span><span class="sxs-lookup"><span data-stu-id="01960-117">**RichEdit 4.1:** Associates a font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="01960-118">Чтобы указать шрифт, используйте следующие члены [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **ихеигхт**, **бчарсет**, **бпитчандфамили**, **сзфаценаме** и **LCID**.</span><span class="sxs-lookup"><span data-stu-id="01960-118">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <span data-ttu-id="01960-119"><dt>**\_ASSOCIATEFONT2 SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-119"><dt>**SCF\_ASSOCIATEFONT2**</dt></span></span> </dl>    | <span data-ttu-id="01960-120">**RichEdit 4,1:** Связывает шрифт суррогата (плоскость 2) с заданным сценарием, тем самым изменяя шрифт по умолчанию для этого скрипта.</span><span class="sxs-lookup"><span data-stu-id="01960-120">**RichEdit 4.1:** Associates a surrogate (plane-2) font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="01960-121">Чтобы указать шрифт, используйте следующие члены [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **ихеигхт**, **бчарсет**, **бпитчандфамили**, **сзфаценаме** и **LCID**.</span><span class="sxs-lookup"><span data-stu-id="01960-121">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <span data-ttu-id="01960-122"><dt>**\_ЧАРРЕПФРОМЛЦИД SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-122"><dt>**SCF\_CHARREPFROMLCID**</dt></span></span> </dl> | <span data-ttu-id="01960-123">Возвращает символ поработать из LCID.</span><span class="sxs-lookup"><span data-stu-id="01960-123">Gets the character repertoire from the LCID.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="01960-124"><dt>**\_по умолчанию — SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-124"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>                         | <span data-ttu-id="01960-125">**RichEdit 4,1:** Задает шрифт по умолчанию для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="01960-125">**RichEdit 4.1:** Sets the default font for the control.</span></span> <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <span data-ttu-id="01960-126"><dt>**SPF \_ донтсетдефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-126"><dt>**SPF\_DONTSETDEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="01960-127">Предотвращает задание формата абзаца по умолчанию, если элемент управления Rich Edit пуст.</span><span class="sxs-lookup"><span data-stu-id="01960-127">Prevents setting the default paragraph format when the rich edit control is empty.</span></span><br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <span data-ttu-id="01960-128"><dt>**\_НОКБУПДАТЕ SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-128"><dt>**SCF\_NOKBUPDATE**</dt></span></span> </dl>                | <span data-ttu-id="01960-129">**RichEdit 4,1:** Предотвращает переключение клавиатуры для соответствия шрифту.</span><span class="sxs-lookup"><span data-stu-id="01960-129">**RichEdit 4.1:** Prevents keyboard switching to match the font.</span></span> <span data-ttu-id="01960-130">Например, если установлен арабский шрифт, то обычно функция автоматической клавиатуры для языков с двунаправленным письмом изменяет клавиатуру на арабскую клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="01960-130">For example, if an Arabic font is set, normally the automatic keyboard feature for Bidi languages changes the keyboard to an Arabic keyboard.</span></span><br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="01960-131"><dt>**Выбор параметров SCF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-131"><dt>**SCF\_SELECTION**</dt></span></span> </dl>                   | <span data-ttu-id="01960-132">Применяет форматирование к текущему выделенному фрагменту.</span><span class="sxs-lookup"><span data-stu-id="01960-132">Applies the formatting to the current selection.</span></span> <span data-ttu-id="01960-133">Если выделение пусто, то к точке вставки применяется форматирование символов, а новый символьный формат действует только до тех пор, пока точка вставки не изменится.</span><span class="sxs-lookup"><span data-stu-id="01960-133">If the selection is empty, the character formatting is applied to the insertion point, and the new character format is in effect only until the insertion point changes.</span></span><br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <span data-ttu-id="01960-134"><dt>**SPF \_ сетдефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-134"><dt>**SPF\_SETDEFAULT**</dt></span></span> </dl>                | <span data-ttu-id="01960-135">Задает атрибуты форматирования абзаца по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="01960-135">Sets the default paragraph formatting attributes.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <span data-ttu-id="01960-136"><dt>**\_СМАРТФОНТ SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-136"><dt>**SCF\_SMARTFONT**</dt></span></span> </dl>                   | <span data-ttu-id="01960-137">Применить шрифт, только если он может работать со скриптом.</span><span class="sxs-lookup"><span data-stu-id="01960-137">Apply the font only if it can handle script.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <span data-ttu-id="01960-138"><dt>**\_УСЕУИРУЛЕС SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-138"><dt>**SCF\_USEUIRULES**</dt></span></span> </dl>                | <span data-ttu-id="01960-139">**RichEdit 4,1:** Используется с **\_ выбором SCF**.</span><span class="sxs-lookup"><span data-stu-id="01960-139">**RichEdit 4.1:** Used with **SCF\_SELECTION**.</span></span> <span data-ttu-id="01960-140">Указывает, что формат получен из панели инструментов или другого средства пользовательского интерфейса, поэтому правила форматирования пользовательского интерфейса следует использовать вместо форматирования литерала.</span><span class="sxs-lookup"><span data-stu-id="01960-140">Indicates that format came from a toolbar or other UI tool, so UI formatting rules should be used instead of literal formatting.</span></span><br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <span data-ttu-id="01960-141"><dt>**\_слово SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="01960-141"><dt>**SCF\_WORD**</dt></span></span> </dl>                                  | <span data-ttu-id="01960-142">Применение форматирования к выбранному слову или словам.</span><span class="sxs-lookup"><span data-stu-id="01960-142">Applies the formatting to the selected word or words.</span></span> <span data-ttu-id="01960-143">Если выделение пустое, но точка вставки находится внутри слова, форматирование применяется к слову.</span><span class="sxs-lookup"><span data-stu-id="01960-143">If the selection is empty but the insertion point is inside a word, the formatting is applied to the word.</span></span> <span data-ttu-id="01960-144">Значение **\_ слова SCF** должно использоваться в сочетании с значением выбора параметра **SCF \_** .</span><span class="sxs-lookup"><span data-stu-id="01960-144">The **SCF\_WORD** value must be used in conjunction with the **SCF\_SELECTION** value.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="01960-145">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01960-145">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01960-146">Указатель на структуру [**чарформат**](/windows/win32/api/richedit/ns-richedit-charformata) , определяющую используемое форматирование символов.</span><span class="sxs-lookup"><span data-stu-id="01960-146">Pointer to a [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure specifying the character formatting to use.</span></span> <span data-ttu-id="01960-147">Изменяются только атрибуты форматирования, заданные элементом **двмаск** .</span><span class="sxs-lookup"><span data-stu-id="01960-147">Only the formatting attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="01960-148">Microsoft Rich Edit 2,0 и более поздние версии: этот параметр может быть указателем на структуру [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , которая является расширением структуры [**чарформат**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="01960-148">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="01960-149">Перед отправкой сообщения **EM \_ сетчарформат** задайте для элемента **кбсизе** структуры значение `sizeof(CHARFORMAT)` или, чтобы `sizeof(CHARFORMAT2)` указать, какая версия структуры используется.</span><span class="sxs-lookup"><span data-stu-id="01960-149">Before sending the **EM\_SETCHARFORMAT** message, set the structure's **cbSize** member to `sizeof(CHARFORMAT)` or `sizeof(CHARFORMAT2)` indicate which version of the structure is being used.</span></span>

<span data-ttu-id="01960-150">Члены **сзфаценаме** и **бчарсет** могут быть перевышены, если они недопустимы для символов, например Arial для символов кандзи.</span><span class="sxs-lookup"><span data-stu-id="01960-150">The **szFaceName** and **bCharSet** members may be overruled when invalid for characters, for example: Arial on kanji characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01960-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01960-151">Return value</span></span>

<span data-ttu-id="01960-152">Если операция завершилась удачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="01960-152">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="01960-153">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="01960-153">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="01960-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01960-154">Remarks</span></span>

<span data-ttu-id="01960-155">Если это сообщение отправляется несколько раз с теми же параметрами, то его воздействие на текст переключается.</span><span class="sxs-lookup"><span data-stu-id="01960-155">If this message is sent more than once with the same parameters, the effect on the text is toggled.</span></span> <span data-ttu-id="01960-156">То есть Отправка сообщения после того, как выдает результат, отправляя сообщение дважды, отменяет результат и т. д.</span><span class="sxs-lookup"><span data-stu-id="01960-156">That is, sending the message once produces the effect, sending the message twice cancels the effect, and so forth.</span></span>

## <a name="requirements"></a><span data-ttu-id="01960-157">Требования</span><span class="sxs-lookup"><span data-stu-id="01960-157">Requirements</span></span>



| <span data-ttu-id="01960-158">Требование</span><span class="sxs-lookup"><span data-stu-id="01960-158">Requirement</span></span> | <span data-ttu-id="01960-159">Значение</span><span class="sxs-lookup"><span data-stu-id="01960-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01960-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01960-160">Minimum supported client</span></span><br/> | <span data-ttu-id="01960-161">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01960-161">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01960-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01960-162">Minimum supported server</span></span><br/> | <span data-ttu-id="01960-163">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01960-163">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01960-164">Header</span><span class="sxs-lookup"><span data-stu-id="01960-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="01960-165"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="01960-165"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01960-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01960-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="01960-167">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="01960-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="01960-168">**чарформат**</span><span class="sxs-lookup"><span data-stu-id="01960-168">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="01960-169">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="01960-169">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





