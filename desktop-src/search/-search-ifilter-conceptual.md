---
description: Microsoft Windows Search использует фильтры для извлечения содержимого элементов, включаемых в полнотекстовый индекс.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Разработка обработчиков фильтров для поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072647"
---
# <a name="developing-filter-handlers-for-windows-search"></a>Разработка обработчиков фильтров для поиска Windows

Microsoft Windows Search использует фильтры для извлечения содержимого элементов, включаемых в полнотекстовый индекс. Можно расширить поиск Windows для индексации новых или собственных типов файлов, написав фильтры для извлечения содержимого и обработчики свойств для извлечения свойств файлов.

В этом разделе представлена концептуальная платформа, необходимая для реализации обработчика фильтра (реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).

- [Основные сведения о обработчиках фильтров в поиске Windows](-search-ifilter-about.md)
- [Рекомендации по созданию обработчиков фильтров в поиске Windows](-search-3x-wds-extidx-filters.md)
- [Возвращение свойств из обработчика фильтра](-search-ifilter-property-filtering.md)
- [Обработчики фильтров, поставляемые с Windows](-search-ifilter-implementations.md)
- [Реализация обработчиков фильтров в поиске Windows](-search-ifilter-constructing-filters.md)
- [Регистрация обработчиков фильтров](-search-ifilter-registering-filters.md)
- [Тестирование обработчиков фильтров](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Дополнительные ресурсы

- Пример кода [ифилтерсампле](-search-sample-ifiltersample.md) , доступный на [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), демонстрирует создание базового класса IFilter для реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).
- Общие сведения о типах файлов см. в разделе [типы файлов](../shell/fa-file-types.md).
- Сведения о запросе атрибутов сопоставления файлов для типа файлов см. в разделе [перцеиведтипес, системфилеассоЦиатионс и регистрация приложения](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
