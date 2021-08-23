---
title: Текстовые модули для автоматизации пользовательского интерфейса
description: В этом разделе описываются единицы текста, поддерживаемые автоматизацией пользовательского интерфейса Майкрософт \ 32; Шаблон элемента управления TextRange. Поставщики и клиенты автоматизации пользовательского интерфейса используют текстовые единицы для указания величины перемещения или изменения размера текстового диапазона.
ms.assetid: 3ec43a81-c4f1-4c73-865f-a60c751fc3fb
keywords:
- Автоматизация пользовательского интерфейса, единицы измерения текста
- единицы текста, сведения
- Модель автоматизации пользовательского интерфейса, список единиц текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5c40604f3c524c1e9f3bcdb36458e099563eb7279fa61133dcfa7ea3fde90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118824167"
---
# <a name="ui-automation-text-units"></a>Единицы текста модели автоматизации пользовательского интерфейса

В этом разделе описываются единицы текста, поддерживаемые шаблоном элемента управления Microsoft UI Automation [TextRange](uiauto-implementingtextandtextrange.md) . Поставщики и клиенты автоматизации пользовательского интерфейса используют текстовые единицы для указания величины перемещения или изменения размера текстового диапазона.

-   [Элементы API единиц текста](#text-unit-api-elements)
-   [Описания единиц текста](#text-unit-descriptions)
    -   [Символ](#character)
    -   [Формат](#format)
    -   [Word](#word)
    -   [Линия](#line)
    -   [Paragraph](#paragraph)
    -   [Страница](#page)
    -   [Document](#document)
-   [Другие возможные диапазоны](#other-potential-ranges)
-   [Связанные темы](#related-topics)

## <a name="text-unit-api-elements"></a>Элементы API единиц текста

API автоматизации пользовательского интерфейса содержит следующие методы, для которых требуется указать единицу текста:

-   [**Итекстранжепровидер:: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)
-   [**Итекстранжепровидер:: Експандтоенклосингунит**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)
-   [**Итекстранжепровидер:: Мовиндпоинтбюнит**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)
-   [**Иуиаутоматионтекстранже:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)
-   [**Иуиаутоматионтекстранже:: Експандтоенклосингунит**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)
-   [**Иуиаутоматионтекстранже:: Мовиндпоинтбюнит**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)

Перечисление [**текстунит**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) определяет единицы текста, поддерживаемые диапазонами текста модели автоматизации пользовательского интерфейса. Чтобы указать единицу текста, член перечисления [**текстунит**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) указывается в вызове метода [**итекстранжепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) или [**иуиаутоматионтекстранже**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) . Ниже приведены текстовые единицы измерения от наименьшего до большего.

-   [**Текстунит \_ символ**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Формат текстунит**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Текстунит \_ слово**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Текстунит \_ строка**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Текстунит \_ абзац**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Страница текстунит**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Документ текстунит**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

Если конкретный текстовый элемент управления не поддерживает указанную единицу текста, поставщик должен ответить, подставив следующую единицу измерения большего размера, которая поддерживается элементом управления. Например, если [**текстунит \_ абзац**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) указан, но не поддерживается, метод может заменить [**Текстунит \_ страницу**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) или [**\_ документ текстунит**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit).

Лингвистические характеристики исходного текста могут усложнить поставщика определить границы текста на основе указанной единицы текста. Для получения справки по определению границ текста поставщик может использовать функции API Uniscribe, такие как [**скриптбреак**](/windows/desktop/api/usp10/nf-usp10-scriptbreak). Дополнительные сведения см. в разделе о [Uniscribe](/windows/desktop/Intl/uniscribe) на веб-сайте MSDN.

## <a name="endpoint-inclusivity"></a>Инклусивити конечной точки

Конечная точка текстового блока может служить как [начальной](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) конечной точкой, так и [конечной](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) конечной точкой для смежных диапазонов текста того же типа. Если конец одной единицы текста также является началом другой единицы текста, диапазон, содержащий [конечную](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) точку, не использует атрибуты или объекты соседнего диапазона, содержащего [начальную](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) конечную точку.

Например, текстовый поток "Hello **World**" содержит две единицы слова с различными атрибутами насыщенности шрифта (обычный и полужирный). В этом случае [Конечная](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) точка слова «Привет» и [Начальная](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) конечная точка слова «**World**» одинаковы, что приводит к следующему результату:

- Диапазон "Hello" не использует атрибут полужирного начертания слова "World" и не возвращает значения атрибута mixed для текстового атрибута "насыщенность шрифта".
- Диапазон «**World**» имеет один и тот же вес шрифта (полужирный) и не использует насыщенность шрифта предшествующей единицы слова «Hello».

Вот еще один пример, когда текстовый поток содержит две единицы слов, одна из которых является ссылкой: `[Foo]() Bar` . В этом случае [Конечная](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) точка в слове `[Foo]()` и [Начальная](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) конечная точка слова «Bar» одинаковы, что приводит к следующему результату:

- Ссылка относится к текстовому диапазону, содержащему "foo".
- Ссылка является дочерней по отношению к текстовому диапазону "foo" и заключена в [итекстпровидер](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).
- Текстовый диапазон не имеет дочерних элементов и заключен в [итекстпровидер](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).

**Дополнительные примечания:**

> Вырожденный (пустой) диапазон на границе единицы текста с текстовым диапазоном того же типа предполагает свойства непосредственно примыкающей единицы текста.
>
> Вызов [иуиаутоматионтекстранже:: експандтоенклосингунит](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit
) для вырожденного диапазона на границе единицы текста с текстовым диапазоном того же типа разворачивает вырожденный диапазон до следующей единицы текста.

## <a name="text-unit-descriptions"></a>Описания единиц текста

В этом разделе описываются все текстовые единицы, поддерживаемые автоматизацией пользовательского интерфейса.

### <a name="character"></a>Знак

[**Текстунит \_ Символ**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) — это лингвистическая единица текста, представляющая один символ. Лингвистическое определение символа зависит от языка. Для английского языка (США) символ обычно размещается с помощью пробела или другого символа, например знака пунктуации, числа или буквы.

Управляющие символы, такие как возврат каретки и знак Юникода слева направо (LTM), не должны рассматриваться как символы, но могут включаться в текстовый диапазон, нормализованный на основе единицы символьного текста.

Знаки пунктуации и символы разрыва слов, такие как пробелы, следует рассматривать как символы.

### <a name="format"></a>Формат

[**Текстунит \_ Формат**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) используется для размещения границы текстового диапазона на основе атрибутов форматирования текста. Например, если текстовый диапазон в данный момент располагается на одном символе слова, то при указании **\_ формата текстунит** в вызове [**иуиаутоматионтекстранже:: експандтоенклосингунит**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) расширяется текстовый диапазон, чтобы он включал весь текст с одинаковыми атрибутами, равными одному символу. Результирующий диапазон текста может содержать или не включать слово целиком. Кроме того, использование единицы форматирования текста не расширяет диапазон текста по границе внедренного объекта, такого как изображение или гиперссылка.

В отличие от других единиц текста, в том числе тех единиц текста, которые меньше, чем сами по себе, [**\_ Формат текстунит**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) может быть меньше или больше, чем другие единицы. Например, если весь документ использует одни и те же атрибуты текста и не содержит внедренные объекты, расширение текстового диапазона по **\_ формату текстунит** создаст новый диапазон, охватывающий весь документ, а при расширении текстового диапазона на [**текстунит \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) создаст меньший диапазон.

### <a name="word"></a>Word

[**Текстунит \_ Слово**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) — это лингвистическая единица текста, представляющая одно целое слово. Лингвистическое определение слова зависит от языка. Для английского языка (США) слова обычно разделяются пробелами или знаками препинания.

Если для установки границы текстового диапазона используется [**текстунит \_ слово**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) , результирующий диапазон текста должен содержать символы разрыва слов, которые находятся в конце слова, но перед началом следующего слова.

### <a name="line"></a>Линия

[**Текстунит \_ Line**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) — это единица текста, представляющая одну строку текста, представленную в окне просмотра элемента управления. При использовании **\_ линии текстунит** для установки границы текстового диапазона поставщик должен задать границу сразу после точки, где управляющий символ разрывает линию, или когда окно просмотра элемента управления заключает текст в новую строку. Граница должна быть установлена, где начинается новая строка.

### <a name="paragraph"></a>Paragraph

[**Текстунит \_ Абзац**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) — это лингвистическая единица текста, представляющая полный абзац. Абзац должен начинаться непосредственно перед первым символом абзаца и обычно заканчиваться сразу после последнего символа. Все пустые строки, следующие за абзацем, должны быть объединены в абзац, если в источнике текста не указано иное. Как правило, конечная граница абзаца также отмечает конечную границу единицы текста [**текстунит \_ строки**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) .

### <a name="page"></a>Страница

[**Текстунит \_ Страница**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) представляет полную текстовую страницу документа. Границы страницы должны быть установлены в тех местах, где начинается и заканчивается страница.

### <a name="document"></a>Документ

[**Текстунит \_ Документ**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) представляет все содержимое документа, поддерживаемое шаблоном элемента управления [Text](uiauto-implementingtextandtextrange.md) . Текст не должен существовать за пределами текстового диапазона, содержащего документ. Любые объекты, которые вставляются в документ, например заметки заметки, пересекающие границу страницы, должны рассматриваться как внедренные объекты документа, а не как часть текстового содержимого документа.

## <a name="other-potential-ranges"></a>Другие возможные диапазоны

Текущая спецификация шаблона элемента управления [TextRange](uiauto-implementingtextandtextrange.md) не допускает добавление новых значений текстовых единиц в перечисление [**текстунит**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) и не позволяет переопределять существующие значения единиц текста. Чтобы предоставить доступ к другим потенциальным диапазонам, таким как заголовки и заметки, поставщик должен предоставить эти диапазоны как внедренные объекты с соответствующим текстовым диапазоном. Таким образом, можно также добавить поддержку соответствующих шаблонов элементов управления. Это решение является более гибким и расширяемым, чем определение новых единиц текста.

## <a name="related-topics"></a>Связанные темы

### <a name="reference"></a>Справочник

[текстпаттернранжеендпоинт](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

[Итекстранжепровидер:: дочерние элементы](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren)





### <a name="conceptual"></a>Основные понятия

[Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого](uiauto-ui-automation-textpattern-overview.md)

[Работа с элементами управления на основе текста](uiauto-workingwithtextbasedcontrols.md)