---
title: Каноническая XML
description: Канонический XML решает проблему преобразования набора узлов XML в байты таким образом, что тривиальные изменения в XML (например, изменение порядка атрибутов в элементе) не изменяют итоговую форму Byte.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Веб-службы канонического XML для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db77e449c4e3d6ee5f6e2cb474c84a6b1161a4fee87c35d01d278882b178cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082988"
---
# <a name="xml-canonicalization"></a>Каноническая XML

Канонический XML решает проблему преобразования набора узлов XML в байты таким образом, что тривиальные изменения в XML (например, изменение порядка атрибутов в элементе) не изменяют итоговую форму Byte. Байты, полученные из канонической разбора, обычно используются для создания криптографической подписи поверх XML-содержимого.


Часто используемые алгоритмы канонизации XML стандартизируют следующие аспекты:

-   Кодировка символов (UTF-8 без преамбулы)
-   Символы перевода строки и другие формы символов
-   Порядок атрибутов в элементе
-   Форма пустого элемента
-   Подготовка к просмотру объявлений пространств имен

API-интерфейсы [**всстартреадерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) и [**всендреадерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) предоставляют функцию канонизации XML при чтении документа.

API-интерфейсы [**всстартвритерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) и [**всендвритерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) предоставляют функцию канонизации XML при записи документа.

Для канонизации используются следующие перечисления.

-   [**\_ \_ алгоритм КАНОНИЗАЦИИ XML WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**\_ \_ \_ идентификатор свойства WS-канонизации \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

Для канонизации используются следующие функции.

-   [**всендреадерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**всендвритерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**всстартреадерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**всстартвритерканоникализатион**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

Для канонизации используются следующие структуры:

-   [**\_ \_ \_ Инклюзивные \_ префиксы WS-XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**\_свойство WS-XML \_ канонизации \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




