---
title: Флаги для режима преобразования (Ктффунк. h)
description: Следующие флаги используются в качестве значения \_ инпутмоде преобразования секций \_ GUID \_ \_ . Это эквивалентно \_ значениям IME кмоде для IMM32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Флаги для платформы текстовых служб в режиме преобразования
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136194"
---
# <a name="flags-for-conversion-mode"></a><span data-ttu-id="61207-105">Флаги для режима преобразования</span><span class="sxs-lookup"><span data-stu-id="61207-105">Flags for Conversion Mode</span></span>

<span data-ttu-id="61207-106">Следующие флаги используются в качестве значения [ \_ \_ \_ Инпутмоде \_ преобразования секций GUID](predefined-compartments.md).</span><span class="sxs-lookup"><span data-stu-id="61207-106">The following flags are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_CONVERSION](predefined-compartments.md).</span></span> <span data-ttu-id="61207-107">Это эквивалентно значениям [IME \_ КМОДЕ](../intl/ime-conversion-mode-values.md) для IMM32.</span><span class="sxs-lookup"><span data-stu-id="61207-107">This is equivalent with [IME\_CMODE](../intl/ime-conversion-mode-values.md) values for IMM32.</span></span>



| <span data-ttu-id="61207-108">Флаг</span><span class="sxs-lookup"><span data-stu-id="61207-108">Flag</span></span>                             | <span data-ttu-id="61207-109">Значение</span><span class="sxs-lookup"><span data-stu-id="61207-109">Value</span></span>  | <span data-ttu-id="61207-110">Описание</span><span class="sxs-lookup"><span data-stu-id="61207-110">Description</span></span>                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="61207-111">TF \_ конверсионмоде, \_ буквенно-цифровой</span><span class="sxs-lookup"><span data-stu-id="61207-111">TF\_CONVERSIONMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="61207-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="61207-112">0x0000</span></span> | <span data-ttu-id="61207-113">Значение 1, если БУКВЕНно-цифровой режим.</span><span class="sxs-lookup"><span data-stu-id="61207-113">Set to 1 if ALPHANUMERIC mode.</span></span>                                  |
| <span data-ttu-id="61207-114">TF \_ конверсионмоде \_ native</span><span class="sxs-lookup"><span data-stu-id="61207-114">TF\_CONVERSIONMODE\_NATIVE</span></span>       | <span data-ttu-id="61207-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="61207-115">0x0001</span></span> | <span data-ttu-id="61207-116">Задайте значение 1, если собственный режим —. 0, если БУКВЕНно-цифровой режим.</span><span class="sxs-lookup"><span data-stu-id="61207-116">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                |
| <span data-ttu-id="61207-117">TF \_ конверсионмоде \_ катакана</span><span class="sxs-lookup"><span data-stu-id="61207-117">TF\_CONVERSIONMODE\_KATAKANA</span></span>     | <span data-ttu-id="61207-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="61207-118">0x0002</span></span> | <span data-ttu-id="61207-119">Задайте значение 1 в режиме катакана. 0, если режим хирагана.</span><span class="sxs-lookup"><span data-stu-id="61207-119">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                  |
| <span data-ttu-id="61207-120">TF \_ конверсионмоде \_ фуллшапе</span><span class="sxs-lookup"><span data-stu-id="61207-120">TF\_CONVERSIONMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="61207-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="61207-121">0x0008</span></span> | <span data-ttu-id="61207-122">Задайте значение 1, если режим полной формы; 0, если режим половинной фигуры.</span><span class="sxs-lookup"><span data-stu-id="61207-122">Set to 1 if full shape mode; 0 if half shape mode.</span></span>              |
| <span data-ttu-id="61207-123">TF \_ конверсионмоде \_ Roman</span><span class="sxs-lookup"><span data-stu-id="61207-123">TF\_CONVERSIONMODE\_ROMAN</span></span>        | <span data-ttu-id="61207-124">0x0010</span><span class="sxs-lookup"><span data-stu-id="61207-124">0x0010</span></span> | <span data-ttu-id="61207-125">Задайте значение 1, чтобы предотвратить обработку преобразований IME. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="61207-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="61207-126">TF \_ конверсионмоде \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="61207-126">TF\_CONVERSIONMODE\_CHARCODE</span></span>     | <span data-ttu-id="61207-127">0x0020</span><span class="sxs-lookup"><span data-stu-id="61207-127">0x0020</span></span> | <span data-ttu-id="61207-128">Значение 1, если режим ввода кода символа; 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="61207-128">Set to 1 if character code input mode; 0 if not.</span></span>                |
| <span data-ttu-id="61207-129">TF \_ конверсионмоде \_ софткэйбоард</span><span class="sxs-lookup"><span data-stu-id="61207-129">TF\_CONVERSIONMODE\_SOFTKEYBOARD</span></span> | <span data-ttu-id="61207-130">0x0080</span><span class="sxs-lookup"><span data-stu-id="61207-130">0x0080</span></span> | <span data-ttu-id="61207-131">Задайте значение 1 в режиме экранной клавиатуры. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="61207-131">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                       |
| <span data-ttu-id="61207-132">TF \_ конверсионмоде, \_ Преобразование</span><span class="sxs-lookup"><span data-stu-id="61207-132">TF\_CONVERSIONMODE\_NOCONVERSION</span></span> | <span data-ttu-id="61207-133">0x0100</span><span class="sxs-lookup"><span data-stu-id="61207-133">0x0100</span></span> | <span data-ttu-id="61207-134">Задайте значение 1, чтобы предотвратить обработку преобразований IME. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="61207-134">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="61207-135">TF \_ конверсионмоде \_ symbol</span><span class="sxs-lookup"><span data-stu-id="61207-135">TF\_CONVERSIONMODE\_SYMBOL</span></span>       | <span data-ttu-id="61207-136">0x0400</span><span class="sxs-lookup"><span data-stu-id="61207-136">0x0400</span></span> | <span data-ttu-id="61207-137">В режиме преобразования символов задайте значение 1. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="61207-137">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                   |
| <span data-ttu-id="61207-138">TF \_ конверсионмоде \_ fixed</span><span class="sxs-lookup"><span data-stu-id="61207-138">TF\_CONVERSIONMODE\_FIXED</span></span>        | <span data-ttu-id="61207-139">0x0800</span><span class="sxs-lookup"><span data-stu-id="61207-139">0x0800</span></span> | <span data-ttu-id="61207-140">При фиксированном режиме преобразования задайте значение 1. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="61207-140">Set to 1 if fixed conversion mode; 0 if not.</span></span>                    |



 

