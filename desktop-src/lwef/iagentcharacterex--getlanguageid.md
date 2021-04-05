---
title: Иажентчарактерекс Жетлангуажеид
description: Иажентчарактерекс Жетлангуажеид
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068331"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="a816b-103">Иажентчарактерекс:: Жетлангуажеид</span><span class="sxs-lookup"><span data-stu-id="a816b-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="a816b-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a816b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="a816b-105">Возвращает идентификатор языка, заданный для символа.</span><span class="sxs-lookup"><span data-stu-id="a816b-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="a816b-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a816b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a816b-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*плангид*</span><span class="sxs-lookup"><span data-stu-id="a816b-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="a816b-108">Адрес переменной, получающей параметр идентификатора языка для символа.</span><span class="sxs-lookup"><span data-stu-id="a816b-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="a816b-109">Длинное целое число, указывающее идентификатор языка для символа.</span><span class="sxs-lookup"><span data-stu-id="a816b-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="a816b-110">Идентификатор языка (LANGID) для символа — это 16-разрядное значение, определенное Windows, состоящее из основного идентификатора языка и дополнительного идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="a816b-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="a816b-111">Ниже приведены примеры значений для некоторых языков.</span><span class="sxs-lookup"><span data-stu-id="a816b-111">The following examples are values for some languages.</span></span> <span data-ttu-id="a816b-112">Чтобы определить значения других языков, см. документацию по пакету SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="a816b-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="a816b-113">Арабский (Саудовская Аравия)</span><span class="sxs-lookup"><span data-stu-id="a816b-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="a816b-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="a816b-114">0x0401</span></span> | <span data-ttu-id="a816b-115">Итальянский</span><span class="sxs-lookup"><span data-stu-id="a816b-115">Italian</span></span>               | <span data-ttu-id="a816b-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="a816b-116">0x0410</span></span> |
| <span data-ttu-id="a816b-117">Баскский</span><span class="sxs-lookup"><span data-stu-id="a816b-117">Basque</span></span>                | <span data-ttu-id="a816b-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="a816b-118">0x042d</span></span> | <span data-ttu-id="a816b-119">Японский</span><span class="sxs-lookup"><span data-stu-id="a816b-119">Japanese</span></span>              | <span data-ttu-id="a816b-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="a816b-120">0x0411</span></span> |
| <span data-ttu-id="a816b-121">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="a816b-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="a816b-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="a816b-122">0x0804</span></span> | <span data-ttu-id="a816b-123">Корейский</span><span class="sxs-lookup"><span data-stu-id="a816b-123">Korean</span></span>                | <span data-ttu-id="a816b-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="a816b-124">0x0412</span></span> |
| <span data-ttu-id="a816b-125">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="a816b-125">Chinese (Traditional)</span></span> | <span data-ttu-id="a816b-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="a816b-126">0x0404</span></span> | <span data-ttu-id="a816b-127">Норвежский</span><span class="sxs-lookup"><span data-stu-id="a816b-127">Norwegian</span></span>             | <span data-ttu-id="a816b-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="a816b-128">0x0414</span></span> |
| <span data-ttu-id="a816b-129">Хорватский</span><span class="sxs-lookup"><span data-stu-id="a816b-129">Croatian</span></span>              | <span data-ttu-id="a816b-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="a816b-130">0x041A</span></span> | <span data-ttu-id="a816b-131">Польский</span><span class="sxs-lookup"><span data-stu-id="a816b-131">Polish</span></span>                | <span data-ttu-id="a816b-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="a816b-132">0x0415</span></span> |
| <span data-ttu-id="a816b-133">Чешский</span><span class="sxs-lookup"><span data-stu-id="a816b-133">Czech</span></span>                 | <span data-ttu-id="a816b-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="a816b-134">0x0405</span></span> | <span data-ttu-id="a816b-135">Португальский (Португалия)</span><span class="sxs-lookup"><span data-stu-id="a816b-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="a816b-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="a816b-136">0x0816</span></span> |
| <span data-ttu-id="a816b-137">Датский</span><span class="sxs-lookup"><span data-stu-id="a816b-137">Danish</span></span>                | <span data-ttu-id="a816b-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="a816b-138">0x0406</span></span> | <span data-ttu-id="a816b-139">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="a816b-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="a816b-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="a816b-140">0x0416</span></span> |
| <span data-ttu-id="a816b-141">Нидерландский</span><span class="sxs-lookup"><span data-stu-id="a816b-141">Dutch</span></span>                 | <span data-ttu-id="a816b-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="a816b-142">0x0413</span></span> | <span data-ttu-id="a816b-143">Румынский</span><span class="sxs-lookup"><span data-stu-id="a816b-143">Romanian</span></span>              | <span data-ttu-id="a816b-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="a816b-144">0x0418</span></span> |
| <span data-ttu-id="a816b-145">Английский (Великобритания)</span><span class="sxs-lookup"><span data-stu-id="a816b-145">English (British)</span></span>     | <span data-ttu-id="a816b-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="a816b-146">0x0809</span></span> | <span data-ttu-id="a816b-147">русском языке</span><span class="sxs-lookup"><span data-stu-id="a816b-147">Russian</span></span>               | <span data-ttu-id="a816b-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="a816b-148">0x0419</span></span> |
| <span data-ttu-id="a816b-149">Английский (США)</span><span class="sxs-lookup"><span data-stu-id="a816b-149">English (US)</span></span>          | <span data-ttu-id="a816b-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="a816b-150">0x0409</span></span> | <span data-ttu-id="a816b-151">Словацкий</span><span class="sxs-lookup"><span data-stu-id="a816b-151">Slovakian</span></span>             | <span data-ttu-id="a816b-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="a816b-152">0x041B</span></span> |
| <span data-ttu-id="a816b-153">Финский</span><span class="sxs-lookup"><span data-stu-id="a816b-153">Finnish</span></span>               | <span data-ttu-id="a816b-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="a816b-154">0x040B</span></span> | <span data-ttu-id="a816b-155">Словенский</span><span class="sxs-lookup"><span data-stu-id="a816b-155">Slovenian</span></span>             | <span data-ttu-id="a816b-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="a816b-156">0x0424</span></span> |
| <span data-ttu-id="a816b-157">Французский</span><span class="sxs-lookup"><span data-stu-id="a816b-157">French</span></span>                | <span data-ttu-id="a816b-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="a816b-158">0x040C</span></span> | <span data-ttu-id="a816b-159">Испанский</span><span class="sxs-lookup"><span data-stu-id="a816b-159">Spanish</span></span>               | <span data-ttu-id="a816b-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="a816b-160">0x0C0A</span></span> |
| <span data-ttu-id="a816b-161">Немецкий</span><span class="sxs-lookup"><span data-stu-id="a816b-161">German</span></span>                | <span data-ttu-id="a816b-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="a816b-162">0x0407</span></span> | <span data-ttu-id="a816b-163">Шведский</span><span class="sxs-lookup"><span data-stu-id="a816b-163">Swedish</span></span>               | <span data-ttu-id="a816b-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="a816b-164">0x041D</span></span> |
| <span data-ttu-id="a816b-165">Греческий</span><span class="sxs-lookup"><span data-stu-id="a816b-165">Greek</span></span>                 | <span data-ttu-id="a816b-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="a816b-166">0x0408</span></span> | <span data-ttu-id="a816b-167">Тайский</span><span class="sxs-lookup"><span data-stu-id="a816b-167">Thai</span></span>                  | <span data-ttu-id="a816b-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="a816b-168">0x041E</span></span> |
| <span data-ttu-id="a816b-169">Иврит</span><span class="sxs-lookup"><span data-stu-id="a816b-169">Hebrew</span></span>                | <span data-ttu-id="a816b-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="a816b-170">0x040D</span></span> | <span data-ttu-id="a816b-171">Турецкий</span><span class="sxs-lookup"><span data-stu-id="a816b-171">Turkish</span></span>               | <span data-ttu-id="a816b-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="a816b-172">0x041F</span></span> |
| <span data-ttu-id="a816b-173">Венгерский</span><span class="sxs-lookup"><span data-stu-id="a816b-173">Hungarian</span></span>             | <span data-ttu-id="a816b-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="a816b-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="a816b-175">Если не задать этот идентификатор языка для символа, ИДЕНТИФИКАТОРом языка символа будет текущий идентификатор языка системы.</span><span class="sxs-lookup"><span data-stu-id="a816b-175">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="a816b-176">Этот параметр также определяет язык для вывода данных в формате TTS, текста всплывающей подсказки в Word, команд во всплывающем меню символа и модуля распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="a816b-176">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="a816b-177">Чтобы определить, доступен ли совместимый модуль распознавания речи для языка символа, используйте [**иажентчарактерекс:: жетсрмодеид**](iagentcharacterex--getsrmodeid.md) или [**Иажентчарактерекс:: жетттсмодеид**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="a816b-177">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="a816b-178">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="a816b-178">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="a816b-179">Если для идентификатора языка задан язык, поддерживающий двунаправленный текст (например, арабский или иврит), но в системе, в которой выполняется приложение, не установлена поддержка двунаправленного письма, текст будет отображаться в выноске слова логический, а не в порядке отображения.</span><span class="sxs-lookup"><span data-stu-id="a816b-179">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="a816b-180">См. также:</span><span class="sxs-lookup"><span data-stu-id="a816b-180">See Also</span></span>

<span data-ttu-id="a816b-181">[**Иажентчарактерекс: сетлангуажеид**](iagentcharacterex--setlanguageid.md), [**Иажентчарактерекс:: жетсрмодеид**](iagentcharacterex--getsrmodeid.md), [**иажентчарактерекс:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="a816b-181">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




