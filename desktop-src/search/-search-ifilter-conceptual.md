---
description: узнайте, как разрабатывать обработчики фильтров в Windows поиске. Поиск использует фильтры для извлечения элементов, включаемых в полнотекстовый индекс.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: разработка обработчиков фильтров для Windowsного поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cb8fe61ce85c86d0b8397d81303014ed1268bc0aef96b22e7b7bab335b7f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597824"
---
# <a name="developing-filter-handlers-for-windows-search"></a>разработка обработчиков фильтров для Windowsного поиска

Microsoft Windows Search использует фильтры для извлечения содержимого элементов, включаемых в полнотекстовый индекс. можно расширить Windows поиск для индексации новых или собственных типов файлов, записав фильтры для извлечения содержимого и обработчики свойств для извлечения свойств файлов.

В этом разделе представлена концептуальная платформа, необходимая для реализации обработчика фильтра (реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).

- [основные сведения о обработчиках фильтров в Windows поиске](-search-ifilter-about.md)
- [рекомендации по созданию обработчиков фильтров в Windowsном поиске](-search-3x-wds-extidx-filters.md)
- [Возвращение свойств из обработчика фильтра](-search-ifilter-property-filtering.md)
- [Обработчики фильтров, поставляемые с Windows](-search-ifilter-implementations.md)
- [реализация обработчиков фильтров в Windowsном поиске](-search-ifilter-constructing-filters.md)
- [Регистрация обработчиков фильтров](-search-ifilter-registering-filters.md)
- [Тестирование обработчиков фильтров](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Дополнительные ресурсы

- пример кода [ифилтерсампле](-search-sample-ifiltersample.md) , доступный на [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), демонстрирует создание базового класса IFilter для реализации интерфейса [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).
- Общие сведения о типах файлов см. в разделе [типы файлов](../shell/fa-file-types.md).
- Сведения о запросе атрибутов сопоставления файлов для типа файлов см. в разделе [перцеиведтипес, системфилеассоЦиатионс и регистрация приложения](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
