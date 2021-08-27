---
title: Объект всплывающего окна
description: Объект всплывающего окна
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc2ad1256b040588121dcb92fc8f66fea540b3051b92a6fe5273eb2f81107b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745976"
---
# <a name="the-balloon-object"></a>Объект всплывающего окна

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

Microsoft Agent поддерживает текстовые субтитры метода [**говорите**](speak-method.md) , используя всплывающее слово. Метод [**обработки**](think-method.md) позволяет отображать текст без звука в подсказке "помышления".

Начальное всплывающее окно символа по умолчанию определяется и компилируется в редакторе символов Microsoft Agent. После запуска всплывающие [**окна и свойства**](enabled-property.md) [**шрифтов**](https://www.bing.com/search?q=**Font**) могут быть переопределены пользователем. Если пользователь изменяет свойства всплывающей подсказки слова, он влияет на все символы. В выносках со словами « [**говорите**](speak-method.md) » и « [**думаю**](think-method.md) » для параметра размер используются одинаковые значения свойств. Можно получить доступ к свойствам всплывающей подсказки для символа через объект- [**выноску**](/windows/desktop/lwef/the-balloon-object) , который является дочерним по отношению к [**символьному**](/windows/desktop/lwef/the-characters-object) объекту.

Объект [**всплывающего**](/windows/desktop/lwef/the-balloon-object) объекта поддерживает следующие свойства:

-   [**BackColor**](backcolor-property.md)
-   [**BorderColor**](bordercolor-property.md)
-   [**чарсперлине**](charsperline-property.md)
-   [**Включен**](enabled-property.md)
-   [**фонтчарсет**](fontcharset-property.md)
-   [**FontName**](fontname-property-bal.md)
-   [**FontBold**](fontbold-property.md)
-   [**FontItalic**](fontitalic-property.md)
-   [**FontSize**](fontsize-property-bal.md)
-   [**фонтстрикесру**](fontstrikethru-property.md)
-   [**FontUnderline**](fontunderline-property.md)
-   [**ForeColor**](forecolor-property.md)
-   [**нумберофлинес**](numberoflines-property.md)
-   [**Стиль**](style-property.md)
-   [**Ярлык**](visible-property-bal.md)

 

 