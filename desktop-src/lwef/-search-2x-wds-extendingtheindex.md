---
title: Расширение индекса (устаревшие функции среды Windows)
description: Использование и разработка версий 2. x Microsoft Windows Desktop Search (WDS) настоятельно не рекомендуется в пользу Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104135002"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a><span data-ttu-id="78238-103">Расширение индекса (устаревшие функции среды Windows)</span><span class="sxs-lookup"><span data-stu-id="78238-103">Extending the Index (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="78238-104">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="78238-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="78238-105">В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="78238-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="78238-106">Использование и разработка версий 2. x Microsoft Windows Desktop Search (WDS) настоятельно не рекомендуется в пользу [Windows Search](../search/-search-3x-wds-overview.md).</span><span class="sxs-lookup"><span data-stu-id="78238-106">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged in favor of [Windows Search](../search/-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="78238-107">WDS можно расширить для индексации содержимого новых типов файлов и хранилищ данных.</span><span class="sxs-lookup"><span data-stu-id="78238-107">WDS can be extended to index the contents of new file types and data stores.</span></span> <span data-ttu-id="78238-108">В настоящее время WDS 2. x содержит фильтры для более чем 200 типов элементов (включая такие элементы, как HTML, XML и файлы исходного кода) и использует ту же технологию [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)и обработчик протокола, что и службы SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="78238-108">Currently, WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)and protocol handler technology as SharePoint Services.</span></span> <span data-ttu-id="78238-109">Если для новых типов файлов уже установлены реализации фильтров, службы WDS могут использовать существующие интерфейсы фильтра для индексирования этих данных.</span><span class="sxs-lookup"><span data-stu-id="78238-109">If you already have filter implementations installed for your new file types, WDS can use the existing filter interfaces to index this data.</span></span>

<span data-ttu-id="78238-110">Надстройки WDS 2. x позволяют индексу просматривать и анализировать новые данные и структуры данных для добавления в каталог с возможностью поиска.</span><span class="sxs-lookup"><span data-stu-id="78238-110">WDS 2.x add-ins enable the index to traverse and parse new data and data structures for information to add to the searchable catalog.</span></span> <span data-ttu-id="78238-111">Эти надстройки также могут расширять оболочку Windows, чтобы связать значки и обработчики контекстного меню с новыми типами файлов и хранилищами данных.</span><span class="sxs-lookup"><span data-stu-id="78238-111">These add-ins can also extend the Windows Shell to associate icons and context-menu handlers with the new file types and data stores.</span></span> <span data-ttu-id="78238-112">Чтобы включить новые типы файлов в каталог WDS, надстройка должна реализовать интерфейс [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter).</span><span class="sxs-lookup"><span data-stu-id="78238-112">To include new file types in the WDS catalog, an add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface.</span></span> <span data-ttu-id="78238-113">Чтобы включить новые хранилища данных, надстройка должна быть обработчиком протокола.</span><span class="sxs-lookup"><span data-stu-id="78238-113">To include new data stores, an add-in must be a protocol handler.</span></span> <span data-ttu-id="78238-114">Если новое хранилище данных содержит внедренные файлы или новые типы файлов, также потребуется написать соответствующий фильтр.</span><span class="sxs-lookup"><span data-stu-id="78238-114">If the new data store includes embedded files or new file types itself, you will also need to write an appropriate filter as well.</span></span>

> [!Note]
>
> <span data-ttu-id="78238-115">Фильтры и обработчики протоколов должны быть написаны в машинном коде из-за потенциальных проблем с управлением версиями среды CLR с помощью процесса все надстройки, запущенные в.</span><span class="sxs-lookup"><span data-stu-id="78238-115">Filters and protocol handlers must be written in native code due to potential CLR versioning issues with the process all add-ins run in.</span></span>

 

## <a name="adding-file-types-to-the-index"></a><span data-ttu-id="78238-116">Добавление типов файлов в индекс</span><span class="sxs-lookup"><span data-stu-id="78238-116">Adding File Types to the Index</span></span>

<span data-ttu-id="78238-117">Надстройки могут расширять службы WDS для индексации новых или собственных типов файлов, а также связывать каждый новый тип файлов с помощью значка файла или контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="78238-117">Add-ins can extend WDS to index new or proprietary file types and to associate each new file type with a file-specific icon or context menu.</span></span> <span data-ttu-id="78238-118">Для этого можно создать и зарегистрировать надстройку, которая:</span><span class="sxs-lookup"><span data-stu-id="78238-118">To do this, you can build and register an add-in that:</span></span>

