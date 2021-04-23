---
title: Сообщение EM_FINDWORDBREAK (RichEdit. h)
description: Поиск следующего разрыва слова до или после указанной позиции символа или получение сведений о символе в этой позиции.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- Элементы управления Windows для EM_FINDWORDBREAK сообщений
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491013"
---
# <a name="em_findwordbreak-message"></a><span data-ttu-id="f0083-104">\_Сообщение ФИНДВОРДБРЕАК EM</span><span class="sxs-lookup"><span data-stu-id="f0083-104">EM\_FINDWORDBREAK message</span></span>

<span data-ttu-id="f0083-105">Поиск следующего разрыва слова до или после указанной позиции символа или получение сведений о символе в этой позиции.</span><span class="sxs-lookup"><span data-stu-id="f0083-105">Finds the next word break before or after the specified character position or retrieves information about the character at that position.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0083-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0083-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0083-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0083-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0083-108">Указывает операцию поиска.</span><span class="sxs-lookup"><span data-stu-id="f0083-108">Specifies the find operation.</span></span> <span data-ttu-id="f0083-109">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="f0083-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f0083-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f0083-110">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="f0083-111">Значение</span><span class="sxs-lookup"><span data-stu-id="f0083-111">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <span data-ttu-id="f0083-112"><dt>**\_классификация WB**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-112"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>                | <span data-ttu-id="f0083-113">Возвращает класс символов и флаги разрыва слова для символа в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="f0083-113">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <span data-ttu-id="f0083-114"><dt>**WB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-114"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl>       | <span data-ttu-id="f0083-115">Возвращает **значение true** , если символ в указанной позиции является разделителем, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f0083-115">Returns **TRUE** if the character at the specified position is a delimiter, or **FALSE** otherwise.</span></span><br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <span data-ttu-id="f0083-116"><dt>**WB \_ слева**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-116"><dt>**WB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="f0083-117">Находит ближайший символ перед заданной позицией, которая начинает слово.</span><span class="sxs-lookup"><span data-stu-id="f0083-117">Finds the nearest character before the specified position that begins a word.</span></span><br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <span data-ttu-id="f0083-118"><dt>**WB \_ лефтбреак**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-118"><dt>**WB\_LEFTBREAK**</dt></span></span> </dl>             | <span data-ttu-id="f0083-119">Поиск следующего слова End перед указанной позицией.</span><span class="sxs-lookup"><span data-stu-id="f0083-119">Finds the next word end before the specified position.</span></span> <span data-ttu-id="f0083-120">Это значение совпадает с WB \_ превбреак.</span><span class="sxs-lookup"><span data-stu-id="f0083-120">This value is the same as WB\_PREVBREAK.</span></span><br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <span data-ttu-id="f0083-121"><dt>**WB \_ мовевордлефт**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-121"><dt>**WB\_MOVEWORDLEFT**</dt></span></span> </dl>    | <span data-ttu-id="f0083-122">Поиск следующего символа, который начинает слово перед указанной позицией.</span><span class="sxs-lookup"><span data-stu-id="f0083-122">Finds the next character that begins a word before the specified position.</span></span> <span data-ttu-id="f0083-123">Это значение используется при нажатии клавиш CTRL + стрелка влево.</span><span class="sxs-lookup"><span data-stu-id="f0083-123">This value is used during CTRL+LEFT ARROW key processing.</span></span> <span data-ttu-id="f0083-124">Это значение аналогично WB \_ мовевордпрев.</span><span class="sxs-lookup"><span data-stu-id="f0083-124">This value is the similar to WB\_MOVEWORDPREV.</span></span> <span data-ttu-id="f0083-125">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="f0083-125">See Remarks for more information.</span></span><br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <span data-ttu-id="f0083-126"><dt>**WB \_ мовевордригхт**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-126"><dt>**WB\_MOVEWORDRIGHT**</dt></span></span> </dl> | <span data-ttu-id="f0083-127">Поиск следующего символа, который начинается со слова после указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="f0083-127">Finds the next character that begins a word after the specified position.</span></span> <span data-ttu-id="f0083-128">Это значение используется во время обработки нажатия CTRL + Right Key.</span><span class="sxs-lookup"><span data-stu-id="f0083-128">This value is used during CTRL+right key processing.</span></span> <span data-ttu-id="f0083-129">Это значение похоже на WB \_ мовеворднекст.</span><span class="sxs-lookup"><span data-stu-id="f0083-129">This value is similar to WB\_MOVEWORDNEXT.</span></span> <span data-ttu-id="f0083-130">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="f0083-130">See Remarks for more information.</span></span><br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <span data-ttu-id="f0083-131"><dt>**WB \_ вправо**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-131"><dt>**WB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="f0083-132">Поиск следующего символа, который начинается со слова после указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="f0083-132">Finds the next character that begins a word after the specified position.</span></span><br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <span data-ttu-id="f0083-133"><dt>**WB \_ ригхтбреак**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-133"><dt>**WB\_RIGHTBREAK**</dt></span></span> </dl>          | <span data-ttu-id="f0083-134">Поиск следующего разделителя конца слова после указанной должности.</span><span class="sxs-lookup"><span data-stu-id="f0083-134">Finds the next end-of-word delimiter after the specified position.</span></span> <span data-ttu-id="f0083-135">Это значение совпадает с WB \_ некстбреак.</span><span class="sxs-lookup"><span data-stu-id="f0083-135">This value is the same as WB\_NEXTBREAK.</span></span><br/>                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="f0083-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0083-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0083-137">Начальная Отсчитываемая от нуля кодировка.</span><span class="sxs-lookup"><span data-stu-id="f0083-137">Zero-based character starting position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0083-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0083-138">Return value</span></span>

