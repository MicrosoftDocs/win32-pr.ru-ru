---
title: Сообщение EM_GETIMEPROPERTY (RichEdit. h)
description: Извлекает свойство и возможности редактора метода ввода (IME), связанного с текущим языковым стандартом ввода.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- Элементы управления Windows для EM_GETIMEPROPERTY сообщений
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136862"
---
# <a name="em_getimeproperty-message"></a><span data-ttu-id="c2d4f-104">\_Сообщение ЖЕТИМЕПРОПЕРТИ EM</span><span class="sxs-lookup"><span data-stu-id="c2d4f-104">EM\_GETIMEPROPERTY message</span></span>

<span data-ttu-id="c2d4f-105">Извлекает свойство и возможности редактора метода ввода (IME), связанного с текущим языковым стандартом ввода.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-105">Retrieves the property and capabilities of the Input Method Editor (IME) associated with the current input locale.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2d4f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2d4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2d4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2d4f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2d4f-108">Указывает тип извлекаемых сведений о свойствах.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-108">Specifies the type of property information to retrieve.</span></span> <span data-ttu-id="c2d4f-109">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c2d4f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c2d4f-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="c2d4f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c2d4f-111">Meaning</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <span data-ttu-id="c2d4f-112"><dt>**ИГП, \_ свойство**</dt></span><span class="sxs-lookup"><span data-stu-id="c2d4f-112"><dt>**IGP\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="c2d4f-113">Сведения о свойстве.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-113">Property information.</span></span><br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <span data-ttu-id="c2d4f-114"><dt>**\_Преобразование ИГП**</dt></span><span class="sxs-lookup"><span data-stu-id="c2d4f-114"><dt>**IGP\_CONVERSION**</dt></span></span> </dl>          | <span data-ttu-id="c2d4f-115">Возможности преобразования.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-115">Conversion capabilities.</span></span> <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <span data-ttu-id="c2d4f-116"><dt>**ИГП \_ предложение**</dt></span><span class="sxs-lookup"><span data-stu-id="c2d4f-116"><dt>**IGP\_SENTENCE**</dt></span></span> </dl>                | <span data-ttu-id="c2d4f-117">Возможности режима предложений.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-117">Sentence mode capabilities.</span></span> <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <span data-ttu-id="c2d4f-118"><dt>**\_Пользовательский интерфейс ИГП**</dt></span><span class="sxs-lookup"><span data-stu-id="c2d4f-118"><dt>**IGP\_UI**</dt></span></span> </dl>                                  | <span data-ttu-id="c2d4f-119">Возможности пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-119">User interface capabilities.</span></span> <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <span data-ttu-id="c2d4f-120"><dt>**ИГП \_ сеткомпстр**</dt></span><span class="sxs-lookup"><span data-stu-id="c2d4f-120"><dt>**IGP\_SETCOMPSTR**</dt></span></span> </dl>          | <span data-ttu-id="c2d4f-121">Возможности строк композиции.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-121">Composition string capabilities.</span></span> <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <span data-ttu-id="c2d4f-122"><dt>**ИГП \_ SELECT**</dt></span><span class="sxs-lookup"><span data-stu-id="c2d4f-122"><dt>**IGP\_SELECT**</dt></span></span> </dl>                      | <span data-ttu-id="c2d4f-123">Возможности наследования выбора.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-123">Selection inheritance capabilities.</span></span> <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <span data-ttu-id="c2d4f-124"><dt>**ИГП \_ жетимеверсион**</dt></span><span class="sxs-lookup"><span data-stu-id="c2d4f-124"><dt>**IGP\_GETIMEVERSION**</dt></span></span> </dl> | <span data-ttu-id="c2d4f-125">Возвращает номер версии системы, для которой был создан указанный редактор IME.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-125">Retrieves the system version number for which the specified IME was created.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="c2d4f-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2d4f-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2d4f-127">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-127">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2d4f-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2d4f-128">Return value</span></span>

<span data-ttu-id="c2d4f-129">Возвращает значение свойства или возможности в зависимости от значения параметра *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c2d4f-129">Returns the property or capability value, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="c2d4f-130">Дополнительные сведения см. в разделе «Примечания».</span><span class="sxs-lookup"><span data-stu-id="c2d4f-130">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2d4f-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2d4f-131">Remarks</span></span>

