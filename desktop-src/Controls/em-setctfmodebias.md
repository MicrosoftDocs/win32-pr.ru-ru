---
title: Сообщение EM_SETCTFMODEBIAS (RichEdit. h)
description: Задает смещение режима в режиме платформы текстовых служб (TSF) для элемента управления расширенного редактирования.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- Элементы управления Windows для EM_SETCTFMODEBIAS сообщений
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535060"
---
# <a name="em_setctfmodebias-message"></a><span data-ttu-id="b257c-104">\_Сообщение СЕТКТФМОДЕБИАС EM</span><span class="sxs-lookup"><span data-stu-id="b257c-104">EM\_SETCTFMODEBIAS message</span></span>

<span data-ttu-id="b257c-105">Задает смещение режима в режиме платформы текстовых служб (TSF) для элемента управления расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="b257c-105">Sets the Text Services Framework (TSF) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b257c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b257c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b257c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b257c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b257c-108">Значение смещения режима.</span><span class="sxs-lookup"><span data-stu-id="b257c-108">Mode bias value.</span></span> <span data-ttu-id="b257c-109">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b257c-109">This can be one of the following values.</span></span>



| <span data-ttu-id="b257c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b257c-110">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="b257c-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b257c-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <span data-ttu-id="b257c-112"><dt>**КТФМОДЕБИАС \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-112"><dt>**CTFMODEBIAS\_DEFAULT**</dt></span></span> </dl>                                           | <span data-ttu-id="b257c-113">Смещение в режиме отсутствует.</span><span class="sxs-lookup"><span data-stu-id="b257c-113">There is no mode bias.</span></span><br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <span data-ttu-id="b257c-114"><dt>**\_имя файла ктфмодебиас**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-114"><dt>**CTFMODEBIAS\_FILENAME**</dt></span></span> </dl>                                        | <span data-ttu-id="b257c-115">Значение смещения — имя файла.</span><span class="sxs-lookup"><span data-stu-id="b257c-115">The bias is to a filename.</span></span><br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <span data-ttu-id="b257c-116"><dt>**\_имя ктфмодебиас**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-116"><dt>**CTFMODEBIAS\_NAME**</dt></span></span> </dl>                                                    | <span data-ttu-id="b257c-117">Значение смещения — имя.</span><span class="sxs-lookup"><span data-stu-id="b257c-117">The bias is to a name.</span></span><br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <span data-ttu-id="b257c-118"><dt>**\_Чтение ктфмодебиас**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-118"><dt>**CTFMODEBIAS\_READING**</dt></span></span> </dl>                                           | <span data-ttu-id="b257c-119">Смещение предназначено для чтения.</span><span class="sxs-lookup"><span data-stu-id="b257c-119">The bias is to the reading.</span></span><br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <span data-ttu-id="b257c-120"><dt>**КТФМОДЕБИАС \_ DateTime**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-120"><dt>**CTFMODEBIAS\_DATETIME**</dt></span></span> </dl>                                        | <span data-ttu-id="b257c-121">Смещение — это дата или время.</span><span class="sxs-lookup"><span data-stu-id="b257c-121">The bias is to a date or time.</span></span><br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <span data-ttu-id="b257c-122"><dt>**КТФМОДЕБИАС \_ беседа**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-122"><dt>**CTFMODEBIAS\_CONVERSATION**</dt></span></span> </dl>                            | <span data-ttu-id="b257c-123">Смещение — это диалог.</span><span class="sxs-lookup"><span data-stu-id="b257c-123">The bias is to a conversation.</span></span><br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <span data-ttu-id="b257c-124"><dt>**КТФМОДЕБИАС \_ числовой**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-124"><dt>**CTFMODEBIAS\_NUMERIC**</dt></span></span> </dl>                                           | <span data-ttu-id="b257c-125">Смещение — это число.</span><span class="sxs-lookup"><span data-stu-id="b257c-125">The bias is to a number.</span></span><br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <span data-ttu-id="b257c-126"><dt>**КТФМОДЕБИАС \_ хирагана**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-126"><dt>**CTFMODEBIAS\_HIRAGANA**</dt></span></span> </dl>                                        | <span data-ttu-id="b257c-127">Смещение — строки хирагана.</span><span class="sxs-lookup"><span data-stu-id="b257c-127">The bias is to hiragana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <span data-ttu-id="b257c-128"><dt>**КТФМОДЕБИАС \_ катакана**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-128"><dt>**CTFMODEBIAS\_KATAKANA**</dt></span></span> </dl>                                        | <span data-ttu-id="b257c-129">Значение смещения — строки катакана.</span><span class="sxs-lookup"><span data-stu-id="b257c-129">The bias is to katakana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <span data-ttu-id="b257c-130"><dt>**\_ХАНГЫЛЬ ктфмодебиас**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-130"><dt>**CTFMODEBIAS\_HANGUL**</dt></span></span> </dl>                                              | <span data-ttu-id="b257c-131">Смещение — символы хангыль.</span><span class="sxs-lookup"><span data-stu-id="b257c-131">The bias is to Hangul characters.</span></span><br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <span data-ttu-id="b257c-132"><dt>**КТФМОДЕБИАС \_ халфвидскатакана**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-132"><dt>**CTFMODEBIAS\_HALFWIDTHKATAKANA**</dt></span></span> </dl>             | <span data-ttu-id="b257c-133">Смещение — строки катакана половинной ширины.</span><span class="sxs-lookup"><span data-stu-id="b257c-133">The bias is to half-width katakana strings.</span></span><br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <span data-ttu-id="b257c-134"><dt>**КТФМОДЕБИАС \_ фуллвидсалфанумерик**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-134"><dt>**CTFMODEBIAS\_FULLWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="b257c-135">Смещение — это алфавитно-цифровые символы в полной ширине.</span><span class="sxs-lookup"><span data-stu-id="b257c-135">The bias is to full-width alphanumeric characters.</span></span><br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <span data-ttu-id="b257c-136"><dt>**КТФМОДЕБИАС \_ халфвидсалфанумерик**</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-136"><dt>**CTFMODEBIAS\_HALFWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="b257c-137">Смещение — это алфавитно-цифровые символы половинной ширины.</span><span class="sxs-lookup"><span data-stu-id="b257c-137">The bias is to half-width alphanumeric characters.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b257c-138">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b257c-138">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b257c-139">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b257c-139">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b257c-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b257c-140">Return value</span></span>

