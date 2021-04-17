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
# <a name="understanding-performance-issues"></a>Основные сведения о проблемах производительности

В этом разделе описываются проблемы производительности, связанные с использованием шаблонов элементов управления [Text и TextRange](uiauto-implementingtextandtextrange.md) .


Интерфейсы [**иуиаутоматионтекстпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) и [**иуиаутоматионтекстранже**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) основываются на межпроцессных вызовах — они не предоставляют механизм кэширования для повышения производительности при извлечении или обработке текстового содержимого.

Клиентское приложение может повысить производительность с помощью метода [**иуиаутоматионтекстранже:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) для получения блоков текста с умеренным размером. Например, использование **gettext** для извлечения одиночных символов приведет к снижению производительности между процессами для каждого символа, в то время как не задавая максимальную длину при вызове **gettext** , и может иметь высокую задержку в зависимости от размера текстового диапазона.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Шаблоны элементов управления Text и TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Работа с элементами управления на основе текста](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




