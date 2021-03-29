---
title: Иажентчарактерекс Сетлангуажеид
description: Иажентчарактерекс Сетлангуажеид
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774414"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="711c7-103">Иажентчарактерекс:: Сетлангуажеид</span><span class="sxs-lookup"><span data-stu-id="711c7-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="711c7-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="711c7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="711c7-105">Задает идентификатор языка, заданный для символа.</span><span class="sxs-lookup"><span data-stu-id="711c7-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="711c7-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="711c7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="711c7-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Надежно*</span><span class="sxs-lookup"><span data-stu-id="711c7-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="711c7-108">Параметр идентификатора языка для символа.</span><span class="sxs-lookup"><span data-stu-id="711c7-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="711c7-109">Длинное целое число, указывающее идентификатор языка для символа.</span><span class="sxs-lookup"><span data-stu-id="711c7-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="711c7-110">Идентификатор языка (LANGID) для символа — это 16-разрядное значение, определенное Windows, состоящее из основного идентификатора языка и дополнительного идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="711c7-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="711c7-111">Для указанных языков можно использовать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="711c7-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="711c7-112">Дополнительные сведения см. в документации по пакету Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="711c7-112">For more information, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="711c7-113">Арабский (Саудовская Аравия)</span><span class="sxs-lookup"><span data-stu-id="711c7-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="711c7-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="711c7-114">0x0401</span></span> | <span data-ttu-id="711c7-115">Итальянский</span><span class="sxs-lookup"><span data-stu-id="711c7-115">Italian</span></span>               | <span data-ttu-id="711c7-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="711c7-116">0x0410</span></span> |
| <span data-ttu-id="711c7-117">Баскский</span><span class="sxs-lookup"><span data-stu-id="711c7-117">Basque</span></span>                | <span data-ttu-id="711c7-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="711c7-118">0x042d</span></span> | <span data-ttu-id="711c7-119">Японский</span><span class="sxs-lookup"><span data-stu-id="711c7-119">Japanese</span></span>              | <span data-ttu-id="711c7-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="711c7-120">0x0411</span></span> |
| <span data-ttu-id="711c7-121">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="711c7-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="711c7-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="711c7-122">0x0804</span></span> | <span data-ttu-id="711c7-123">Корейский</span><span class="sxs-lookup"><span data-stu-id="711c7-123">Korean</span></span>                | <span data-ttu-id="711c7-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="711c7-124">0x0412</span></span> |
| <span data-ttu-id="711c7-125">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="711c7-125">Chinese (Traditional)</span></span> | <span data-ttu-id="711c7-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="711c7-126">0x0404</span></span> | <span data-ttu-id="711c7-127">Норвежский</span><span class="sxs-lookup"><span data-stu-id="711c7-127">Norwegian</span></span>             | <span data-ttu-id="711c7-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="711c7-128">0x0414</span></span> |
| <span data-ttu-id="711c7-129">Хорватский</span><span class="sxs-lookup"><span data-stu-id="711c7-129">Croatian</span></span>              | <span data-ttu-id="711c7-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="711c7-130">0x041A</span></span> | <span data-ttu-id="711c7-131">Польский</span><span class="sxs-lookup"><span data-stu-id="711c7-131">Polish</span></span>                | <span data-ttu-id="711c7-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="711c7-132">0x0415</span></span> |
| <span data-ttu-id="711c7-133">Чешский</span><span class="sxs-lookup"><span data-stu-id="711c7-133">Czech</span></span>                 | <span data-ttu-id="711c7-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="711c7-134">0x0405</span></span> | <span data-ttu-id="711c7-135">Португальский (Португалия)</span><span class="sxs-lookup"><span data-stu-id="711c7-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="711c7-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="711c7-136">0x0816</span></span> |
| <span data-ttu-id="711c7-137">Датский</span><span class="sxs-lookup"><span data-stu-id="711c7-137">Danish</span></span>                | <span data-ttu-id="711c7-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="711c7-138">0x0406</span></span> | <span data-ttu-id="711c7-139">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="711c7-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="711c7-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="711c7-140">0x0416</span></span> |
| <span data-ttu-id="711c7-141">Нидерландский</span><span class="sxs-lookup"><span data-stu-id="711c7-141">Dutch</span></span>                 | <span data-ttu-id="711c7-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="711c7-142">0x0413</span></span> | <span data-ttu-id="711c7-143">Румынский</span><span class="sxs-lookup"><span data-stu-id="711c7-143">Romanian</span></span>              | <span data-ttu-id="711c7-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="711c7-144">0x0418</span></span> |
| <span data-ttu-id="711c7-145">Английский (Великобритания)</span><span class="sxs-lookup"><span data-stu-id="711c7-145">English (British)</span></span>     | <span data-ttu-id="711c7-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="711c7-146">0x0809</span></span> | <span data-ttu-id="711c7-147">русском языке</span><span class="sxs-lookup"><span data-stu-id="711c7-147">Russian</span></span>               | <span data-ttu-id="711c7-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="711c7-148">0x0419</span></span> |
| <span data-ttu-id="711c7-149">Английский (США)</span><span class="sxs-lookup"><span data-stu-id="711c7-149">English (US)</span></span>          | <span data-ttu-id="711c7-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="711c7-150">0x0409</span></span> | <span data-ttu-id="711c7-151">Словацкий</span><span class="sxs-lookup"><span data-stu-id="711c7-151">Slovakian</span></span>             | <span data-ttu-id="711c7-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="711c7-152">0x041B</span></span> |
| <span data-ttu-id="711c7-153">Финский</span><span class="sxs-lookup"><span data-stu-id="711c7-153">Finnish</span></span>               | <span data-ttu-id="711c7-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="711c7-154">0x040B</span></span> | <span data-ttu-id="711c7-155">Словенский</span><span class="sxs-lookup"><span data-stu-id="711c7-155">Slovenian</span></span>             | <span data-ttu-id="711c7-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="711c7-156">0x0424</span></span> |
| <span data-ttu-id="711c7-157">Французский</span><span class="sxs-lookup"><span data-stu-id="711c7-157">French</span></span>                | <span data-ttu-id="711c7-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="711c7-158">0x040C</span></span> | <span data-ttu-id="711c7-159">Испанский</span><span class="sxs-lookup"><span data-stu-id="711c7-159">Spanish</span></span>               | <span data-ttu-id="711c7-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="711c7-160">0x0C0A</span></span> |
| <span data-ttu-id="711c7-161">Немецкий</span><span class="sxs-lookup"><span data-stu-id="711c7-161">German</span></span>                | <span data-ttu-id="711c7-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="711c7-162">0x0407</span></span> | <span data-ttu-id="711c7-163">Шведский</span><span class="sxs-lookup"><span data-stu-id="711c7-163">Swedish</span></span>               | <span data-ttu-id="711c7-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="711c7-164">0x041D</span></span> |
| <span data-ttu-id="711c7-165">Греческий</span><span class="sxs-lookup"><span data-stu-id="711c7-165">Greek</span></span>                 | <span data-ttu-id="711c7-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="711c7-166">0x0408</span></span> | <span data-ttu-id="711c7-167">Тайский</span><span class="sxs-lookup"><span data-stu-id="711c7-167">Thai</span></span>                  | <span data-ttu-id="711c7-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="711c7-168">0x041E</span></span> |
| <span data-ttu-id="711c7-169">Иврит</span><span class="sxs-lookup"><span data-stu-id="711c7-169">Hebrew</span></span>                | <span data-ttu-id="711c7-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="711c7-170">0x040D</span></span> | <span data-ttu-id="711c7-171">Турецкий</span><span class="sxs-lookup"><span data-stu-id="711c7-171">Turkish</span></span>               | <span data-ttu-id="711c7-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="711c7-172">0x041F</span></span> |
| <span data-ttu-id="711c7-173">Венгерский</span><span class="sxs-lookup"><span data-stu-id="711c7-173">Hungarian</span></span>             | <span data-ttu-id="711c7-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="711c7-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="711c7-175">Если не задать идентификатор языка для символа, идентификатор языка будет текущим ИДЕНТИФИКАТОРом языка системы, если установлена соответствующая библиотека DLL языка агента. в противном случае языком символа будет английский (США).</span><span class="sxs-lookup"><span data-stu-id="711c7-175">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="711c7-176">Это свойство также определяет язык для текста всплывающей подсказки, команды во всплывающем меню символа и модуль распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="711c7-176">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="711c7-177">Он также определяет язык по умолчанию для вывода TTS.</span><span class="sxs-lookup"><span data-stu-id="711c7-177">It also determines the default language for TTS output.</span></span> <span data-ttu-id="711c7-178">Чтобы определить, доступен ли совместимый модуль распознавания речи для языка символа, используйте [**иажентчарактерекс:: жетсрмодеид**](iagentcharacterex--getsrmodeid.md) или [**Иажентчарактерекс:: жетттсмодеид**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="711c7-178">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="711c7-179">Если вы попытаетесь задать идентификатор языка для символа и языковых ресурсов агента, кодовая страница или отображаемый шрифт для идентификатора языка недоступен, агент возвращает ошибку, а идентификатор языка символа остается в последнем задании.</span><span class="sxs-lookup"><span data-stu-id="711c7-179">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="711c7-180">Установка этого свойства не возвращает ошибку, если для языка нет соответствующих обработчиков речи.</span><span class="sxs-lookup"><span data-stu-id="711c7-180">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="711c7-181">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="711c7-181">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="711c7-182">Если задать в качестве идентификатора языка символа язык, поддерживающий двунаправленный текст (например, арабский или иврит), но в системе, в которой выполняется приложение, не установлена поддержка двунаправленного письма, текст будет отображаться в выноске слова логический, а не в порядке отображения.</span><span class="sxs-lookup"><span data-stu-id="711c7-182">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="711c7-183">См. также:</span><span class="sxs-lookup"><span data-stu-id="711c7-183">See Also</span></span>

<span data-ttu-id="711c7-184">[**Иажентчарактерекс: жетлангуажеид**](iagentcharacterex--getlanguageid.md), [**Иажентчарактерекс:: жетсрмодеид**](iagentcharacterex--getsrmodeid.md), [**иажентчарактерекс:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="711c7-184">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




