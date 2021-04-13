---
description: Для разделения обычного текста в приложениях следует использовать символ разделителя строки (0x2028) и символ разделителя абзаца (0x2029). Новая строка начинается после каждого разделителя в виде линии. Новый абзац начинается после каждого разделителя абзаца.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Использование разделителей строк и абзацев
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9511ba2a8889b3c9139daf1d088d91ed746db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272954"
---
# <a name="using-line-and-paragraph-separators"></a><span data-ttu-id="54b56-105">Использование разделителей строк и абзацев</span><span class="sxs-lookup"><span data-stu-id="54b56-105">Using Line and Paragraph Separators</span></span>

<span data-ttu-id="54b56-106">Для разделения обычного текста в приложениях следует использовать символ разделителя строки (0x2028) и символ разделителя абзаца (0x2029).</span><span class="sxs-lookup"><span data-stu-id="54b56-106">Your applications should use the line separator character (0x2028) and the paragraph separator character (0x2029) to divide plain text.</span></span> <span data-ttu-id="54b56-107">Новая строка начинается после каждого разделителя в виде линии.</span><span class="sxs-lookup"><span data-stu-id="54b56-107">A new line is begun after each line separator.</span></span> <span data-ttu-id="54b56-108">Новый абзац начинается после каждого разделителя абзаца.</span><span class="sxs-lookup"><span data-stu-id="54b56-108">A new paragraph is begun after each paragraph separator.</span></span>

<span data-ttu-id="54b56-109">Не обязательно начинать первую строку или абзац в файле с этими символами или заканчивать их последней строкой или абзацем.</span><span class="sxs-lookup"><span data-stu-id="54b56-109">It is not necessary to start the first line or paragraph in a file with these characters, or to end the last line or paragraph with them.</span></span> <span data-ttu-id="54b56-110">Это означает, что в этом расположении есть пустая строка или абзац.</span><span class="sxs-lookup"><span data-stu-id="54b56-110">Doing so indicates that there is an empty line or paragraph in that location.</span></span>

<span data-ttu-id="54b56-111">Приложение может использовать разделитель строк для обозначения безусловного конца строки.</span><span class="sxs-lookup"><span data-stu-id="54b56-111">The application can use the line separator to indicate an unconditional end of line.</span></span> <span data-ttu-id="54b56-112">Однако разделители в виде линии не соответствуют отдельным символам возврата каретки и перевода строки или сочетанию этих символов.</span><span class="sxs-lookup"><span data-stu-id="54b56-112">However, line separators do not correspond to the separate carriage return and linefeed characters, or to a combination of these characters.</span></span> <span data-ttu-id="54b56-113">Разделители в виде линии следует обрабатывать отдельно от символов возврата каретки и перевода строки.</span><span class="sxs-lookup"><span data-stu-id="54b56-113">Line separators must be processed separately from carriage return and linefeed characters.</span></span>

<span data-ttu-id="54b56-114">Приложение может вставлять разделитель абзацев между абзацами текста.</span><span class="sxs-lookup"><span data-stu-id="54b56-114">The application can insert a paragraph separator between paragraphs of text.</span></span> <span data-ttu-id="54b56-115">Использование этого разделителя разрешит создание файлов обычного текста, которые можно форматировать с помощью области строки в различных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="54b56-115">Use of this separator allows creation of plain text files that can be formatted with different line widths on different operating systems.</span></span> <span data-ttu-id="54b56-116">Целевая система может игнорировать разделители в виде линии и разделить абзацы только в разделителях абзаца.</span><span class="sxs-lookup"><span data-stu-id="54b56-116">The target system can ignore any line separators and break paragraphs only at the paragraph separators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54b56-117">См. также</span><span class="sxs-lookup"><span data-stu-id="54b56-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54b56-118">Использование специальных символов в Юникоде</span><span class="sxs-lookup"><span data-stu-id="54b56-118">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



