---
description: Сложный скрипт — это скрипт, для которого элемент Фкомплекс свойств СКРИПТа \_ имеет значение true. В этом разделе описываются свойства, которые может иметь сложный скрипт.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: О сложных скриптах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081073"
---
# <a name="about-complex-scripts"></a><span data-ttu-id="8c54a-104">О сложных скриптах</span><span class="sxs-lookup"><span data-stu-id="8c54a-104">About Complex Scripts</span></span>

<span data-ttu-id="8c54a-105">[Сложный скрипт](uniscribe-glossary.md) — это скрипт, для которого элемент **фкомплекс** [**\_ свойств скрипта**](/windows/desktop/api/Usp10/ns-usp10-script_properties) имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="8c54a-105">A [complex script](uniscribe-glossary.md) is a script for which the **fComplex** member of [**SCRIPT\_PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) is set to **TRUE**.</span></span> <span data-ttu-id="8c54a-106">В этом разделе описываются свойства, которые может иметь сложный скрипт.</span><span class="sxs-lookup"><span data-stu-id="8c54a-106">This topic details the properties that a complex script might have.</span></span>

## <a name="bidirectional-rendering"></a><span data-ttu-id="8c54a-107">Двунаправленная отрисовка</span><span class="sxs-lookup"><span data-stu-id="8c54a-107">Bidirectional Rendering</span></span>

<span data-ttu-id="8c54a-108">Двунаправленная визуализация — это обработка текста, который считывает как слева направо, так и справа налево.</span><span class="sxs-lookup"><span data-stu-id="8c54a-108">Bidirectional rendering is handling of text that reads both left-to-right and right-to-left.</span></span> <span data-ttu-id="8c54a-109">Например, в двунаправленной отрисовке для текста по умолчанию используется направление чтения справа налево, но для некоторых чисел оно слева направо.</span><span class="sxs-lookup"><span data-stu-id="8c54a-109">For example, in the bidirectional rendering of Arabic, the default reading direction for text is right-to-left, but it is left-to-right for some numbers.</span></span> <span data-ttu-id="8c54a-110">Обработка сложного сценария должна учитывать разницу между логическим порядком (нажатием клавиши) и визуальным порядком глифов.</span><span class="sxs-lookup"><span data-stu-id="8c54a-110">Processing a complex script must account for the difference between the logical (keystroke) order and the visual order of the glyphs.</span></span> <span data-ttu-id="8c54a-111">Кроме того, обработка должна правильно работать с перемещением курсора и проверкой попадания.</span><span class="sxs-lookup"><span data-stu-id="8c54a-111">In addition, processing must properly deal with caret movement and hit testing.</span></span> <span data-ttu-id="8c54a-112">Для сопоставления между положением экрана и индексом символов необходимо понимать алгоритмы макета для конкретного отображения, например, выбор текста или курсора.</span><span class="sxs-lookup"><span data-stu-id="8c54a-112">The mapping between screen position and a character index requires an understanding of the layout algorithms for the particular display, for example, selection of text or caret display.</span></span>

## <a name="contextual-shaping"></a><span data-ttu-id="8c54a-113">Контекстуальное формирование</span><span class="sxs-lookup"><span data-stu-id="8c54a-113">Contextual Shaping</span></span>

<span data-ttu-id="8c54a-114">В контекстном режиме форма символов изменяется в зависимости от символов, которые их окружают.</span><span class="sxs-lookup"><span data-stu-id="8c54a-114">In contextual shaping, script characters change shape depending on the characters that surround them.</span></span> <span data-ttu-id="8c54a-115">Такая обработка происходит в письменном письме на английском языке, когда форма «l» изменяется в нижнем регистре, в зависимости от предшествующего ей символа, например «a» (подключается к «l») или «o» (высокое соединение).</span><span class="sxs-lookup"><span data-stu-id="8c54a-115">Such shaping occurs in English cursive writing when a lowercase "l" changes shape depending on the character that precedes it, such as an "a" (connects low to the "l") or an "o" (connects high).</span></span> <span data-ttu-id="8c54a-116">Например, арабский является сценарием, который представляет собой контекстную форму.</span><span class="sxs-lookup"><span data-stu-id="8c54a-116">For example, Arabic is a script that exhibits contextual shaping.</span></span>

