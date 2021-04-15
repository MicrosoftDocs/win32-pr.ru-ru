---
description: Можно расширить поиск Windows, чтобы индексировать содержимое и свойства новых форматов файлов, а также хранилища данных с помощью интерфейсов надстроек данных.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Расширение индекса (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701407"
---
# <a name="extending-the-index-windows-search"></a><span data-ttu-id="8faa7-103">Расширение индекса (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="8faa7-103">Extending the Index (Windows Search)</span></span>

<span data-ttu-id="8faa7-104">Можно расширить поиск Windows, чтобы индексировать содержимое и свойства новых форматов файлов, а также хранилища данных с помощью [интерфейсов надстроек данных](./-search-data-addins-interfaces-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="8faa7-104">You can extend Windows Search to index the contents and properties of new file formats, and data stores using [data add-in interfaces](./-search-data-addins-interfaces-entry-page.md).</span></span> <span data-ttu-id="8faa7-105">Чтобы создать надстройки для поиска Windows, сторонние разработчики должны сначала реализовать хранилище данных оболочки, а затем разработать обработчик протокола, чтобы поиск Windows мог получить доступ к данным для индексирования.</span><span class="sxs-lookup"><span data-stu-id="8faa7-105">To create Windows Search add-ins, third-party developers must first implement a Shell data store, and then develop a protocol handler so that Windows Search can access the data for indexing.</span></span> <span data-ttu-id="8faa7-106">При наличии пользовательского формата файла необходимо разработать обработчик фильтра для индексирования содержимого файла и обработчика свойств для каждого типа файлов в свойствах индекса.</span><span class="sxs-lookup"><span data-stu-id="8faa7-106">If you have a custom file format, you must develop a filter handler to index file contents, and a property handler for every file type to index properties.</span></span>

<span data-ttu-id="8faa7-107">В настоящее время Поиск Windows поддерживает индексирование более чем 200 типов элементов (например, форматы txt, HTML и XML) и может работать с несколькими типами хранилищ данных (например, с файловой системой NTFS и Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="8faa7-107">Windows Search currently supports the indexing of over 200 types of items (such as .txt, .html, and .xml file formats) and can work with multiple types of data stores (such as the NTFS file system and Microsoft Outlook).</span></span> <span data-ttu-id="8faa7-108">В Windows Search используется технология фильтров и обработчиков протоколов, аналогичная серверу SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8faa7-108">Windows Search uses filter and protocol handler technology similar to SharePoint Server.</span></span> <span data-ttu-id="8faa7-109">Таким образом, если у вас уже есть реализации для формата файлов, можно обновить реализации, чтобы инициализировать поток с помощью [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) , чтобы фильтр работал с поиском Windows.</span><span class="sxs-lookup"><span data-stu-id="8faa7-109">Hence, if you already have implementations for your file format, you can update the implementations to be initialized with a stream by using [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) so that the filter will work with Windows Search.</span></span>

> [!Note]  
> <span data-ttu-id="8faa7-110">Обработчики фильтров, обработчики свойств и обработчики протоколов должны быть написаны в машинном коде.</span><span class="sxs-lookup"><span data-stu-id="8faa7-110">Filter handlers, property handlers, and protocol handlers must be written in native code.</span></span> <span data-ttu-id="8faa7-111">Это происходит из-за потенциальных проблем с управлением версиями среды CLR при работе нескольких надстроек.</span><span class="sxs-lookup"><span data-stu-id="8faa7-111">This is due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

 

<span data-ttu-id="8faa7-112">В этом разделе по расширению индекса с помощью надстроек содержатся следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="8faa7-112">This section on extending the index with add-ins contains the following topics:</span></span>

-   [<span data-ttu-id="8faa7-113">Разработка обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="8faa7-113">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
-   [<span data-ttu-id="8faa7-114">Разработка обработчиков свойств для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="8faa7-114">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="8faa7-115">Разработка обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="8faa7-115">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a><span data-ttu-id="8faa7-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8faa7-116">Additional Resources</span></span>

<span data-ttu-id="8faa7-117">Связанные примеры кода см. в разделе [примеры кода для поиска Windows](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="8faa7-117">For related code samples, see [Windows Search Code Samples](-search-samples-ovw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8faa7-118">См. также</span><span class="sxs-lookup"><span data-stu-id="8faa7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8faa7-119">Руководством по разработке для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="8faa7-119">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="8faa7-120">Управление индексом</span><span class="sxs-lookup"><span data-stu-id="8faa7-120">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="8faa7-121">Отправка программных запросов к индексу</span><span class="sxs-lookup"><span data-stu-id="8faa7-121">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="8faa7-122">Расширение языковых ресурсов</span><span class="sxs-lookup"><span data-stu-id="8faa7-122">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
