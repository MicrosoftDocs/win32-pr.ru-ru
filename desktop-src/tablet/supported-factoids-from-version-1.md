---
description: Платформа Tablet PC поддерживает ряд фактоидс, которые используются для повышения точности распознавания.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Поддерживаемые Фактоидс из версии 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674399"
---
# <a name="supported-factoids-from-version-1"></a><span data-ttu-id="f5596-103">Поддерживаемые Фактоидс из версии 1</span><span class="sxs-lookup"><span data-stu-id="f5596-103">Supported Factoids from Version 1</span></span>

<span data-ttu-id="f5596-104">\[Обратите внимание на следующее описание фактоидс, поддерживаемого в версии 1 пакета Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK), по-прежнему поддерживается распознавателями, но рекомендуется, чтобы все новые разработки (для распознавания символов латиницы) использовали значения, определенные в перечислении [инпутскопе](/windows/win32/api/inputscope/ne-inputscope-inputscope) .\]</span><span class="sxs-lookup"><span data-stu-id="f5596-104">\[Note the following description of the factoids supported in version 1 of the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) are still supported by recognizers, but it is recommended that all new development (for recognizers of Latin script) use the values defined in the [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration.\]</span></span>

<span data-ttu-id="f5596-105">Платформа Tablet PC поддерживает ряд фактоидс, которые используются для повышения точности распознавания.</span><span class="sxs-lookup"><span data-stu-id="f5596-105">The Tablet PC Platform supports a number of factoids that are used to increase recognition accuracy.</span></span> <span data-ttu-id="f5596-106">При использовании фактоидс важно, чтобы ожидаемые входные данные точно соответствовали определению фактоид.</span><span class="sxs-lookup"><span data-stu-id="f5596-106">When using factoids, it is important that the expected input exactly match the definition of the factoid.</span></span> <span data-ttu-id="f5596-107">Если входные данные не совпадают с определением фактоид, точность распознавания снижается.</span><span class="sxs-lookup"><span data-stu-id="f5596-107">If the input does not match the definition of the factoid, recognition accuracy suffers.</span></span> <span data-ttu-id="f5596-108">Например, если задано **число** фактоид и пользователь вводит буквы, точность распознавания букв будет низкой.</span><span class="sxs-lookup"><span data-stu-id="f5596-108">For example, if the **Number** factoid is set and the user enters letters, the recognition accuracy for letters is poor.</span></span>

<span data-ttu-id="f5596-109">Некоторые фактоидс, такие как **Электронная почта** и **цифра**, практически идентичны на разных языках.</span><span class="sxs-lookup"><span data-stu-id="f5596-109">Certain factoids, such as **Email** and **Digit**, are almost identical across languages.</span></span> <span data-ttu-id="f5596-110">Другие фактоидс, такие как **телефонные** и **PostalCode**, зависят от языка.</span><span class="sxs-lookup"><span data-stu-id="f5596-110">Other factoids, such as **Telephone** and **PostalCode**, vary by language.</span></span> <span data-ttu-id="f5596-111">Изучите формат каждого фактоид для используемого языка.</span><span class="sxs-lookup"><span data-stu-id="f5596-111">Examine the format of each factoid for the language that you are using.</span></span> <span data-ttu-id="f5596-112">Список форматов для каждого фактоид в каждом языке можно найти в таблицах в подразделах, следующих за этим разделом.</span><span class="sxs-lookup"><span data-stu-id="f5596-112">A list of formats for each factoid in each language can be found in the tables in the topics following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="f5596-113">Существует слабое, но важное различие между фактоидс для западных языков и фактоидс для восточно-азиатских языков.</span><span class="sxs-lookup"><span data-stu-id="f5596-113">There is a subtle but important distinction between factoids for western languages and factoids for East Asian languages.</span></span> <span data-ttu-id="f5596-114">Фактоидс для западных языков реализуются с помощью выражений, описывающих нужный результат.</span><span class="sxs-lookup"><span data-stu-id="f5596-114">Factoids for western languages are implemented by using expressions that describe the desired result.</span></span> <span data-ttu-id="f5596-115">Затем распознаватель получает результаты, соответствующие этому выражению.</span><span class="sxs-lookup"><span data-stu-id="f5596-115">The recognizer is then biased to produce results that match this expression.</span></span> <span data-ttu-id="f5596-116">Фактоидс для восточно-азиатских языков реализуются путем указания допустимого диапазона символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="f5596-116">Factoids for East Asian languages are implemented by specifying an acceptable range of Unicode characters.</span></span> <span data-ttu-id="f5596-117">Например, **Дата** фактоид для восточно-азиатских языков принимает только символы Юникода в пределах определенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="f5596-117">For example, the **Date** factoid for East Asian languages accepts only Unicode characters within a certain range.</span></span>

 