<span data-ttu-id="c2d4f-132">Если свойство *wParam* имеет значение ИГП \_ , оно возвращает одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-132">If *wParam* is IGP\_PROPERTY, it returns one or more of the following values.</span></span>



| <span data-ttu-id="c2d4f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="c2d4f-133">Requirement</span></span> | <span data-ttu-id="c2d4f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="c2d4f-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d4f-135">\_prop в редакторе IME \_ на \_ курсоре</span><span class="sxs-lookup"><span data-stu-id="c2d4f-135">IME\_PROP\_AT\_CARET</span></span>                | <span data-ttu-id="c2d4f-136">Если задано, окно преобразования находится в позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-136">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="c2d4f-137">Если флажок снят, окно находится ближе к позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-137">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="c2d4f-138">\_ \_ Специальный \_ Пользовательский интерфейс редактора IME</span><span class="sxs-lookup"><span data-stu-id="c2d4f-138">IME\_PROP\_SPECIAL\_UI</span></span>              | <span data-ttu-id="c2d4f-139">Если задано, IME имеет нестандартный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-139">If set, IME has a nonstandard user interface.</span></span> <span data-ttu-id="c2d4f-140">Приложение не должно рисоваться в окне IME.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-140">The application should not draw in the IME window.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="c2d4f-141">Кандлист свойства IME, \_ \_ \_ начиная \_ с \_ 1</span><span class="sxs-lookup"><span data-stu-id="c2d4f-141">IME\_PROP\_CANDLIST\_START\_FROM\_1</span></span> | <span data-ttu-id="c2d4f-142">Если задано значение, строки в списке кандидатов нумеруются, начиная с 1.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-142">If set, strings in the candidate list are numbered starting at 1.</span></span> <span data-ttu-id="c2d4f-143">Если флажок снят, строки начинаются с нуля.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-143">If clear, strings start at zero.</span></span>                                                                                                                                                                |
| <span data-ttu-id="c2d4f-144">редактор IME, \_ \_ кодировка Юникод</span><span class="sxs-lookup"><span data-stu-id="c2d4f-144">IME\_PROP\_UNICODE</span></span>                  | <span data-ttu-id="c2d4f-145">Если этот параметр задан, редактор IME просматривается как Уникодеиме.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-145">If set, the IME is viewed as a UnicodeIME.</span></span> <span data-ttu-id="c2d4f-146">Система и редактор IME будут взаимодействовать через интерфейс Уникодеиме.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-146">The system and the IME will communicate through the UnicodeIME interface.</span></span> <span data-ttu-id="c2d4f-147">Если флажок снят, IME будет использовать интерфейс ANSI для взаимодействия с системой.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-147">If clear, IME will use the ANSI interface to communicate with the system.</span></span>                                                                    |
| <span data-ttu-id="c2d4f-148">не \_ \_ выбрано Автозаполнение IME \_ \_</span><span class="sxs-lookup"><span data-stu-id="c2d4f-148">IME\_PROP\_COMPLETE\_ON\_UNSELECT</span></span>   | <span data-ttu-id="c2d4f-149">Если задано, окно преобразования находится в позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-149">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="c2d4f-150">Если флажок снят, окно находится ближе к позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-150">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="c2d4f-151">режим IME " \_ \_ принять \_ широкий \_ ключ"</span><span class="sxs-lookup"><span data-stu-id="c2d4f-151">IME\_PROP\_ACCEPT\_WIDE\_VKEY</span></span>       | <span data-ttu-id="c2d4f-152">Если этот параметр задан, редактор IME обрабатывает вставленный символ Юникода, который поступил из функции [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) с помощью \_ пакета VK.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-152">If set, the IME processes the injected Unicode that came from the [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) function by using VK\_PACKET.</span></span> <span data-ttu-id="c2d4f-153">Если это не так, редактор IME может не обработать введенный символ Юникода, а вставленный в него символ Unicode может быть отправлен непосредственно приложению.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-153">If clear, the IME might not process the injected Unicode, and the injected Unicode might be sent to the application directly.</span></span> |



 

<span data-ttu-id="c2d4f-154">Если параметр *wParam* имеет значение ИГП \_ UI, он возвращает одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-154">If *wParam* is IGP\_UI, it returns one or more of the following values.</span></span>



