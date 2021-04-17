---
title: Основные сведения о проблемах производительности
description: В этом разделе описываются проблемы производительности, связанные с использованием шаблонов элементов управления Text и TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- Клиенты, основные сведения о проблемах производительности
- Клиенты, текстовые элементы управления
- Клиенты, текстовые диапазоны
- Клиенты, шаблон элемента управления Text
- Клиенты, шаблон элемента управления TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339725"
---
# <a name="understanding-performance-issues"></a><span data-ttu-id="dc53a-108">Основные сведения о проблемах производительности</span><span class="sxs-lookup"><span data-stu-id="dc53a-108">Understanding Performance Issues</span></span>

<span data-ttu-id="dc53a-109">В этом разделе описываются проблемы производительности, связанные с использованием шаблонов элементов управления [Text и TextRange](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="dc53a-109">This topic describes performance issues associated with using the [Text and TextRange](uiauto-implementingtextandtextrange.md) control patterns.</span></span>


<span data-ttu-id="dc53a-110">Интерфейсы [**иуиаутоматионтекстпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) и [**иуиаутоматионтекстранже**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) основываются на межпроцессных вызовах — они не предоставляют механизм кэширования для повышения производительности при извлечении или обработке текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="dc53a-110">The [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) interfaces rely on cross-process calls—they do not provide a caching mechanism to improve performance when retrieving or processing textual content.</span></span>

<span data-ttu-id="dc53a-111">Клиентское приложение может повысить производительность с помощью метода [**иуиаутоматионтекстранже:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) для получения блоков текста с умеренным размером.</span><span class="sxs-lookup"><span data-stu-id="dc53a-111">A client application can improve performance by using the [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) method to retrieve moderately sized blocks of text.</span></span> <span data-ttu-id="dc53a-112">Например, использование **gettext** для извлечения одиночных символов приведет к снижению производительности между процессами для каждого символа, в то время как не задавая максимальную длину при вызове **gettext** , и может иметь высокую задержку в зависимости от размера текстового диапазона.</span><span class="sxs-lookup"><span data-stu-id="dc53a-112">For example, using **GetText** to retrieve single characters will incur a cross-process performance hit for each character, whereas not specifying a maximum length when calling **GetText** will incur one cross-process hit, but can have high latency depending on the size of the text range.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc53a-113">См. также</span><span class="sxs-lookup"><span data-stu-id="dc53a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc53a-114">Шаблоны элементов управления Text и TextRange</span><span class="sxs-lookup"><span data-stu-id="dc53a-114">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="dc53a-115">Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого</span><span class="sxs-lookup"><span data-stu-id="dc53a-115">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="dc53a-116">Работа с элементами управления на основе текста</span><span class="sxs-lookup"><span data-stu-id="dc53a-116">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




