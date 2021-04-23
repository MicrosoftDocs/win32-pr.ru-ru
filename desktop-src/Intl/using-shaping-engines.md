---
description: Uniscribe использует несколько механизмов формирования, которые содержат сведения о макете для определенных скриптов.
ms.assetid: 3cdd18f3-51d3-4d1c-be31-f5709074cbe7
title: Использование механизмов формирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a106e993aba515af38edd2b809ef60454a186cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651200"
---
# <a name="using-shaping-engines"></a><span data-ttu-id="764e3-103">Использование механизмов формирования</span><span class="sxs-lookup"><span data-stu-id="764e3-103">Using Shaping Engines</span></span>

<span data-ttu-id="764e3-104">Uniscribe использует несколько механизмов формирования, которые содержат сведения о макете для определенных скриптов.</span><span class="sxs-lookup"><span data-stu-id="764e3-104">Uniscribe uses multiple shaping engines that contain the layout knowledge for particular scripts.</span></span> <span data-ttu-id="764e3-105">Он также использует преимущества механизма формирования макета OpenType для обработки функций сценариев, связанных со шрифтами, таких как создание глифов, измерение экстентов и поддержка разбиения по словам.</span><span class="sxs-lookup"><span data-stu-id="764e3-105">It also takes advantage of the OpenType layout shaping engine for handling font-specific script features, such as glyph generation, extent measurement, and word-breaking support.</span></span> <span data-ttu-id="764e3-106">Uniscribe управляет двунаправленным изменением порядка символов с помощью двунаправленного алгоритма Юникода и распознает форматы шрифтов, отличные от OpenType, для написания арабского, иврита и тайского языков.</span><span class="sxs-lookup"><span data-stu-id="764e3-106">Uniscribe manages bidirectional character reordering using the Unicode bidirectional algorithm, and understands non-OpenType layout font formats for Arabic, Hebrew, and Thai shaping.</span></span>

<span data-ttu-id="764e3-107">Поскольку диапазоны кодовых точек, назначенных каждому механизму формирования, могут различаться, Номера скриптов не публикуются, за исключением того, что скрипт не \_ определен.</span><span class="sxs-lookup"><span data-stu-id="764e3-107">Since the exact code point ranges assigned to each shaping engine might vary, script numbers are not published, with the exception of SCRIPT\_UNDEFINED.</span></span> <span data-ttu-id="764e3-108">Однако приложение может проверить атрибуты скриптов, вызвав функцию [**скриптжетпропертиес**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) , которая обращается к таблице свойств глобального скрипта.</span><span class="sxs-lookup"><span data-stu-id="764e3-108">However, your application can test the attributes of scripts by calling the [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) function, which accesses the global script properties table.</span></span> <span data-ttu-id="764e3-109">Приложение может использовать глобальные свойства скрипта для объединения собственных правил макета с требуемыми делениями механизма формирования.</span><span class="sxs-lookup"><span data-stu-id="764e3-109">The application can use the global script properties to help combine its own layout rules with the required shaping engine divisions.</span></span>

<span data-ttu-id="764e3-110">Приложение обращается к механизму формирования, вызвав функцию [**скриптшапе**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) .</span><span class="sxs-lookup"><span data-stu-id="764e3-110">The application accesses a shaping engine with a call to the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) function.</span></span> <span data-ttu-id="764e3-111">Все сложные механизмы формирования скриптов, механизмы формирования цифр и модули формирования ASCII перед формированием проверяют шрифт, указанный в дескрипторе контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="764e3-111">All the complex script shaping engines, the digit shaping engines, and the ASCII shaping engines validate the font indicated in the device context handle before shaping.</span></span> <span data-ttu-id="764e3-112">Для удобочитаемости сложные скрипты должны быть написаны с помощью сценария, возвращаемого функцией [**скриптитемизе**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) .</span><span class="sxs-lookup"><span data-stu-id="764e3-112">Complex scripts must be shaped using the script returned by the [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) function in order to be legible.</span></span> <span data-ttu-id="764e3-113">Другие запуски остаются в неопределенном виде, если написание скрипта не \_ определено в элементе **ескрипт** структуры [**\_ анализа скриптов**](/windows/win32/api/usp10/ns-usp10-script_analysis) , хотя они могут потерять типографское качество.</span><span class="sxs-lookup"><span data-stu-id="764e3-113">Other runs remain legible if shaped with SCRIPT\_UNDEFINED specified in the **eScript** member of the [**SCRIPT\_ANALYSIS**](/windows/win32/api/usp10/ns-usp10-script_analysis) structure, although they might lose typographic quality.</span></span>

<span data-ttu-id="764e3-114">[**Скриптшапе**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) возвращает 0 в случае успешного выполнения или \_ USP \_ E \_ \_ в \_ шрифте, если шрифт, предоставленный приложением, не содержит достаточное количество глифов или таблиц формирования.</span><span class="sxs-lookup"><span data-stu-id="764e3-114">[**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) returns 0 if successful, or USP\_E\_SCRIPT\_NOT\_IN\_FONT if the font supplied by the application does not contain sufficient glyphs or shaping tables.</span></span> <span data-ttu-id="764e3-115">Если в приложении указан \_ неопределенный сценарий и некоторые символы не поддерживаются шрифтом, функция все равно будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="764e3-115">If the application specifies SCRIPT\_UNDEFINED and some characters are not supported by the font, the function still succeeds.</span></span> <span data-ttu-id="764e3-116">В этом случае приложение должно проверять выходной буфер глифов на наличие отсутствующих глифов.</span><span class="sxs-lookup"><span data-stu-id="764e3-116">In this case, the application should scan the glyph output buffer for the presence of missing glyphs.</span></span> <span data-ttu-id="764e3-117">Рекомендации по обработке отсутствующих глифов см. в разделе [Использование отката шрифта](using-font-fallback.md).</span><span class="sxs-lookup"><span data-stu-id="764e3-117">For strategies to deal with missing glyphs, see [Using Font Fallback](using-font-fallback.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="764e3-118">См. также</span><span class="sxs-lookup"><span data-stu-id="764e3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="764e3-119">Использование Uniscribe</span><span class="sxs-lookup"><span data-stu-id="764e3-119">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



