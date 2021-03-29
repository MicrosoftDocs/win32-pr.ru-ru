---
title: Обработка результатов поиска
description: После первого вызова IDirectorySearch Жетфирстров или IDirectorySearch GetNextRow, либо ОК, либо \_ \_ \_ все \_ строки, либо возвращается результат ошибки.
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- Обработка результатов поиска
- Active Directory, поиск, обработка результатов поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732128438162f5ee8f6fe75bb4d2ce53e0d43070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "105654283"
---
# <a name="processing-the-search-results"></a>Обработка результатов поиска

После первого вызова [**IDirectorySearch:: жетфирстров**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) или [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow), **s \_ ОК**, **s \_ баннеры \_ \_** не со строки или возвращается результат ошибки.

Если возвращаемое значение равно S, то больше **\_ \_ \_ строк** не найдено ни одного объекта, соответствующего фильтру. Если возвращается результат ошибки, запрос не выполнен. В обоих случаях обработка строк в результате не требуется, так как ничего не было возвращено.

Если возвращается значение **S \_ ОК** , то была получена строка. Столбцы можно анализировать по имени с помощью [**IDirectorySearch:: column**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn). Имя является атрибутом **lDAPDisplayName** атрибута в столбце. Набор всех столбцов был определен параметром Паттрибутенамес метода [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) . Если указано **значение NULL** , набор всех столбцов является объединением всех свойств, найденных для всех возвращаемых объектов. Чтобы считать весь набор столбцов, возвращаемых для объекта, используйте [**IDirectorySearch:: жетнекстколумннаме**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) для итерации каждого столбца и используйте имя столбца, возвращенное для вызова **IDirectorySearch::** GetObject.

Метод [**IDirectorySearch:: DataColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) возвращает структуру [**\_ \_ столбца поиска ADS**](/windows/desktop/api/iads/ns-iads-ads_search_column) , содержащую имя атрибута, тип атрибута, число значений и указатель на массив структур [**адсвалуе**](/windows/desktop/api/iads/ns-iads-adsvalue) , содержащих значения. Структуры **адсвалуе** можно прокручивать, чтобы считать значения для свойства, возвращаемого столбцом. Необходимо прочитать соответствующий элемент структуры **адсвалуе** , основанный на [**адстипе**](/windows/win32/api/iads/ne-iads-adstypeenum) , заданном элементом **двадстипе** структуры **\_ \_ столбцов поиска баннеров** (или членом **двтипе** структуры **адсвалуе** ). Например, если **двадстипе** было **адстипе \_ Integer**, то вы бы читали **целочисленный** элемент каждой структуры **адсвалуе** .

Дополнительные сведения и пример кода см. в разделе [пример кода для поиска пользователей](example-code-for-searching-for-users.md).

 

 