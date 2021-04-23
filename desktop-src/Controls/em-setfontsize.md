---
title: Сообщение EM_SETFONTSIZE (RichEdit. h)
description: Задает размер шрифта для выделенного текста в элементе управления Rich Edit.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- Элементы управления Windows для EM_SETFONTSIZE сообщений
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490722"
---
# <a name="em_setfontsize-message"></a><span data-ttu-id="81f5d-104">\_Сообщение СЕТФОНТСИЗЕ EM</span><span class="sxs-lookup"><span data-stu-id="81f5d-104">EM\_SETFONTSIZE message</span></span>

<span data-ttu-id="81f5d-105">Задает размер шрифта для выделенного текста в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="81f5d-105">Sets the font size for the selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="81f5d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81f5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81f5d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81f5d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81f5d-108">Изменить размер выделенного текста в пунктах.</span><span class="sxs-lookup"><span data-stu-id="81f5d-108">Change in point size of the selected text.</span></span> <span data-ttu-id="81f5d-109">Результат будет округлен в соответствии со значениями, приведенными в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="81f5d-109">The result will be rounded according to values shown in the following table.</span></span> <span data-ttu-id="81f5d-110">Этот параметр должен находиться в диапазоне от-1637 до 1638.</span><span class="sxs-lookup"><span data-stu-id="81f5d-110">This parameter should be in the range of -1637 to 1638.</span></span> <span data-ttu-id="81f5d-111">Итоговый размер шрифта будет в диапазоне от 1 до 1638.</span><span class="sxs-lookup"><span data-stu-id="81f5d-111">The resulting font size will be within the range of 1 to 1638.</span></span>

</dd> <dt>

<span data-ttu-id="81f5d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81f5d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81f5d-113">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="81f5d-113">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81f5d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81f5d-114">Return value</span></span>

<span data-ttu-id="81f5d-115">Если ошибка не возникла, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="81f5d-115">If no error occurred, the return value is **TRUE**.</span></span>

<span data-ttu-id="81f5d-116">Если произошла ошибка, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="81f5d-116">If an error occurred, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="81f5d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81f5d-117">Remarks</span></span>

