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
ms.openlocfilehash: 24846fea2f35cd9d265ab4f898b60dba2fc4e959b9a0f8bd7baea4661855f0a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861224"
---
# <a name="understanding-performance-issues"></a>Основные сведения о проблемах производительности

В этом разделе описываются проблемы производительности, связанные с использованием шаблонов элементов управления [Text и TextRange](uiauto-implementingtextandtextrange.md) .


Интерфейсы [**иуиаутоматионтекстпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) и [**иуиаутоматионтекстранже**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) основываются на межпроцессных вызовах — они не предоставляют механизм кэширования для повышения производительности при извлечении или обработке текстового содержимого.

Клиентское приложение может повысить производительность с помощью метода [**иуиаутоматионтекстранже:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) для получения блоков текста с умеренным размером. Например, использование **gettext** для извлечения одиночных символов приведет к снижению производительности между процессами для каждого символа, в то время как не задавая максимальную длину при вызове **gettext** , и может иметь высокую задержку в зависимости от размера текстового диапазона.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Шаблоны элементов управления Text и TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Работа с элементами управления на основе текста](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




