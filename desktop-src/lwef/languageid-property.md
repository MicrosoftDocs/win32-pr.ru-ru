---
title: LanguageID, свойство
description: LanguageID, свойство
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331995"
---
# <a name="languageid-property"></a><span data-ttu-id="39fc3-103">LanguageID, свойство</span><span class="sxs-lookup"><span data-stu-id="39fc3-103">LanguageID Property</span></span>

<span data-ttu-id="39fc3-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="39fc3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="39fc3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="39fc3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="39fc3-106">Возвращает или задает идентификатор языка для символа.</span><span class="sxs-lookup"><span data-stu-id="39fc3-106">Returns or sets the language ID for the character.</span></span>

</dd> <dt>

<span data-ttu-id="39fc3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="39fc3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="39fc3-108">Символы агента. \*\* \* \*\* \*  **("***Чарактерид***"). LanguageID** \[  =  *LanguageID*\]</span><span class="sxs-lookup"><span data-stu-id="39fc3-108">*agent.\*\*\*Characters*\* **("***CharacterID***").LanguageID** \[ = *LanguageID*\]</span></span>



<span data-ttu-id="39fc3-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="39fc3-109">Part</span></span>

<span data-ttu-id="39fc3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="39fc3-110">Description</span></span>

<span data-ttu-id="39fc3-111">LanguageID</span><span class="sxs-lookup"><span data-stu-id="39fc3-111">LanguageID</span></span>

<span data-ttu-id="39fc3-112">Длинное целое число, указывающее идентификатор языка для символа.</span><span class="sxs-lookup"><span data-stu-id="39fc3-112">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="39fc3-113">Идентификатор языка (LANGID) для символа — это 16-разрядное значение, определенное Windows, состоящее из основного идентификатора языка и дополнительного идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="39fc3-113">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="39fc3-114">Ниже приведены примеры значений для языков, поддерживаемых Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="39fc3-114">The following examples are values for languages supported by Microsoft Agent.</span></span> <span data-ttu-id="39fc3-115">Чтобы определить значения для других языков, см. *документацию по пакету SDK для платформы*.</span><span class="sxs-lookup"><span data-stu-id="39fc3-115">To determine the value for other languages, see the *Platform SDK documentation*.</span></span>

 

<span data-ttu-id="39fc3-116">Арабский</span><span class="sxs-lookup"><span data-stu-id="39fc3-116">Arabic</span></span>

<span data-ttu-id="39fc3-117">&H0401</span><span class="sxs-lookup"><span data-stu-id="39fc3-117">&H0401</span></span>

<span data-ttu-id="39fc3-118">Итальянский</span><span class="sxs-lookup"><span data-stu-id="39fc3-118">Italian</span></span>

<span data-ttu-id="39fc3-119">&H0410</span><span class="sxs-lookup"><span data-stu-id="39fc3-119">&H0410</span></span>

 

<span data-ttu-id="39fc3-120">Баскский</span><span class="sxs-lookup"><span data-stu-id="39fc3-120">Basque</span></span>

<span data-ttu-id="39fc3-121">&H042D</span><span class="sxs-lookup"><span data-stu-id="39fc3-121">&H042D</span></span>

<span data-ttu-id="39fc3-122">Японский</span><span class="sxs-lookup"><span data-stu-id="39fc3-122">Japanese</span></span>

<span data-ttu-id="39fc3-123">&H0411</span><span class="sxs-lookup"><span data-stu-id="39fc3-123">&H0411</span></span>

 

<span data-ttu-id="39fc3-124">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="39fc3-124">Chinese (Simplified)</span></span>

<span data-ttu-id="39fc3-125">&H0804</span><span class="sxs-lookup"><span data-stu-id="39fc3-125">&H0804</span></span>

<span data-ttu-id="39fc3-126">Корейский</span><span class="sxs-lookup"><span data-stu-id="39fc3-126">Korean</span></span>

<span data-ttu-id="39fc3-127">&H0412</span><span class="sxs-lookup"><span data-stu-id="39fc3-127">&H0412</span></span>

 

<span data-ttu-id="39fc3-128">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="39fc3-128">Chinese (Traditional)</span></span>

<span data-ttu-id="39fc3-129">&H0404</span><span class="sxs-lookup"><span data-stu-id="39fc3-129">&H0404</span></span>

<span data-ttu-id="39fc3-130">Норвежский</span><span class="sxs-lookup"><span data-stu-id="39fc3-130">Norwegian</span></span>

<span data-ttu-id="39fc3-131">&H0414</span><span class="sxs-lookup"><span data-stu-id="39fc3-131">&H0414</span></span>

 

<span data-ttu-id="39fc3-132">Хорватский</span><span class="sxs-lookup"><span data-stu-id="39fc3-132">Croatian</span></span>

<span data-ttu-id="39fc3-133">&H041A</span><span class="sxs-lookup"><span data-stu-id="39fc3-133">&H041A</span></span>

<span data-ttu-id="39fc3-134">Польский</span><span class="sxs-lookup"><span data-stu-id="39fc3-134">Polish</span></span>

