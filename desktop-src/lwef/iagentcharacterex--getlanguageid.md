---
title: Иажентчарактерекс Жетлангуажеид
description: Иажентчарактерекс Жетлангуажеид
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d847bf392709b2433b045a357a703173e2de454
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120650"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="7eeba-103">Иажентчарактерекс:: Жетлангуажеид</span><span class="sxs-lookup"><span data-stu-id="7eeba-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="7eeba-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7eeba-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="7eeba-105">Возвращает идентификатор языка, заданный для символа.</span><span class="sxs-lookup"><span data-stu-id="7eeba-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="7eeba-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7eeba-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7eeba-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*плангид*</span><span class="sxs-lookup"><span data-stu-id="7eeba-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="7eeba-108">Адрес переменной, получающей параметр идентификатора языка для символа.</span><span class="sxs-lookup"><span data-stu-id="7eeba-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="7eeba-109">Длинное целое число, указывающее идентификатор языка для символа.</span><span class="sxs-lookup"><span data-stu-id="7eeba-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="7eeba-110">Идентификатор языка (LANGID) для символа — это 16-разрядное значение, определенное Windows, состоящее из основного идентификатора языка и дополнительного идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="7eeba-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="7eeba-111">Ниже приведены примеры значений для некоторых языков.</span><span class="sxs-lookup"><span data-stu-id="7eeba-111">The following examples are values for some languages.</span></span> <span data-ttu-id="7eeba-112">Чтобы определить значения других языков, см. документацию по пакету SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="7eeba-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="7eeba-113">Язык</span><span class="sxs-lookup"><span data-stu-id="7eeba-113">Language</span></span>              | <span data-ttu-id="7eeba-114">ID</span><span class="sxs-lookup"><span data-stu-id="7eeba-114">ID</span></span>     | <span data-ttu-id="7eeba-115">Язык</span><span class="sxs-lookup"><span data-stu-id="7eeba-115">Language</span></span>              | <span data-ttu-id="7eeba-116">ID</span><span class="sxs-lookup"><span data-stu-id="7eeba-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="7eeba-117">Арабский (Саудовская Аравия)</span><span class="sxs-lookup"><span data-stu-id="7eeba-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="7eeba-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="7eeba-118">0x0401</span></span> | <span data-ttu-id="7eeba-119">Итальянский</span><span class="sxs-lookup"><span data-stu-id="7eeba-119">Italian</span></span>               | <span data-ttu-id="7eeba-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="7eeba-120">0x0410</span></span> |
| <span data-ttu-id="7eeba-121">Баскский</span><span class="sxs-lookup"><span data-stu-id="7eeba-121">Basque</span></span>                | <span data-ttu-id="7eeba-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="7eeba-122">0x042d</span></span> | <span data-ttu-id="7eeba-123">Японский</span><span class="sxs-lookup"><span data-stu-id="7eeba-123">Japanese</span></span>              | <span data-ttu-id="7eeba-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="7eeba-124">0x0411</span></span> |
| <span data-ttu-id="7eeba-125">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="7eeba-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="7eeba-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="7eeba-126">0x0804</span></span> | <span data-ttu-id="7eeba-127">Корейский</span><span class="sxs-lookup"><span data-stu-id="7eeba-127">Korean</span></span>                | <span data-ttu-id="7eeba-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="7eeba-128">0x0412</span></span> |
| <span data-ttu-id="7eeba-129">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="7eeba-129">Chinese (Traditional)</span></span> | <span data-ttu-id="7eeba-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="7eeba-130">0x0404</span></span> | <span data-ttu-id="7eeba-131">Норвежский</span><span class="sxs-lookup"><span data-stu-id="7eeba-131">Norwegian</span></span>             | <span data-ttu-id="7eeba-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="7eeba-132">0x0414</span></span> |
| <span data-ttu-id="7eeba-133">Хорватский</span><span class="sxs-lookup"><span data-stu-id="7eeba-133">Croatian</span></span>              | <span data-ttu-id="7eeba-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="7eeba-134">0x041A</span></span> | <span data-ttu-id="7eeba-135">Польский</span><span class="sxs-lookup"><span data-stu-id="7eeba-135">Polish</span></span>                | <span data-ttu-id="7eeba-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="7eeba-136">0x0415</span></span> |
| <span data-ttu-id="7eeba-137">Чешский</span><span class="sxs-lookup"><span data-stu-id="7eeba-137">Czech</span></span>                 | <span data-ttu-id="7eeba-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="7eeba-138">0x0405</span></span> | <span data-ttu-id="7eeba-139">Португальский (Португалия)</span><span class="sxs-lookup"><span data-stu-id="7eeba-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="7eeba-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="7eeba-140">0x0816</span></span> |
| <span data-ttu-id="7eeba-141">Датский</span><span class="sxs-lookup"><span data-stu-id="7eeba-141">Danish</span></span>                | <span data-ttu-id="7eeba-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="7eeba-142">0x0406</span></span> | <span data-ttu-id="7eeba-143">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="7eeba-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="7eeba-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="7eeba-144">0x0416</span></span> |
| <span data-ttu-id="7eeba-145">Голландский</span><span class="sxs-lookup"><span data-stu-id="7eeba-145">Dutch</span></span>                 | <span data-ttu-id="7eeba-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="7eeba-146">0x0413</span></span> | <span data-ttu-id="7eeba-147">Румынский</span><span class="sxs-lookup"><span data-stu-id="7eeba-147">Romanian</span></span>              | <span data-ttu-id="7eeba-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="7eeba-148">0x0418</span></span> |
| <span data-ttu-id="7eeba-149">Английский (Великобритания)</span><span class="sxs-lookup"><span data-stu-id="7eeba-149">English (British)</span></span>     | <span data-ttu-id="7eeba-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="7eeba-150">0x0809</span></span> | <span data-ttu-id="7eeba-151">Русский</span><span class="sxs-lookup"><span data-stu-id="7eeba-151">Russian</span></span>               | <span data-ttu-id="7eeba-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="7eeba-152">0x0419</span></span> |
| <span data-ttu-id="7eeba-153">Английский (США)</span><span class="sxs-lookup"><span data-stu-id="7eeba-153">English (US)</span></span>          | <span data-ttu-id="7eeba-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="7eeba-154">0x0409</span></span> | <span data-ttu-id="7eeba-155">Словацкий</span><span class="sxs-lookup"><span data-stu-id="7eeba-155">Slovakian</span></span>             | <span data-ttu-id="7eeba-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="7eeba-156">0x041B</span></span> |
| <span data-ttu-id="7eeba-157">Финский</span><span class="sxs-lookup"><span data-stu-id="7eeba-157">Finnish</span></span>               | <span data-ttu-id="7eeba-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="7eeba-158">0x040B</span></span> | <span data-ttu-id="7eeba-159">Словенский</span><span class="sxs-lookup"><span data-stu-id="7eeba-159">Slovenian</span></span>             | <span data-ttu-id="7eeba-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="7eeba-160">0x0424</span></span> |
| <span data-ttu-id="7eeba-161">Французский</span><span class="sxs-lookup"><span data-stu-id="7eeba-161">French</span></span>                | <span data-ttu-id="7eeba-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="7eeba-162">0x040C</span></span> | <span data-ttu-id="7eeba-163">Испанский</span><span class="sxs-lookup"><span data-stu-id="7eeba-163">Spanish</span></span>               | <span data-ttu-id="7eeba-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="7eeba-164">0x0C0A</span></span> |
| <span data-ttu-id="7eeba-165">Немецкий</span><span class="sxs-lookup"><span data-stu-id="7eeba-165">German</span></span>                | <span data-ttu-id="7eeba-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="7eeba-166">0x0407</span></span> | <span data-ttu-id="7eeba-167">Шведский</span><span class="sxs-lookup"><span data-stu-id="7eeba-167">Swedish</span></span>               | <span data-ttu-id="7eeba-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="7eeba-168">0x041D</span></span> |
| <span data-ttu-id="7eeba-169">Греческий</span><span class="sxs-lookup"><span data-stu-id="7eeba-169">Greek</span></span>                 | <span data-ttu-id="7eeba-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="7eeba-170">0x0408</span></span> | <span data-ttu-id="7eeba-171">Тайский</span><span class="sxs-lookup"><span data-stu-id="7eeba-171">Thai</span></span>                  | <span data-ttu-id="7eeba-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="7eeba-172">0x041E</span></span> |
| <span data-ttu-id="7eeba-173">Иврит</span><span class="sxs-lookup"><span data-stu-id="7eeba-173">Hebrew</span></span>                | <span data-ttu-id="7eeba-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="7eeba-174">0x040D</span></span> | <span data-ttu-id="7eeba-175">Турецкий</span><span class="sxs-lookup"><span data-stu-id="7eeba-175">Turkish</span></span>               | <span data-ttu-id="7eeba-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="7eeba-176">0x041F</span></span> |
| <span data-ttu-id="7eeba-177">Венгерский</span><span class="sxs-lookup"><span data-stu-id="7eeba-177">Hungarian</span></span>             | <span data-ttu-id="7eeba-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="7eeba-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="7eeba-179">Если не задать этот идентификатор языка для символа, ИДЕНТИФИКАТОРом языка символа будет текущий идентификатор языка системы.</span><span class="sxs-lookup"><span data-stu-id="7eeba-179">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="7eeba-180">Этот параметр также определяет язык для вывода данных в формате TTS, текста всплывающей подсказки в Word, команд во всплывающем меню символа и модуля распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="7eeba-180">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="7eeba-181">Чтобы определить, доступен ли совместимый модуль распознавания речи для языка символа, используйте [**иажентчарактерекс:: жетсрмодеид**](iagentcharacterex--getsrmodeid.md) или [**Иажентчарактерекс:: жетттсмодеид**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="7eeba-181">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="7eeba-182">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="7eeba-182">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="7eeba-183">Если для идентификатора языка задан язык, поддерживающий двунаправленный текст (например, арабский или иврит), но в системе, в которой выполняется приложение, не установлена поддержка двунаправленного письма, текст будет отображаться в выноске слова логический, а не в порядке отображения.</span><span class="sxs-lookup"><span data-stu-id="7eeba-183">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="7eeba-184">См. также</span><span class="sxs-lookup"><span data-stu-id="7eeba-184">See Also</span></span>

<span data-ttu-id="7eeba-185">[**Иажентчарактерекс: сетлангуажеид**](iagentcharacterex--setlanguageid.md), [**Иажентчарактерекс:: жетсрмодеид**](iagentcharacterex--getsrmodeid.md), [**иажентчарактерекс:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="7eeba-185">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