<span data-ttu-id="61207-141">В качестве значения параметра [ \_ \_ \_ инпутмоде \_ Секции GUID](predefined-compartments.md)используются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="61207-141">The following values are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_SENTENCE](predefined-compartments.md).</span></span> <span data-ttu-id="61207-142">Это эквивалентно значениям [IME \_ СМОДЕ](../intl/ime-composition-string-values.md) для IMM32.</span><span class="sxs-lookup"><span data-stu-id="61207-142">This is equivalent with [IME\_SMODE](../intl/ime-composition-string-values.md) values for IMM32.</span></span>



| <span data-ttu-id="61207-143">Флаг</span><span class="sxs-lookup"><span data-stu-id="61207-143">Flag</span></span>                            | <span data-ttu-id="61207-144">Значение</span><span class="sxs-lookup"><span data-stu-id="61207-144">Value</span></span>  | <span data-ttu-id="61207-145">Описание</span><span class="sxs-lookup"><span data-stu-id="61207-145">Description</span></span>                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| <span data-ttu-id="61207-146">TF \_ сентенцемоде \_ None</span><span class="sxs-lookup"><span data-stu-id="61207-146">TF\_SENTENCEMODE\_NONE</span></span>          | <span data-ttu-id="61207-147">0x0000</span><span class="sxs-lookup"><span data-stu-id="61207-147">0x0000</span></span> | <span data-ttu-id="61207-148">Нет сведений о предложении.</span><span class="sxs-lookup"><span data-stu-id="61207-148">No information for sentence.</span></span>                                               |
| <span data-ttu-id="61207-149">TF \_ сентенцемоде \_ плауралклаусе</span><span class="sxs-lookup"><span data-stu-id="61207-149">TF\_SENTENCEMODE\_PLAURALCLAUSE</span></span> | <span data-ttu-id="61207-150">0x0001</span><span class="sxs-lookup"><span data-stu-id="61207-150">0x0001</span></span> | <span data-ttu-id="61207-151">Редактор IME использует сведения о предложении plural для выполнения обработки преобразования.</span><span class="sxs-lookup"><span data-stu-id="61207-151">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="61207-152">TF \_ сентенцемоде \_ синглеконверт</span><span class="sxs-lookup"><span data-stu-id="61207-152">TF\_SENTENCEMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="61207-153">0x0002</span><span class="sxs-lookup"><span data-stu-id="61207-153">0x0002</span></span> | <span data-ttu-id="61207-154">Редактор IME выполняет обработку преобразования в односимвольном режиме.</span><span class="sxs-lookup"><span data-stu-id="61207-154">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="61207-155">TF \_ сентенцемоде \_ Automatic</span><span class="sxs-lookup"><span data-stu-id="61207-155">TF\_SENTENCEMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="61207-156">0x0004</span><span class="sxs-lookup"><span data-stu-id="61207-156">0x0004</span></span> | <span data-ttu-id="61207-157">Редактор IME выполняет обработку преобразования в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="61207-157">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="61207-158">TF \_ сентенцемоде \_ фрасепредикт</span><span class="sxs-lookup"><span data-stu-id="61207-158">TF\_SENTENCEMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="61207-159">0x0008</span><span class="sxs-lookup"><span data-stu-id="61207-159">0x0008</span></span> | <span data-ttu-id="61207-160">Редактор IME использует сведения о фразах для прогнозирования следующего символа.</span><span class="sxs-lookup"><span data-stu-id="61207-160">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="61207-161">TF \_ сентенцемоде \_ CONVERSATION</span><span class="sxs-lookup"><span data-stu-id="61207-161">TF\_SENTENCEMODE\_CONVERSATION</span></span>  | <span data-ttu-id="61207-162">0x0010</span><span class="sxs-lookup"><span data-stu-id="61207-162">0x0010</span></span> | <span data-ttu-id="61207-163">Редактор IME использует режим диалога.</span><span class="sxs-lookup"><span data-stu-id="61207-163">The IME uses conversation mode.</span></span> <span data-ttu-id="61207-164">Это полезно для приложений разговора.</span><span class="sxs-lookup"><span data-stu-id="61207-164">This is useful for chat applications.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="61207-165">Требования</span><span class="sxs-lookup"><span data-stu-id="61207-165">Requirements</span></span>