<span data-ttu-id="81f5d-118">Размер шрифта можно легко получить, отправив сообщение [**EM \_ жетчарформат**](em-getcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="81f5d-118">You can easily get the font size by sending the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span>

<span data-ttu-id="81f5d-119">Расширенное редактирование сначала добавляет параметр *wParam* к текущему размеру шрифта, а затем использует полученный размер и следующую таблицу для определения значения округления.</span><span class="sxs-lookup"><span data-stu-id="81f5d-119">Rich Edit first adds *wParam* to the current font size and then uses the resulting size and the following table to determine the rounding value.</span></span>



| <span data-ttu-id="81f5d-120">Строки</span><span class="sxs-lookup"><span data-stu-id="81f5d-120">Band</span></span>    | <span data-ttu-id="81f5d-121">Значение округления</span><span class="sxs-lookup"><span data-stu-id="81f5d-121">Rounding value</span></span> |
|---------|----------------|
| <span data-ttu-id="81f5d-122"><= 12</span><span class="sxs-lookup"><span data-stu-id="81f5d-122"><=12</span></span> | <span data-ttu-id="81f5d-123">1</span><span class="sxs-lookup"><span data-stu-id="81f5d-123">1</span></span>              |
| <span data-ttu-id="81f5d-124">28</span><span class="sxs-lookup"><span data-stu-id="81f5d-124">28</span></span>      | <span data-ttu-id="81f5d-125">2</span><span class="sxs-lookup"><span data-stu-id="81f5d-125">2</span></span>              |
| <span data-ttu-id="81f5d-126">36</span><span class="sxs-lookup"><span data-stu-id="81f5d-126">36</span></span>      | <span data-ttu-id="81f5d-127">0</span><span class="sxs-lookup"><span data-stu-id="81f5d-127">0</span></span>              |
| <span data-ttu-id="81f5d-128">48</span><span class="sxs-lookup"><span data-stu-id="81f5d-128">48</span></span>      | <span data-ttu-id="81f5d-129">0</span><span class="sxs-lookup"><span data-stu-id="81f5d-129">0</span></span>              |
| <span data-ttu-id="81f5d-130">72</span><span class="sxs-lookup"><span data-stu-id="81f5d-130">72</span></span>      | <span data-ttu-id="81f5d-131">0</span><span class="sxs-lookup"><span data-stu-id="81f5d-131">0</span></span>              |
| <span data-ttu-id="81f5d-132">80</span><span class="sxs-lookup"><span data-stu-id="81f5d-132">80</span></span>      | <span data-ttu-id="81f5d-133">0</span><span class="sxs-lookup"><span data-stu-id="81f5d-133">0</span></span>              |
| <span data-ttu-id="81f5d-134">> 80</span><span class="sxs-lookup"><span data-stu-id="81f5d-134">> 80</span></span> | <span data-ttu-id="81f5d-135">10</span><span class="sxs-lookup"><span data-stu-id="81f5d-135">10</span></span>             |



 

<span data-ttu-id="81f5d-136">Если итоговый размер шрифта не делится равномерно на величину округления, то размер шрифта округляется до числа, равномерно кратного значению округления.</span><span class="sxs-lookup"><span data-stu-id="81f5d-136">If the resulting font size is not evenly divisible by the rounding value, the font size is then rounded to a number evenly divisible by the rounding value.</span></span> <span data-ttu-id="81f5d-137">Поэтому, если размер шрифта меньше или равен 12, значение округления будет равно 1.</span><span class="sxs-lookup"><span data-stu-id="81f5d-137">So if the font size is less than or equal to 12, the rounding value will be 1.</span></span> <span data-ttu-id="81f5d-138">Аналогично, если размер шрифта меньше или равен 28, то значение округления равно 2.</span><span class="sxs-lookup"><span data-stu-id="81f5d-138">Similarly, if the font size is less than or equal to 28, the rounding value is 2.</span></span> <span data-ttu-id="81f5d-139">Для значений, превышающих 28, размеры шрифтов округляются до следующей полосы.</span><span class="sxs-lookup"><span data-stu-id="81f5d-139">For values greater than 28, font sizes are rounded to the next band.</span></span> <span data-ttu-id="81f5d-140">Таким образом, размер шрифта переходит к 36, 48, 72, 80.</span><span class="sxs-lookup"><span data-stu-id="81f5d-140">So, the font size jumps to 36, 48, 72, 80.</span></span> <span data-ttu-id="81f5d-141">После 80 все округления выполняется с шагом в десять точек.</span><span class="sxs-lookup"><span data-stu-id="81f5d-141">After 80, all rounding is done in increments of ten points.</span></span>

<span data-ttu-id="81f5d-142">Размер шрифта округляется вверх или вниз в зависимости от знака параметра *wParam*.</span><span class="sxs-lookup"><span data-stu-id="81f5d-142">The font size is rounded up or down depending on the sign of *wParam*.</span></span> <span data-ttu-id="81f5d-143">Если параметр *wParam* имеет положительное значение, округление всегда вверх.</span><span class="sxs-lookup"><span data-stu-id="81f5d-143">If *wParam* is positive, the rounding is always up.</span></span> <span data-ttu-id="81f5d-144">В противном случае округление всегда не работает.</span><span class="sxs-lookup"><span data-stu-id="81f5d-144">Otherwise, rounding is always down.</span></span> <span data-ttu-id="81f5d-145">Таким образом, если текущий размер шрифта равен 10, а параметр *wParam* имеет значение 3, то итоговый размер шрифта будет равен 14 (10 + 3 = 13, что не делится на 2, поэтому размер округляется до 14).</span><span class="sxs-lookup"><span data-stu-id="81f5d-145">So, if the current font size is 10 and *wParam* is 3, the resulting font size would be 14 (10 + 3 = 13, which is not divisible by 2, so the size rounds up to 14).</span></span> <span data-ttu-id="81f5d-146">И наоборот, если текущий размер шрифта равен 14, а параметр *wParam* имеет значение-3, то итоговый размер шрифта будет равен 10 (14-3 = 11, который не делится на 2, поэтому размер округляется до 10).</span><span class="sxs-lookup"><span data-stu-id="81f5d-146">Conversely, if the current font size is 14 and *wParam* is -3, the resulting font size would be 10 (14 - 3 = 11, which is not divisible by 2, so the size rounds down to 10).</span></span>

<span data-ttu-id="81f5d-147">Изменение применяется к каждой части выделения.</span><span class="sxs-lookup"><span data-stu-id="81f5d-147">The change is applied to each part of the selection.</span></span> <span data-ttu-id="81f5d-148">Таким образом, если часть текста имеет значение 10 пт и некоторые до пунктов, после вызова с параметром *wParam* , равным 1, размеры шрифта становятся 11pt и 22pt соответственно.</span><span class="sxs-lookup"><span data-stu-id="81f5d-148">So, if some of the text is 10pt and some 20pt, after a call with *wParam* set to 1, the font sizes become 11pt and 22pt, respectively.</span></span>

<span data-ttu-id="81f5d-149">Дополнительные примеры приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="81f5d-149">Additional examples are shown in the following table.</span></span>



| <span data-ttu-id="81f5d-150">Исходный размер шрифта</span><span class="sxs-lookup"><span data-stu-id="81f5d-150">Original font size</span></span> | <span data-ttu-id="81f5d-151">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81f5d-151">*wParam*</span></span> | <span data-ttu-id="81f5d-152">Итоговый размер шрифта</span><span class="sxs-lookup"><span data-stu-id="81f5d-152">Resulting font size</span></span> |
|--------------------|----------|---------------------|
| <span data-ttu-id="81f5d-153">7</span><span class="sxs-lookup"><span data-stu-id="81f5d-153">7</span></span>                  | <span data-ttu-id="81f5d-154">1</span><span class="sxs-lookup"><span data-stu-id="81f5d-154">1</span></span>        | <span data-ttu-id="81f5d-155">8</span><span class="sxs-lookup"><span data-stu-id="81f5d-155">8</span></span>                   |
| <span data-ttu-id="81f5d-156">7</span><span class="sxs-lookup"><span data-stu-id="81f5d-156">7</span></span>                  | <span data-ttu-id="81f5d-157">3</span><span class="sxs-lookup"><span data-stu-id="81f5d-157">3</span></span>        | <span data-ttu-id="81f5d-158">10</span><span class="sxs-lookup"><span data-stu-id="81f5d-158">10</span></span>                  |
| <span data-ttu-id="81f5d-159">10</span><span class="sxs-lookup"><span data-stu-id="81f5d-159">10</span></span>                 | <span data-ttu-id="81f5d-160">3</span><span class="sxs-lookup"><span data-stu-id="81f5d-160">3</span></span>        | <span data-ttu-id="81f5d-161">14</span><span class="sxs-lookup"><span data-stu-id="81f5d-161">14</span></span>                  |
| <span data-ttu-id="81f5d-162">14</span><span class="sxs-lookup"><span data-stu-id="81f5d-162">14</span></span>                 | <span data-ttu-id="81f5d-163">–3</span><span class="sxs-lookup"><span data-stu-id="81f5d-163">-3</span></span>       | <span data-ttu-id="81f5d-164">10</span><span class="sxs-lookup"><span data-stu-id="81f5d-164">10</span></span>                  |
| <span data-ttu-id="81f5d-165">28</span><span class="sxs-lookup"><span data-stu-id="81f5d-165">28</span></span>                 | <span data-ttu-id="81f5d-166">1</span><span class="sxs-lookup"><span data-stu-id="81f5d-166">1</span></span>        | <span data-ttu-id="81f5d-167">36</span><span class="sxs-lookup"><span data-stu-id="81f5d-167">36</span></span>                  |
| <span data-ttu-id="81f5d-168">28</span><span class="sxs-lookup"><span data-stu-id="81f5d-168">28</span></span>                 | <span data-ttu-id="81f5d-169">3</span><span class="sxs-lookup"><span data-stu-id="81f5d-169">3</span></span>        | <span data-ttu-id="81f5d-170">36</span><span class="sxs-lookup"><span data-stu-id="81f5d-170">36</span></span>                  |
| <span data-ttu-id="81f5d-171">80</span><span class="sxs-lookup"><span data-stu-id="81f5d-171">80</span></span>                 | <span data-ttu-id="81f5d-172">1</span><span class="sxs-lookup"><span data-stu-id="81f5d-172">1</span></span>        | <span data-ttu-id="81f5d-173">90</span><span class="sxs-lookup"><span data-stu-id="81f5d-173">90</span></span>                  |
| <span data-ttu-id="81f5d-174">80</span><span class="sxs-lookup"><span data-stu-id="81f5d-174">80</span></span>                 | <span data-ttu-id="81f5d-175">-1</span><span class="sxs-lookup"><span data-stu-id="81f5d-175">-1</span></span>       | <span data-ttu-id="81f5d-176">72</span><span class="sxs-lookup"><span data-stu-id="81f5d-176">72</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="81f5d-177">Требования</span><span class="sxs-lookup"><span data-stu-id="81f5d-177">Requirements</span></span>



| <span data-ttu-id="81f5d-178">Требование</span><span class="sxs-lookup"><span data-stu-id="81f5d-178">Requirement</span></span> | <span data-ttu-id="81f5d-179">Значение</span><span class="sxs-lookup"><span data-stu-id="81f5d-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81f5d-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81f5d-180">Minimum supported client</span></span><br/> | <span data-ttu-id="81f5d-181">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81f5d-181">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81f5d-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81f5d-182">Minimum supported server</span></span><br/> | <span data-ttu-id="81f5d-183">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81f5d-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81f5d-184">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="81f5d-184">Redistributable</span></span><br/>          | <span data-ttu-id="81f5d-185">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="81f5d-185">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="81f5d-186">Header</span><span class="sxs-lookup"><span data-stu-id="81f5d-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="81f5d-187"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="81f5d-187"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81f5d-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81f5d-188">See also</span></span>

<dl> <dt>

<span data-ttu-id="81f5d-189">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="81f5d-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81f5d-190">**EM \_ жетчарформат**</span><span class="sxs-lookup"><span data-stu-id="81f5d-190">**EM\_GETCHARFORMAT**</span></span>](em-getcharformat.md)
</dt> <dt>

[<span data-ttu-id="81f5d-191">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="81f5d-191">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

<span data-ttu-id="81f5d-192">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="81f5d-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="81f5d-193">Общие сведения об элементах управления "поле ввода"</span><span class="sxs-lookup"><span data-stu-id="81f5d-193">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