<span data-ttu-id="39fc3-135">&H0415</span><span class="sxs-lookup"><span data-stu-id="39fc3-135">&H0415</span></span>

 

<span data-ttu-id="39fc3-136">Чешский</span><span class="sxs-lookup"><span data-stu-id="39fc3-136">Czech</span></span>

<span data-ttu-id="39fc3-137">&H0405</span><span class="sxs-lookup"><span data-stu-id="39fc3-137">&H0405</span></span>

<span data-ttu-id="39fc3-138">Португальский (Португалия)</span><span class="sxs-lookup"><span data-stu-id="39fc3-138">Portuguese (Portugal)</span></span>

<span data-ttu-id="39fc3-139">&H0816</span><span class="sxs-lookup"><span data-stu-id="39fc3-139">&H0816</span></span>

 

<span data-ttu-id="39fc3-140">Датский</span><span class="sxs-lookup"><span data-stu-id="39fc3-140">Danish</span></span>

<span data-ttu-id="39fc3-141">&H0406</span><span class="sxs-lookup"><span data-stu-id="39fc3-141">&H0406</span></span>

<span data-ttu-id="39fc3-142">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="39fc3-142">Portuguese (Brazil)</span></span>

<span data-ttu-id="39fc3-143">&H0416</span><span class="sxs-lookup"><span data-stu-id="39fc3-143">&H0416</span></span>

 

<span data-ttu-id="39fc3-144">Нидерландский</span><span class="sxs-lookup"><span data-stu-id="39fc3-144">Dutch</span></span>

<span data-ttu-id="39fc3-145">&H0413</span><span class="sxs-lookup"><span data-stu-id="39fc3-145">&H0413</span></span>

<span data-ttu-id="39fc3-146">Румынский</span><span class="sxs-lookup"><span data-stu-id="39fc3-146">Romanian</span></span>

<span data-ttu-id="39fc3-147">&H0418</span><span class="sxs-lookup"><span data-stu-id="39fc3-147">&H0418</span></span>

 

<span data-ttu-id="39fc3-148">Английский (Великобритания)</span><span class="sxs-lookup"><span data-stu-id="39fc3-148">English (British)</span></span>

<span data-ttu-id="39fc3-149">&H0809</span><span class="sxs-lookup"><span data-stu-id="39fc3-149">&H0809</span></span>

<span data-ttu-id="39fc3-150">русском языке</span><span class="sxs-lookup"><span data-stu-id="39fc3-150">Russian</span></span>

<span data-ttu-id="39fc3-151">&H0419</span><span class="sxs-lookup"><span data-stu-id="39fc3-151">&H0419</span></span>

 

<span data-ttu-id="39fc3-152">Английский (США)</span><span class="sxs-lookup"><span data-stu-id="39fc3-152">English (US)</span></span>

<span data-ttu-id="39fc3-153">&H0409</span><span class="sxs-lookup"><span data-stu-id="39fc3-153">&H0409</span></span>

<span data-ttu-id="39fc3-154">Словацкий</span><span class="sxs-lookup"><span data-stu-id="39fc3-154">Slovakian</span></span>

<span data-ttu-id="39fc3-155">&H041B</span><span class="sxs-lookup"><span data-stu-id="39fc3-155">&H041B</span></span>

 

<span data-ttu-id="39fc3-156">Финский</span><span class="sxs-lookup"><span data-stu-id="39fc3-156">Finnish</span></span>

<span data-ttu-id="39fc3-157">&H040B</span><span class="sxs-lookup"><span data-stu-id="39fc3-157">&H040B</span></span>

<span data-ttu-id="39fc3-158">Словенский</span><span class="sxs-lookup"><span data-stu-id="39fc3-158">Slovenian</span></span>

<span data-ttu-id="39fc3-159">&H0424</span><span class="sxs-lookup"><span data-stu-id="39fc3-159">&H0424</span></span>

 

<span data-ttu-id="39fc3-160">Французский</span><span class="sxs-lookup"><span data-stu-id="39fc3-160">French</span></span>

<span data-ttu-id="39fc3-161">&H040C</span><span class="sxs-lookup"><span data-stu-id="39fc3-161">&H040C</span></span>

<span data-ttu-id="39fc3-162">Испанский</span><span class="sxs-lookup"><span data-stu-id="39fc3-162">Spanish</span></span>

<span data-ttu-id="39fc3-163">&H0C0A</span><span class="sxs-lookup"><span data-stu-id="39fc3-163">&H0C0A</span></span>

 

<span data-ttu-id="39fc3-164">Немецкий</span><span class="sxs-lookup"><span data-stu-id="39fc3-164">German</span></span>

<span data-ttu-id="39fc3-165">&H0407</span><span class="sxs-lookup"><span data-stu-id="39fc3-165">&H0407</span></span>

<span data-ttu-id="39fc3-166">Шведский</span><span class="sxs-lookup"><span data-stu-id="39fc3-166">Swedish</span></span>

