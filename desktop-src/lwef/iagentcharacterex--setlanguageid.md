---
title: Иажентчарактерекс Сетлангуажеид
description: Иажентчарактерекс Сетлангуажеид
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036e1d41878adaae878a5961b45d190971d790af
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119009"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="7b8de-103">Иажентчарактерекс:: Сетлангуажеид</span><span class="sxs-lookup"><span data-stu-id="7b8de-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="7b8de-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7b8de-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="7b8de-105">Задает идентификатор языка, заданный для символа.</span><span class="sxs-lookup"><span data-stu-id="7b8de-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="7b8de-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7b8de-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7b8de-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Надежно*</span><span class="sxs-lookup"><span data-stu-id="7b8de-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="7b8de-108">Параметр идентификатора языка для символа.</span><span class="sxs-lookup"><span data-stu-id="7b8de-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="7b8de-109">Длинное целое число, указывающее идентификатор языка для символа.</span><span class="sxs-lookup"><span data-stu-id="7b8de-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="7b8de-110">Идентификатор языка (LANGID) для символа — это 16-разрядное значение, определенное Windows, состоящее из основного идентификатора языка и дополнительного идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="7b8de-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="7b8de-111">Для указанных языков можно использовать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7b8de-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="7b8de-112">Дополнительные сведения см. в документации по пакету Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="7b8de-112">For more information, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="7b8de-113">Язык</span><span class="sxs-lookup"><span data-stu-id="7b8de-113">Language</span></span>              | <span data-ttu-id="7b8de-114">ID</span><span class="sxs-lookup"><span data-stu-id="7b8de-114">ID</span></span>     |  <span data-ttu-id="7b8de-115">Язык</span><span class="sxs-lookup"><span data-stu-id="7b8de-115">Language</span></span>             | <span data-ttu-id="7b8de-116">ID</span><span class="sxs-lookup"><span data-stu-id="7b8de-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="7b8de-117">Арабский (Саудовская Аравия)</span><span class="sxs-lookup"><span data-stu-id="7b8de-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="7b8de-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="7b8de-118">0x0401</span></span> | <span data-ttu-id="7b8de-119">Итальянский</span><span class="sxs-lookup"><span data-stu-id="7b8de-119">Italian</span></span>               | <span data-ttu-id="7b8de-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="7b8de-120">0x0410</span></span> |
| <span data-ttu-id="7b8de-121">Баскский</span><span class="sxs-lookup"><span data-stu-id="7b8de-121">Basque</span></span>                | <span data-ttu-id="7b8de-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="7b8de-122">0x042d</span></span> | <span data-ttu-id="7b8de-123">Японский</span><span class="sxs-lookup"><span data-stu-id="7b8de-123">Japanese</span></span>              | <span data-ttu-id="7b8de-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="7b8de-124">0x0411</span></span> |
| <span data-ttu-id="7b8de-125">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="7b8de-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="7b8de-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="7b8de-126">0x0804</span></span> | <span data-ttu-id="7b8de-127">Корейский</span><span class="sxs-lookup"><span data-stu-id="7b8de-127">Korean</span></span>                | <span data-ttu-id="7b8de-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="7b8de-128">0x0412</span></span> |
| <span data-ttu-id="7b8de-129">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="7b8de-129">Chinese (Traditional)</span></span> | <span data-ttu-id="7b8de-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="7b8de-130">0x0404</span></span> | <span data-ttu-id="7b8de-131">Норвежский</span><span class="sxs-lookup"><span data-stu-id="7b8de-131">Norwegian</span></span>             | <span data-ttu-id="7b8de-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="7b8de-132">0x0414</span></span> |
| <span data-ttu-id="7b8de-133">Хорватский</span><span class="sxs-lookup"><span data-stu-id="7b8de-133">Croatian</span></span>              | <span data-ttu-id="7b8de-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="7b8de-134">0x041A</span></span> | <span data-ttu-id="7b8de-135">Польский</span><span class="sxs-lookup"><span data-stu-id="7b8de-135">Polish</span></span>                | <span data-ttu-id="7b8de-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="7b8de-136">0x0415</span></span> |
| <span data-ttu-id="7b8de-137">Чешский</span><span class="sxs-lookup"><span data-stu-id="7b8de-137">Czech</span></span>                 | <span data-ttu-id="7b8de-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="7b8de-138">0x0405</span></span> | <span data-ttu-id="7b8de-139">Португальский (Португалия)</span><span class="sxs-lookup"><span data-stu-id="7b8de-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="7b8de-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="7b8de-140">0x0816</span></span> |
| <span data-ttu-id="7b8de-141">Датский</span><span class="sxs-lookup"><span data-stu-id="7b8de-141">Danish</span></span>                | <span data-ttu-id="7b8de-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="7b8de-142">0x0406</span></span> | <span data-ttu-id="7b8de-143">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="7b8de-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="7b8de-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="7b8de-144">0x0416</span></span> |
| <span data-ttu-id="7b8de-145">Голландский</span><span class="sxs-lookup"><span data-stu-id="7b8de-145">Dutch</span></span>                 | <span data-ttu-id="7b8de-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="7b8de-146">0x0413</span></span> | <span data-ttu-id="7b8de-147">Румынский</span><span class="sxs-lookup"><span data-stu-id="7b8de-147">Romanian</span></span>              | <span data-ttu-id="7b8de-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="7b8de-148">0x0418</span></span> |
| <span data-ttu-id="7b8de-149">Английский (Великобритания)</span><span class="sxs-lookup"><span data-stu-id="7b8de-149">English (British)</span></span>     | <span data-ttu-id="7b8de-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="7b8de-150">0x0809</span></span> | <span data-ttu-id="7b8de-151">Русский</span><span class="sxs-lookup"><span data-stu-id="7b8de-151">Russian</span></span>               | <span data-ttu-id="7b8de-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="7b8de-152">0x0419</span></span> |
| <span data-ttu-id="7b8de-153">Английский (США)</span><span class="sxs-lookup"><span data-stu-id="7b8de-153">English (US)</span></span>          | <span data-ttu-id="7b8de-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="7b8de-154">0x0409</span></span> | <span data-ttu-id="7b8de-155">Словацкий</span><span class="sxs-lookup"><span data-stu-id="7b8de-155">Slovakian</span></span>             | <span data-ttu-id="7b8de-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="7b8de-156">0x041B</span></span> |
| <span data-ttu-id="7b8de-157">Финский</span><span class="sxs-lookup"><span data-stu-id="7b8de-157">Finnish</span></span>               | <span data-ttu-id="7b8de-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="7b8de-158">0x040B</span></span> | <span data-ttu-id="7b8de-159">Словенский</span><span class="sxs-lookup"><span data-stu-id="7b8de-159">Slovenian</span></span>             | <span data-ttu-id="7b8de-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="7b8de-160">0x0424</span></span> |
| <span data-ttu-id="7b8de-161">Французский</span><span class="sxs-lookup"><span data-stu-id="7b8de-161">French</span></span>                | <span data-ttu-id="7b8de-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="7b8de-162">0x040C</span></span> | <span data-ttu-id="7b8de-163">Испанский</span><span class="sxs-lookup"><span data-stu-id="7b8de-163">Spanish</span></span>               | <span data-ttu-id="7b8de-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="7b8de-164">0x0C0A</span></span> |
| <span data-ttu-id="7b8de-165">Немецкий</span><span class="sxs-lookup"><span data-stu-id="7b8de-165">German</span></span>                | <span data-ttu-id="7b8de-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="7b8de-166">0x0407</span></span> | <span data-ttu-id="7b8de-167">Шведский</span><span class="sxs-lookup"><span data-stu-id="7b8de-167">Swedish</span></span>               | <span data-ttu-id="7b8de-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="7b8de-168">0x041D</span></span> |
| <span data-ttu-id="7b8de-169">Греческий</span><span class="sxs-lookup"><span data-stu-id="7b8de-169">Greek</span></span>                 | <span data-ttu-id="7b8de-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="7b8de-170">0x0408</span></span> | <span data-ttu-id="7b8de-171">Тайский</span><span class="sxs-lookup"><span data-stu-id="7b8de-171">Thai</span></span>                  | <span data-ttu-id="7b8de-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="7b8de-172">0x041E</span></span> |
| <span data-ttu-id="7b8de-173">Иврит</span><span class="sxs-lookup"><span data-stu-id="7b8de-173">Hebrew</span></span>                | <span data-ttu-id="7b8de-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="7b8de-174">0x040D</span></span> | <span data-ttu-id="7b8de-175">Турецкий</span><span class="sxs-lookup"><span data-stu-id="7b8de-175">Turkish</span></span>               | <span data-ttu-id="7b8de-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="7b8de-176">0x041F</span></span> |
| <span data-ttu-id="7b8de-177">Венгерский</span><span class="sxs-lookup"><span data-stu-id="7b8de-177">Hungarian</span></span>             | <span data-ttu-id="7b8de-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="7b8de-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="7b8de-179">Если не задать идентификатор языка для символа, идентификатор языка будет текущим ИДЕНТИФИКАТОРом языка системы, если установлена соответствующая библиотека DLL языка агента. в противном случае языком символа будет английский (США).</span><span class="sxs-lookup"><span data-stu-id="7b8de-179">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="7b8de-180">Это свойство также определяет язык для текста всплывающей подсказки, команды во всплывающем меню символа и модуль распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="7b8de-180">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="7b8de-181">Он также определяет язык по умолчанию для вывода TTS.</span><span class="sxs-lookup"><span data-stu-id="7b8de-181">It also determines the default language for TTS output.</span></span> <span data-ttu-id="7b8de-182">Чтобы определить, доступен ли совместимый модуль распознавания речи для языка символа, используйте [**иажентчарактерекс:: жетсрмодеид**](iagentcharacterex--getsrmodeid.md) или [**Иажентчарактерекс:: жетттсмодеид**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="7b8de-182">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="7b8de-183">Если вы попытаетесь задать идентификатор языка для символа и языковых ресурсов агента, кодовая страница или отображаемый шрифт для идентификатора языка недоступен, агент возвращает ошибку, а идентификатор языка символа остается в последнем задании.</span><span class="sxs-lookup"><span data-stu-id="7b8de-183">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="7b8de-184">Установка этого свойства не возвращает ошибку, если для языка нет соответствующих обработчиков речи.</span><span class="sxs-lookup"><span data-stu-id="7b8de-184">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="7b8de-185">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="7b8de-185">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="7b8de-186">Если задать в качестве идентификатора языка символа язык, поддерживающий двунаправленный текст (например, арабский или иврит), но в системе, в которой выполняется приложение, не установлена поддержка двунаправленного письма, текст будет отображаться в выноске слова логический, а не в порядке отображения.</span><span class="sxs-lookup"><span data-stu-id="7b8de-186">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="7b8de-187">См. также</span><span class="sxs-lookup"><span data-stu-id="7b8de-187">See Also</span></span>

<span data-ttu-id="7b8de-188">[**Иажентчарактерекс: жетлангуажеид**](iagentcharacterex--getlanguageid.md), [**Иажентчарактерекс:: жетсрмодеид**](iagentcharacterex--getsrmodeid.md), [**иажентчарактерекс:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="7b8de-188">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




