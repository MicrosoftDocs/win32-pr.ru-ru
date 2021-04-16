---
description: Служба обнаружения языка ELS называется Microsoft распознавание языка. Эта служба использует технологию, запатентованную корпорацией Майкрософт, чтобы позволить приложениям определять язык, на котором написан конкретный текст.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Microsoft распознавание языка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682995"
---
# <a name="microsoft-language-detection"></a><span data-ttu-id="783de-104">Microsoft распознавание языка</span><span class="sxs-lookup"><span data-stu-id="783de-104">Microsoft Language Detection</span></span>

<span data-ttu-id="783de-105">Служба обнаружения языка ELS называется Microsoft распознавание языка.</span><span class="sxs-lookup"><span data-stu-id="783de-105">The ELS language detection service is called Microsoft Language Detection.</span></span> <span data-ttu-id="783de-106">Эта служба использует технологию, запатентованную корпорацией Майкрософт, чтобы позволить приложениям определять язык, на котором написан конкретный текст.</span><span class="sxs-lookup"><span data-stu-id="783de-106">This service uses Microsoft-patented technology to allow applications to detect the language in which specific text is written.</span></span>

## <a name="input-to-microsoft-language-detection"></a><span data-ttu-id="783de-107">Входные данные в Microsoft распознавание языка</span><span class="sxs-lookup"><span data-stu-id="783de-107">Input to Microsoft Language Detection</span></span>

<span data-ttu-id="783de-108">Входными данными для службы Microsoft распознавание языка является текст UTF-16 (Нормализованная форма C).</span><span class="sxs-lookup"><span data-stu-id="783de-108">The input to the Microsoft Language Detection service is UTF-16 (normalized form C) text.</span></span> <span data-ttu-id="783de-109">Служба должна определить язык для этого текста.</span><span class="sxs-lookup"><span data-stu-id="783de-109">The service has to determine the language for this text.</span></span>

## <a name="output-of-microsoft-language-detection"></a><span data-ttu-id="783de-110">Выходные данные Microsoft распознавание языка</span><span class="sxs-lookup"><span data-stu-id="783de-110">Output of Microsoft Language Detection</span></span>

<span data-ttu-id="783de-111">Служба Microsoft распознавание языка извлекает строки в формате UTF-16 с двойным нулем, которые представлены с помощью имен, разделенных символами NULL.</span><span class="sxs-lookup"><span data-stu-id="783de-111">The Microsoft Language Detection service retrieves a double-null-terminated, registry-formatted UTF-16 string listing languages, represented by their names, separated by null character delimiters.</span></span> <span data-ttu-id="783de-112">Список сортируется по релевантности.</span><span class="sxs-lookup"><span data-stu-id="783de-112">The list is sorted by relevance.</span></span> <span data-ttu-id="783de-113">Для большинства языков используются нейтральные имена.</span><span class="sxs-lookup"><span data-stu-id="783de-113">For most languages, neutral names are used.</span></span> <span data-ttu-id="783de-114">Однако для некоторых, например, SR-Цирл, SR-ЛАТН, zh-Hant и zh-Ханс, используются полные имена.</span><span class="sxs-lookup"><span data-stu-id="783de-114">However, for some, for example, sr-Cyrl, sr-Latn, zh-Hant, and zh-Hans, full names are used.</span></span>

## <a name="microsoft-language-detection-operation"></a><span data-ttu-id="783de-115">Операция Microsoft распознавание языка</span><span class="sxs-lookup"><span data-stu-id="783de-115">Microsoft Language Detection Operation</span></span>

<span data-ttu-id="783de-116">Служба Microsoft распознавание языка проверяет скрипт Юникода текста, предоставленного приложением.</span><span class="sxs-lookup"><span data-stu-id="783de-116">The Microsoft Language Detection service checks the Unicode script of the text provided by the application.</span></span> <span data-ttu-id="783de-117">Он разделяет текст на основе обнаруженных им скриптов, а затем определяет язык, на котором записан каждый сегмент.</span><span class="sxs-lookup"><span data-stu-id="783de-117">It segments the text based on the scripts that it detects, and then determines the language in which each segment is written.</span></span> <span data-ttu-id="783de-118">Если сценарий указывает на один язык, этот язык будет гарантированно представлен в списке выходных данных языков.</span><span class="sxs-lookup"><span data-stu-id="783de-118">If a script indicates a single language, the language is guaranteed to be present in the output list of languages.</span></span> <span data-ttu-id="783de-119">Служба использует запатентованный алгоритм для определения релевантности каждого поддерживаемого языка.</span><span class="sxs-lookup"><span data-stu-id="783de-119">The service uses a patented algorithm to determine the relevance of each supported language.</span></span>

## <a name="microsoft-language-detection-guid"></a><span data-ttu-id="783de-120">Идентификатор GUID распознавание языка Microsoft</span><span class="sxs-lookup"><span data-stu-id="783de-120">Microsoft Language Detection GUID</span></span>

<span data-ttu-id="783de-121">Идентификатор GUID для службы Microsoft распознавание языка объявляется в Елссрвк. h, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="783de-121">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a><span data-ttu-id="783de-122">См. также</span><span class="sxs-lookup"><span data-stu-id="783de-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="783de-123">О расширенных лингвистических службах</span><span class="sxs-lookup"><span data-stu-id="783de-123">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