<span data-ttu-id="f5596-118">Фактоидс для западных языков включают фактоидс для английского языка (Великобритания), английского (США), французского, немецкого и испанского.</span><span class="sxs-lookup"><span data-stu-id="f5596-118">Factoids for western languages include factoids for English (United Kingdom), English (United States), French, German, and Spanish.</span></span> <span data-ttu-id="f5596-119">Фактоидс для восточноазиатских языков включают фактоидс для китайского языка (упрощенное письмо), китайский (традиционное письмо), японский и корейский.</span><span class="sxs-lookup"><span data-stu-id="f5596-119">Factoids for East Asian languages include factoids for Chinese (Simplified), Chinese (Traditional), Japanese, and Korean.</span></span>

<span data-ttu-id="f5596-120">В следующих разделах показаны форматы, поддерживаемые для каждого фактоид на каждом языке:</span><span class="sxs-lookup"><span data-stu-id="f5596-120">The following sections show the formats supported for each factoid in each language:</span></span>

-   [<span data-ttu-id="f5596-121">Фактоидс, общие для разных языков</span><span class="sxs-lookup"><span data-stu-id="f5596-121">Factoids Common Across Languages</span></span>](factoids-common-across-languages.md)
-   [<span data-ttu-id="f5596-122">Фактоидс для западных языков</span><span class="sxs-lookup"><span data-stu-id="f5596-122">Factoids for Western Languages</span></span>](factoids-for-western-languages.md)
-   [<span data-ttu-id="f5596-123">Фактоидс для восточно-азиатских языков</span><span class="sxs-lookup"><span data-stu-id="f5596-123">Factoids for East Asian Languages</span></span>](factoids-for-east-asian-languages.md)

<span data-ttu-id="f5596-124">Если предполагается, что входные данные отличаются от форматов, перечисленных в таблицах в этих разделах, не используйте фактоид.</span><span class="sxs-lookup"><span data-stu-id="f5596-124">If you expect input that is different from the formats listed in the tables in these sections, do not use a factoid.</span></span> <span data-ttu-id="f5596-125">Кроме того, фактоидс встроены в распознаватель для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="f5596-125">In addition, factoids are built into the recognizer for each language.</span></span> <span data-ttu-id="f5596-126">Нельзя использовать фактоидс на одном языке с распознавателем из другого языка.</span><span class="sxs-lookup"><span data-stu-id="f5596-126">You cannot use factoids from one language with a recognizer from another language.</span></span> <span data-ttu-id="f5596-127">Например, нельзя использовать французский **Телефон** фактоид с распознавателем японского языка.</span><span class="sxs-lookup"><span data-stu-id="f5596-127">For example, you cannot use the French **Telephone** factoid with a Japanese recognizer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5596-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f5596-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5596-129">**Константы фактоид**</span><span class="sxs-lookup"><span data-stu-id="f5596-129">**Factoid Constants**</span></span>](factoid-constants.md)
</dt> <dt>

<span data-ttu-id="f5596-130">[Класс Microsoft. Ink. фактоид](/previous-versions/ms583657(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="f5596-130">[Microsoft.Ink.Factoid Class](/previous-versions/ms583657(v=vs.100))</span></span>
</dt> </dl>

 

 