| <span data-ttu-id="c2d4f-155">Требование</span><span class="sxs-lookup"><span data-stu-id="c2d4f-155">Requirement</span></span> | <span data-ttu-id="c2d4f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="c2d4f-156">Value</span></span> |
|-----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d4f-157">Ограничение пользовательского интерфейса \_ \_ 2700</span><span class="sxs-lookup"><span data-stu-id="c2d4f-157">UI\_CAP\_2700</span></span>   | <span data-ttu-id="c2d4f-158">Поддерживает значения режима escape-последовательности 0 или 2700.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-158">Supports text escapement values of 0 or 2700.</span></span> <span data-ttu-id="c2d4f-159">Дополнительные сведения см. в разделе **лфескапемент**.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-159">For more information, see **lfEscapement**.</span></span>             |
| <span data-ttu-id="c2d4f-160">\_ROT90 Cap пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="c2d4f-160">UI\_CAP\_ROT90</span></span>  | <span data-ttu-id="c2d4f-161">Поддерживает значения 0, 900, 1800 и 2700 для текста.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-161">Supports text escapement values of 0, 900, 1800, or 2700.</span></span> <span data-ttu-id="c2d4f-162">Дополнительные сведения см. в разделе **лфескапемент**.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-162">For more information, see **lfEscapement**.</span></span> |
| <span data-ttu-id="c2d4f-163">\_ротани Cap пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="c2d4f-163">UI\_CAP\_ROTANY</span></span> | <span data-ttu-id="c2d4f-164">Поддерживает любое значение escape-последовательности текста.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-164">Supports any text escapement value.</span></span> <span data-ttu-id="c2d4f-165">Дополнительные сведения см. в разделе **лфескапемент**.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-165">For more information, see **lfEscapement**.</span></span>                       |



 

<span data-ttu-id="c2d4f-166">Если параметр *wParam* имеет значение ИГП \_ сеткомпстр, он возвращает одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-166">If *wParam* is IGP\_SETCOMPSTR, it returns one or more of the following values.</span></span>



| <span data-ttu-id="c2d4f-167">Требование</span><span class="sxs-lookup"><span data-stu-id="c2d4f-167">Requirement</span></span> | <span data-ttu-id="c2d4f-168">Значение</span><span class="sxs-lookup"><span data-stu-id="c2d4f-168">Value</span></span> |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d4f-169">\_КОМПСТР SCS Cap \_</span><span class="sxs-lookup"><span data-stu-id="c2d4f-169">SCS\_CAP\_COMPSTR</span></span>            | <span data-ttu-id="c2d4f-170">Может создать строку композиции, вызвав функцию [**иммсеткомпоситионстринг**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) с параметром SCS \_ сетстр.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-170">Can create the composition string by calling the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with the SCS\_SETSTR value.</span></span>                                                      |
| <span data-ttu-id="c2d4f-171">\_МАКЕРЕАД SCS Cap \_</span><span class="sxs-lookup"><span data-stu-id="c2d4f-171">SCS\_CAP\_MAKEREAD</span></span>           | <span data-ttu-id="c2d4f-172">Может создать строку чтения из соответствующей строки композиции при использовании функции [**иммсеткомпоситионстринг**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) с SCS \_ сетстр и без установки *лпреад*.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-172">Can create the reading string from corresponding composition string when using the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with SCS\_SETSTR and without setting *lpRead*.</span></span> |
| <span data-ttu-id="c2d4f-173">\_СЕТРЕКОНВЕРТСТРИНГ SCS Cap \_</span><span class="sxs-lookup"><span data-stu-id="c2d4f-173">SCS\_CAP\_SETRECONVERTSTRING</span></span> | <span data-ttu-id="c2d4f-174">Этот редактор IME может поддерживать повторное преобразование.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-174">This IME can support reconversion.</span></span> <span data-ttu-id="c2d4f-175">Используйте [**иммсеткомпоситионстринг**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) для повторного преобразования.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-175">Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) to do the reconversion.</span></span>                                                                             |



 

<span data-ttu-id="c2d4f-176">Если параметр *wParam* имеет значение ИГП \_ SELECT, то он возвращает одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-176">If *wParam* is IGP\_SELECT, it returns one or more of the following values.</span></span>