<span data-ttu-id="f0083-139">Сообщение возвращает значение, основанное на параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f0083-139">The message returns a value based on the *wParam* parameter.</span></span>



| <span data-ttu-id="f0083-140">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f0083-140">Return code</span></span>                                                                                    | <span data-ttu-id="f0083-141">Описание</span><span class="sxs-lookup"><span data-stu-id="f0083-141">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0083-142"><dt>**wParam**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-142"><dt>**wParam**</dt></span></span> </dl>          | <span data-ttu-id="f0083-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0083-143">Return Value</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="f0083-144"><dt>**\_классификация WB**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-144"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>    | <span data-ttu-id="f0083-145">Возвращает класс символов и флаги разрыва слова для символа в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="f0083-145">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                |
| <dl> <span data-ttu-id="f0083-146"><dt>**WB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-146"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl> | <span data-ttu-id="f0083-147">Возвращает **значение true** , если символ в указанной позиции является разделителем; в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f0083-147">Returns **TRUE** if the character at the specified position is a delimiter; otherwise it returns **FALSE**.</span></span><br/> |
| <dl> <span data-ttu-id="f0083-148"><dt>**Прочие**</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-148"><dt>**Others**</dt></span></span> </dl>          | <span data-ttu-id="f0083-149">Возвращает индекс символа для разрыва слова.</span><span class="sxs-lookup"><span data-stu-id="f0083-149">Returns the character index of the word break.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="f0083-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0083-150">Remarks</span></span>

<span data-ttu-id="f0083-151">Если параметр *wParam* имеет значение WB \_ Left и WB \_ right, то процедура разрыва слов позволяет найти разрывы слов только после разделителей.</span><span class="sxs-lookup"><span data-stu-id="f0083-151">If *wParam* is WB\_LEFT and WB\_RIGHT, the word-break procedure finds word breaks only after delimiters.</span></span> <span data-ttu-id="f0083-152">Это соответствует функциональным возможностям элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="f0083-152">This matches the functionality of an edit control.</span></span> <span data-ttu-id="f0083-153">Если параметр *wParam* имеет значение WB \_ мовевордлефт или WB \_ мовевордригхт, то процедура разбиения по словам также сравнивает классы символов и флаги разбиения по словам.</span><span class="sxs-lookup"><span data-stu-id="f0083-153">If *wParam* is WB\_MOVEWORDLEFT or WB\_MOVEWORDRIGHT, the word-break procedure also compares character classes and word-break flags.</span></span>

<span data-ttu-id="f0083-154">Сведения о классах символов и флагах разбиения по словам см. в разделе [разрывы слов и строк](using-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f0083-154">For information about character classes and word-break flags, see [Word and Line Breaks](using-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0083-155">Требования</span><span class="sxs-lookup"><span data-stu-id="f0083-155">Requirements</span></span>



| <span data-ttu-id="f0083-156">Требование</span><span class="sxs-lookup"><span data-stu-id="f0083-156">Requirement</span></span> | <span data-ttu-id="f0083-157">Значение</span><span class="sxs-lookup"><span data-stu-id="f0083-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0083-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0083-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f0083-159">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0083-159">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0083-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0083-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f0083-161">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0083-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0083-162">Header</span><span class="sxs-lookup"><span data-stu-id="f0083-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0083-163"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0083-163"><dt>Richedit.h</dt></span></span> </dl> |



 

 