<span data-ttu-id="39fc3-167">&H041D</span><span class="sxs-lookup"><span data-stu-id="39fc3-167">&H041D</span></span>

 

<span data-ttu-id="39fc3-168">Греческий</span><span class="sxs-lookup"><span data-stu-id="39fc3-168">Greek</span></span>

<span data-ttu-id="39fc3-169">&H0408</span><span class="sxs-lookup"><span data-stu-id="39fc3-169">&H0408</span></span>

<span data-ttu-id="39fc3-170">Тайский</span><span class="sxs-lookup"><span data-stu-id="39fc3-170">Thai</span></span>

<span data-ttu-id="39fc3-171">&H041E</span><span class="sxs-lookup"><span data-stu-id="39fc3-171">&H041E</span></span>

 

<span data-ttu-id="39fc3-172">Иврит</span><span class="sxs-lookup"><span data-stu-id="39fc3-172">Hebrew</span></span>

<span data-ttu-id="39fc3-173">&H040D</span><span class="sxs-lookup"><span data-stu-id="39fc3-173">&H040D</span></span>

<span data-ttu-id="39fc3-174">Турецкий</span><span class="sxs-lookup"><span data-stu-id="39fc3-174">Turkish</span></span>

<span data-ttu-id="39fc3-175">&H041F</span><span class="sxs-lookup"><span data-stu-id="39fc3-175">&H041F</span></span>

 

<span data-ttu-id="39fc3-176">Венгерский</span><span class="sxs-lookup"><span data-stu-id="39fc3-176">Hungarian</span></span>

<span data-ttu-id="39fc3-177">&H040E</span><span class="sxs-lookup"><span data-stu-id="39fc3-177">&H040E</span></span>

 

 



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39fc3-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39fc3-178">Remarks</span></span>

<span data-ttu-id="39fc3-179">Если для символа не задано значение **LanguageID** , идентификатор языка будет соответствовать ТЕКУЩЕМу идентификатору языка системы, если установлена соответствующая библиотека DLL языка агента. в противном случае язык символа будет АНГЛИЙСКИМ (US).</span><span class="sxs-lookup"><span data-stu-id="39fc3-179">If you do not set the **LanguageID** for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed, otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="39fc3-180">Это свойство также определяет язык для текста всплывающей подсказки по слову, команды во всплывающем меню символа и модуль распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="39fc3-180">This property also determines the language for word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="39fc3-181">Он также определяет язык по умолчанию для вывода TTS.</span><span class="sxs-lookup"><span data-stu-id="39fc3-181">It also determines the default language for TTS output.</span></span>

<span data-ttu-id="39fc3-182">Если вы попытаетесь задать **LanguageID** для символа, а библиотека DLL языка агента для этого языка не установлена или шрифт не отображается для идентификатора языка, то агент выдает ошибку, и **LanguageID** остается в последнем задании.</span><span class="sxs-lookup"><span data-stu-id="39fc3-182">If you try to set the **LanguageID** for a character and the Agent language DLL for that language is not installed or a display font for the language ID is not available, Agent raises an error and **LanguageID** remains at its last setting.</span></span>

<span data-ttu-id="39fc3-183">Установка этого свойства не вызывает ошибку, если для языка нет соответствующих обработчиков речи.</span><span class="sxs-lookup"><span data-stu-id="39fc3-183">Setting this property does not raise an error if there are no matching speech engines for the language.</span></span> <span data-ttu-id="39fc3-184">Чтобы определить, доступен ли совместимый модуль распознавания речи для **LanguageID**, проверьте [**срмодеид**](srmodeid-property.md) или [**ттсмодеид**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="39fc3-184">To determine if there is a compatible speech engine available for the **LanguageID**, check [**SRModeID**](srmodeid-property.md) or [**TTSModeID**](ttsmodeid-property.md).</span></span> <span data-ttu-id="39fc3-185">Если параметр **LanguageID** не задан, для него будет задано значение по умолчанию для параметра идентификатор языка пользователя.</span><span class="sxs-lookup"><span data-stu-id="39fc3-185">If you do not set **LanguageID**, it will be set to the user default language ID setting.</span></span>

<span data-ttu-id="39fc3-186">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="39fc3-186">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="39fc3-187">Если задать для **LanguageID** язык, поддерживающий двунаправленный текст (например, арабский или иврит), но в системе, где выполняется приложение, не установлена поддержка двунаправленного письма, текст в выноске слова будет отображаться как логический, а не как порядок отображения.</span><span class="sxs-lookup"><span data-stu-id="39fc3-187">If you set **LanguageID** to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text in the word balloon will appear in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="39fc3-188">См. также:</span><span class="sxs-lookup"><span data-stu-id="39fc3-188">See Also</span></span>

<span data-ttu-id="39fc3-189">[**Свойство срмодеид**](srmodeid-property.md), [ **свойство ттсмодеид**](ttsmodeid-property.md)</span><span class="sxs-lookup"><span data-stu-id="39fc3-189">[**SRModeID property**](srmodeid-property.md), [**TTSModeID property**](ttsmodeid-property.md)</span></span>


 

 