| <span data-ttu-id="c2d4f-177">Требование</span><span class="sxs-lookup"><span data-stu-id="c2d4f-177">Requirement</span></span> | <span data-ttu-id="c2d4f-178">Значение</span><span class="sxs-lookup"><span data-stu-id="c2d4f-178">Value</span></span> |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="c2d4f-179">Выбор \_ ограничения \_ конвмоде</span><span class="sxs-lookup"><span data-stu-id="c2d4f-179">SELECT\_CAP\_CONVMODE</span></span> | <span data-ttu-id="c2d4f-180">Наследует режим преобразования, если выбран новый редактор IME.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-180">Inherits conversion mode when a new IME is selected.</span></span> |
| <span data-ttu-id="c2d4f-181">Выбор \_ \_ предложения крепления</span><span class="sxs-lookup"><span data-stu-id="c2d4f-181">SELECT\_CAP\_SENTENCE</span></span> | <span data-ttu-id="c2d4f-182">Наследует режим предложения при выборе нового редактора IME.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-182">Inherits sentence mode when a new IME is selected.</span></span>   |



 

<span data-ttu-id="c2d4f-183">Если параметр *wParam* имеет значение ИГП \_ жетимеверсион, он возвращает одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-183">If *wParam* is IGP\_GETIMEVERSION, it returns one or more of the following values.</span></span>



| <span data-ttu-id="c2d4f-184">Требование</span><span class="sxs-lookup"><span data-stu-id="c2d4f-184">Requirement</span></span> | <span data-ttu-id="c2d4f-185">Значение</span><span class="sxs-lookup"><span data-stu-id="c2d4f-185">Value</span></span> |
|--------------|---------------------------------------------|
| <span data-ttu-id="c2d4f-186">Непостоянное \_ 0310</span><span class="sxs-lookup"><span data-stu-id="c2d4f-186">IMEVER\_0310</span></span> | <span data-ttu-id="c2d4f-187">Редактор IME был создан для Windows 3,1.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-187">The IME was created for Windows 3.1.</span></span>        |
| <span data-ttu-id="c2d4f-188">Непостоянное \_ 0400</span><span class="sxs-lookup"><span data-stu-id="c2d4f-188">IMEVER\_0400</span></span> | <span data-ttu-id="c2d4f-189">Редактор IME был создан для Windows 95 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c2d4f-189">The IME was created for Windows 95 or later</span></span> |



 

<span data-ttu-id="c2d4f-190">Это сообщение похоже на [**иммжетпроперти**](/windows/desktop/api/imm/nf-imm-immgetproperty), за исключением того, что он использует текущий языковой стандарт ввода.</span><span class="sxs-lookup"><span data-stu-id="c2d4f-190">This message is similar to [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), except that it uses the current input locale.</span></span> <span data-ttu-id="c2d4f-191">Перед вызовом этой функции приложение должно вызвать [**EM \_ исиме**](em-isime.md) .</span><span class="sxs-lookup"><span data-stu-id="c2d4f-191">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2d4f-192">Требования</span><span class="sxs-lookup"><span data-stu-id="c2d4f-192">Requirements</span></span>



| <span data-ttu-id="c2d4f-193">Требование</span><span class="sxs-lookup"><span data-stu-id="c2d4f-193">Requirement</span></span> | <span data-ttu-id="c2d4f-194">Значение</span><span class="sxs-lookup"><span data-stu-id="c2d4f-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d4f-195">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2d4f-195">Minimum supported client</span></span><br/> | <span data-ttu-id="c2d4f-196">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2d4f-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2d4f-197">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2d4f-197">Minimum supported server</span></span><br/> | <span data-ttu-id="c2d4f-198">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2d4f-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2d4f-199">Header</span><span class="sxs-lookup"><span data-stu-id="c2d4f-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2d4f-200"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2d4f-200"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2d4f-201">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2d4f-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2d4f-202">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-202">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c2d4f-203">**EM \_ исиме**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-203">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

<span data-ttu-id="c2d4f-204">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-204">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c2d4f-205">**иммжетпроперти**</span><span class="sxs-lookup"><span data-stu-id="c2d4f-205">**ImmGetProperty**</span></span>](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