## <a name="combining-characters"></a><span data-ttu-id="8c54a-117">Объединение символов</span><span class="sxs-lookup"><span data-stu-id="8c54a-117">Combining Characters</span></span>

<span data-ttu-id="8c54a-118">Сочетание символов, называемое также "лигатурами", — это символы, которые объединяются в один символ при их совместном помещении.</span><span class="sxs-lookup"><span data-stu-id="8c54a-118">Combining characters, also called "ligatures," are characters that join into one character when placed together.</span></span> <span data-ttu-id="8c54a-119">Арабский — это сценарий, имеющий множество присоединяемых символов.</span><span class="sxs-lookup"><span data-stu-id="8c54a-119">Arabic is a script that has many combining characters.</span></span> <span data-ttu-id="8c54a-120">Одним из примеров использования Объединенных символов является «a», за которым следует «комбинированный грависом», для которого визуализированное представление — «продажам».</span><span class="sxs-lookup"><span data-stu-id="8c54a-120">One example of the use of combining characters is the "a" followed by "combining grave", for which the rendered representation is "à".</span></span> <span data-ttu-id="8c54a-121">Поток Юникода "U + 0061 U + 0300" требует некоторой обработки, чтобы убедиться, что "комбинированный грависом" правильно расположен над "a".</span><span class="sxs-lookup"><span data-stu-id="8c54a-121">The Unicode stream "U+0061 U+0300" requires some processing to make sure the "combining grave" is correctly positioned above the "a".</span></span>

## <a name="specialized-word-break-and-justification"></a><span data-ttu-id="8c54a-122">Специальное разбиение и обоснование слов</span><span class="sxs-lookup"><span data-stu-id="8c54a-122">Specialized Word Break and Justification</span></span>

<span data-ttu-id="8c54a-123">Некоторые сценарии, например тайский, имеют сложные правила разделения слов между строками или выравнивания текста в строке.</span><span class="sxs-lookup"><span data-stu-id="8c54a-123">Some scripts, for example, Thai, have complex rules for dividing words between lines or justifying text on a line.</span></span>

## <a name="filtering-for-illegal-character-combinations"></a><span data-ttu-id="8c54a-124">Фильтрация недопустимых сочетаний символов</span><span class="sxs-lookup"><span data-stu-id="8c54a-124">Filtering for Illegal Character Combinations</span></span>

<span data-ttu-id="8c54a-125">Сложный сценарий, например тайский, может отфильтровывать недопустимые сочетания символов, если язык не допускает определенных сочетаний символов.</span><span class="sxs-lookup"><span data-stu-id="8c54a-125">A complex script, for example, Thai, can filter out illegal character combinations when a language does not allow certain character combinations.</span></span>

## <a name="font-fallback"></a><span data-ttu-id="8c54a-126">Откат шрифта</span><span class="sxs-lookup"><span data-stu-id="8c54a-126">Font Fallback</span></span>

<span data-ttu-id="8c54a-127">Откат шрифта — это автоматический выбор шрифта, отличного от шрифта, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="8c54a-127">Font fallback is the automated selection of a font other than the font selected by the user.</span></span> <span data-ttu-id="8c54a-128">В Uniscribe откат шрифта применяется функцией [**скриптстринганалисе**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) , когда весь текст или его часть находится в сценарии, который не поддерживается выбранным пользователем шрифтом.</span><span class="sxs-lookup"><span data-stu-id="8c54a-128">In Uniscribe, font fallback is applied by the [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) function when all or part of the text is in a script that the user-selected font does not support.</span></span> <span data-ttu-id="8c54a-129">Дополнительные сведения см. [в разделе Использование отката шрифта](using-font-fallback.md).</span><span class="sxs-lookup"><span data-stu-id="8c54a-129">For more information, see [Using Font Fallback](using-font-fallback.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c54a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="8c54a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c54a-131">О Uniscribe</span><span class="sxs-lookup"><span data-stu-id="8c54a-131">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