1.  <span data-ttu-id="78238-119">Реализует интерфейс [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)для каждого типа файлов, чтобы службы WDS могли обращаться к тексту и метаданным типа файла и индексировать их.</span><span class="sxs-lookup"><span data-stu-id="78238-119">Implements an [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface for each file type so WDS can access and index the file type's text and metadata.</span></span>
2.  <span data-ttu-id="78238-120">Реализует интерфейсы **иекстрактикон** и **IContextMenu** для добавления значков и контекстных меню для повышения степени интеграции и удобства использования.</span><span class="sxs-lookup"><span data-stu-id="78238-120">Implements the **IExtractIcon** and **IContextMenu** interfaces to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="78238-121">Обсуждение реализации фильтров см. в разделе [Разработка надстроек IFilter](-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="78238-121">For a discussion on implementing filters, see [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="adding-data-stores-to-the-index"></a><span data-ttu-id="78238-122">Добавление хранилищ данных в индекс</span><span class="sxs-lookup"><span data-stu-id="78238-122">Adding Data Stores to the Index</span></span>

<span data-ttu-id="78238-123">Надстройки могут расширять возможности WDS для индексации новых хранилищ данных и сопоставления файлов с помощью значка файла или контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="78238-123">Add-ins can extend WDS to index new data stores and to associate files with a file-specific icon or context menu.</span></span> <span data-ttu-id="78238-124">Для этого можно создать и зарегистрировать обработчик протокола, который:</span><span class="sxs-lookup"><span data-stu-id="78238-124">To do this, you can build and register a protocol handler that:</span></span>

1.  <span data-ttu-id="78238-125">Реализует интерфейсы **исеарчпротокол** и **иурлакцессор** для обработки и привязки отдельных элементов в источнике содержимого.</span><span class="sxs-lookup"><span data-stu-id="78238-125">Implements the **ISearchProtocol** and **IUrlAccessor** interfaces to process and bind individual items in the content source.</span></span> <span data-ttu-id="78238-126">WDS использует URL-адреса для уникальной идентификации элементов, будь то элементы в файловой системе, в хранилище, похожем на базу данных, или в Интернете.</span><span class="sxs-lookup"><span data-stu-id="78238-126">WDS uses URLs to uniquely identify items, whether those items are in the file system, inside a database-like store, or on the Web.</span></span>
2.  <span data-ttu-id="78238-127">Реализует интерфейс **иперсистфолдер** и части интерфейса **ишеллфолдер** для добавления значков и контекстных меню для повышения степени интеграции и удобства использования.</span><span class="sxs-lookup"><span data-stu-id="78238-127">Implements the **IPersistFolder** interface and portions of the **IShellFolder** interface to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="78238-128">Обсуждение реализации обработчиков протоколов см. в разделе [Разработка обработчиков протоколов](-search-2x-wds-phaddins.md).</span><span class="sxs-lookup"><span data-stu-id="78238-128">For a discussion on implementing protocol handlers, see [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span></span>

## <a name="add-in-installer-guidelines"></a><span data-ttu-id="78238-129">Рекомендации по установщику для надстройки</span><span class="sxs-lookup"><span data-stu-id="78238-129">Add-in Installer Guidelines</span></span>

<span data-ttu-id="78238-130">Установка надстройки должна соответствовать следующим рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="78238-130">Installation of an add-in should follow the following guidelines:</span></span>

-   <span data-ttu-id="78238-131">Установщик должен использовать установщик EXE или MSI.</span><span class="sxs-lookup"><span data-stu-id="78238-131">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="78238-132">Необходимо указать заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="78238-132">Release notes must be provided.</span></span>
-   <span data-ttu-id="78238-133">Для каждой установленной надстройки необходимо создать запись « **Установка и удаление программ** ».</span><span class="sxs-lookup"><span data-stu-id="78238-133">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="78238-134">Установщик должен задействовать все параметры реестра для конкретного типа файлов или хранить данные, распознаваемые текущей надстройкой.</span><span class="sxs-lookup"><span data-stu-id="78238-134">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="78238-135">Если предыдущая надстройка перезаписывается, установщик должен уведомить пользователя.</span><span class="sxs-lookup"><span data-stu-id="78238-135">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="78238-136">Если более новая надстройка перезаписала предыдущую надстройку, то должна быть возможность восстановить функциональность предыдущей надстройки и сделать ее надстройкой по умолчанию для этого типа файла или хранилища.</span><span class="sxs-lookup"><span data-stu-id="78238-136">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78238-137">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="78238-137">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="78238-138">**Reference**</span><span class="sxs-lookup"><span data-stu-id="78238-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78238-139">Разработка надстроек IFilter</span><span class="sxs-lookup"><span data-stu-id="78238-139">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="78238-140">Разработка обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="78238-140">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="78238-141">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="78238-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="78238-142">**IFilter**</span><span class="sxs-lookup"><span data-stu-id="78238-142">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
