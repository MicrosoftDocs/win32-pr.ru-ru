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
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="27687-103">Разработка обработчиков фильтров для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="27687-103">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="27687-104">Microsoft Windows Search использует фильтры для извлечения содержимого элементов, включаемых в полнотекстовый индекс.</span><span class="sxs-lookup"><span data-stu-id="27687-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="27687-105">Можно расширить поиск Windows для индексации новых или собственных типов файлов, написав фильтры для извлечения содержимого и обработчики свойств для извлечения свойств файлов.</span><span class="sxs-lookup"><span data-stu-id="27687-105">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="27687-106">В этом разделе представлена концептуальная платформа, необходимая для реализации обработчика фильтра (реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).</span><span class="sxs-lookup"><span data-stu-id="27687-106">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="27687-107">Основные сведения о обработчиках фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="27687-107">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="27687-108">Рекомендации по созданию обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="27687-108">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="27687-109">Возвращение свойств из обработчика фильтра</span><span class="sxs-lookup"><span data-stu-id="27687-109">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="27687-110">Обработчики фильтров, поставляемые с Windows</span><span class="sxs-lookup"><span data-stu-id="27687-110">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="27687-111">Реализация обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="27687-111">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="27687-112">Регистрация обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="27687-112">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="27687-113">Тестирование обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="27687-113">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="27687-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="27687-114">Additional Resources</span></span>

- <span data-ttu-id="27687-115">Пример кода [ифилтерсампле](-search-sample-ifiltersample.md) , доступный на [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), демонстрирует создание базового класса IFilter для реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="27687-115">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="27687-116">Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="27687-116">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="27687-117">Общие сведения о типах файлов см. в разделе [типы файлов](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="27687-117">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="27687-118">Сведения о запросе атрибутов сопоставления файлов для типа файлов см. в разделе [перцеиведтипес, системфилеассоЦиатионс и регистрация приложения](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="27687-118">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
