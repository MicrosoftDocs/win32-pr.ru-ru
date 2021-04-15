---
description: сскриптс ЛОКАЛи \_
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662498"
---
# <a name="locale_sscripts"></a><span data-ttu-id="2fcdd-103">сскриптс ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="2fcdd-103">LOCALE\_SSCRIPTS</span></span>

<span data-ttu-id="2fcdd-104">**Windows Vista и более поздние версии:** Строка, представляющая список скриптов с использованием 4-символьной нотации, используемой в [стандарте ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="2fcdd-104">**Windows Vista and later:** A string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="2fcdd-105">Имя каждого сценария состоит из четырех латинских символов, а список упорядочивается в алфавитном порядке с каждым именем, включая фамилию, за которой следует точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="2fcdd-105">Each script name consists of four Latin characters and the list is arranged in alphabetical order with each name, including the last, followed by a semicolon.</span></span>

<span data-ttu-id="2fcdd-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) или [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) можно вызвать с параметром *LCType* , установленным в \_ сскриптс locale, как часть стратегии, чтобы устранить проблемы безопасности, связанные с международными доменными именами (IDNs).</span><span class="sxs-lookup"><span data-stu-id="2fcdd-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) can be called with *LCType* set to LOCALE\_SSCRIPTS as part of a strategy to mitigate security issues related to Internationalized Domain Names (IDNs).</span></span> <span data-ttu-id="2fcdd-107">Ниже приведены некоторые примеры значений.</span><span class="sxs-lookup"><span data-stu-id="2fcdd-107">Here are some example values:</span></span>



| <span data-ttu-id="2fcdd-108">Locale</span><span class="sxs-lookup"><span data-stu-id="2fcdd-108">Locale</span></span>                  | <span data-ttu-id="2fcdd-109">Языковой стандарт или имя языка</span><span class="sxs-lookup"><span data-stu-id="2fcdd-109">Locale/language name</span></span> | <span data-ttu-id="2fcdd-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2fcdd-110">Value</span></span>                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcdd-111">Английский (США)</span><span class="sxs-lookup"><span data-stu-id="2fcdd-111">English (United States)</span></span> | <span data-ttu-id="2fcdd-112">ru-RU</span><span class="sxs-lookup"><span data-stu-id="2fcdd-112">en-US</span></span>                | <span data-ttu-id="2fcdd-113">ЛАТН;</span><span class="sxs-lookup"><span data-stu-id="2fcdd-113">Latn;</span></span>                                                                                                  |
| <span data-ttu-id="2fcdd-114">Хинди (Индия)</span><span class="sxs-lookup"><span data-stu-id="2fcdd-114">Hindi (India)</span></span>           | <span data-ttu-id="2fcdd-115">hi-IN</span><span class="sxs-lookup"><span data-stu-id="2fcdd-115">hi-IN</span></span>                | <span data-ttu-id="2fcdd-116">Дева;</span><span class="sxs-lookup"><span data-stu-id="2fcdd-116">Deva;</span></span>                                                                                                  |
| <span data-ttu-id="2fcdd-117">Японский (Япония)</span><span class="sxs-lookup"><span data-stu-id="2fcdd-117">Japanese (Japan)</span></span>        | <span data-ttu-id="2fcdd-118">ja-JP</span><span class="sxs-lookup"><span data-stu-id="2fcdd-118">ja-JP</span></span>                | <span data-ttu-id="2fcdd-119">**Windows 7 и более поздние версии:** Хани; Хира; Жпан; Знаков</span><span class="sxs-lookup"><span data-stu-id="2fcdd-119">**Windows 7 and later:** Hani;Hira;Jpan;Kana;</span></span><br/> <span data-ttu-id="2fcdd-120">**Windows Vista:** Хани; Хира; Знаков</span><span class="sxs-lookup"><span data-stu-id="2fcdd-120">**Windows Vista:** Hani;Hira;Kana;</span></span><br/> |



 

<span data-ttu-id="2fcdd-121">Значение составного скрипта не включает Латинский сценарий, если он не является важнейшей частью системы записи, используемой для конкретного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="2fcdd-121">A compound script value does not include the Latin script unless it is an essential part of the writing system used for the particular locale.</span></span> <span data-ttu-id="2fcdd-122">Символы латиницы часто используются в контексте национальных настроек, для которых они не являются собственными, например для внешнего имени компании.</span><span class="sxs-lookup"><span data-stu-id="2fcdd-122">Latin characters are often used in the context of locales for which they are not native, for example, for a foreign business name.</span></span> <span data-ttu-id="2fcdd-123">В приведенном выше примере для языка хинди в Индии единственным значением сценария является «Дева» (для «деванагари»), хотя символы латиницы также могут отображаться в тексте на языке хинди.</span><span class="sxs-lookup"><span data-stu-id="2fcdd-123">In the example above for Hindi in India, the only script value is "Deva" (for "Devanagari"), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="2fcdd-124">Функция [верифискриптс](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) имеет специальный флаг для решения этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="2fcdd-124">The [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) function has a special flag to address this case.</span></span>

 

 