<span data-ttu-id="b257c-141">В случае успеха возвращаемое значение является новым значением смещения режима TSF.</span><span class="sxs-lookup"><span data-stu-id="b257c-141">If successful, the return value is the new TSF mode bias value.</span></span> <span data-ttu-id="b257c-142">В случае неудачи возвращаемое значение является старым значением смещения режима TSF.</span><span class="sxs-lookup"><span data-stu-id="b257c-142">If unsuccessful, the return value is the old TSF mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b257c-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b257c-143">Remarks</span></span>

<span data-ttu-id="b257c-144">Если приложение Microsoft Rich Edit использует TSF, оно может выбрать смещение режима TSF.</span><span class="sxs-lookup"><span data-stu-id="b257c-144">When a Microsoft Rich Edit application uses TSF, it can select the TSF mode bias.</span></span> <span data-ttu-id="b257c-145">Это сообщение задает критерии, по которым в верхней части списка появляется альтернативный вариант выбора.</span><span class="sxs-lookup"><span data-stu-id="b257c-145">This message sets the criteria by which an alternative choice appears at the top of the list for selection.</span></span>

<span data-ttu-id="b257c-146">Чтобы установить сдвиг режима для редактора метода ввода (IME), используйте [**EM \_ сетимемодебиас**](em-setimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="b257c-146">To set the mode bias for the Input Method Editor (IME), use [**EM\_SETIMEMODEBIAS**](em-setimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b257c-147">Требования</span><span class="sxs-lookup"><span data-stu-id="b257c-147">Requirements</span></span>



| <span data-ttu-id="b257c-148">Требование</span><span class="sxs-lookup"><span data-stu-id="b257c-148">Requirement</span></span> | <span data-ttu-id="b257c-149">Значение</span><span class="sxs-lookup"><span data-stu-id="b257c-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b257c-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b257c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b257c-151">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="b257c-151">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b257c-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b257c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b257c-153">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b257c-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b257c-154">Header</span><span class="sxs-lookup"><span data-stu-id="b257c-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="b257c-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b257c-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b257c-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b257c-156">See also</span></span>

<dl> <dt>

<span data-ttu-id="b257c-157">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b257c-157">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b257c-158">**EM \_ жетктфмодебиас**</span><span class="sxs-lookup"><span data-stu-id="b257c-158">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="b257c-159">**EM \_ сетимемодебиас**</span><span class="sxs-lookup"><span data-stu-id="b257c-159">**EM\_SETIMEMODEBIAS**</span></span>](em-setimemodebias.md)
</dt> </dl>

 

 