| <span data-ttu-id="61207-166">Требование</span><span class="sxs-lookup"><span data-stu-id="61207-166">Requirement</span></span> | <span data-ttu-id="61207-167">Значение</span><span class="sxs-lookup"><span data-stu-id="61207-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61207-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61207-168">Minimum supported client</span></span><br/> | <span data-ttu-id="61207-169">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61207-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="61207-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61207-170">Minimum supported server</span></span><br/> | <span data-ttu-id="61207-171">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61207-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="61207-172">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="61207-172">Redistributable</span></span><br/>          | <span data-ttu-id="61207-173">TSF 1,0 — Windows NT 4.0, Windows 2000 Профессионаландвиндовс Мевиндовс 98</span><span class="sxs-lookup"><span data-stu-id="61207-173">TSF 1.0 onWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98</span></span><br/>   |
| <span data-ttu-id="61207-174">Header</span><span class="sxs-lookup"><span data-stu-id="61207-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="61207-175"><dt>Ктффунк. h</dt></span><span class="sxs-lookup"><span data-stu-id="61207-175"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="61207-176">IDL</span><span class="sxs-lookup"><span data-stu-id="61207-176">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61207-177"><dt>Ктффунк. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61207-177"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61207-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61207-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61207-179">Стандартные секции</span><span class="sxs-lookup"><span data-stu-id="61207-179">Predefined Compartments</span></span>](predefined-compartments.md)
</dt> </dl>

 

