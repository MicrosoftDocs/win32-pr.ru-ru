---
description: Установка обработчика протокола включает копирование библиотек DLL в соответствующее расположение в каталоге Program Files, а затем регистрацию обработчика протокола с помощью реестра.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Установка и регистрация обработчиков протоколов (Поиск Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682530"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a><span data-ttu-id="71e55-103">Установка и регистрация обработчиков протоколов (Поиск Windows)</span><span class="sxs-lookup"><span data-stu-id="71e55-103">Installing and Registering Protocol Handlers (Windows Search)</span></span>

<span data-ttu-id="71e55-104">Установка обработчика протокола включает копирование библиотек DLL в соответствующее расположение в каталоге Program Files, а затем регистрацию обработчика протокола с помощью реестра.</span><span class="sxs-lookup"><span data-stu-id="71e55-104">Installing a protocol handler involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the protocol handler through the registry.</span></span> <span data-ttu-id="71e55-105">Приложение установки может также добавить правила корня и области поиска, чтобы определить область обхода по умолчанию для источника данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="71e55-105">The installation application can also add a search root and scope rules to define a default crawl scope for the Shell data source.</span></span>

<span data-ttu-id="71e55-106">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="71e55-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="71e55-107">Об URL-адресах</span><span class="sxs-lookup"><span data-stu-id="71e55-107">About URLs</span></span>](#about-urls)
-   [<span data-ttu-id="71e55-108">Реализация интерфейсов обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-108">Implementing Protocol Handler Interfaces</span></span>](#implementing-protocol-handler-interfaces)
    -   [<span data-ttu-id="71e55-109">Исеарчпротокол и ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="71e55-109">ISearchProtocol and ISearchProtocol2</span></span>](#isearchprotocol-and-isearchprotocol2)
    -   [<span data-ttu-id="71e55-110">Иурлакцессор, IUrlAccessor2, IUrlAccessor3 и IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="71e55-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [<span data-ttu-id="71e55-111">ипротоколхандлерсите</span><span class="sxs-lookup"><span data-stu-id="71e55-111">IProtocolHandlerSite</span></span>](#iprotocolhandlersite)
-   [<span data-ttu-id="71e55-112">Реализация обработчиков фильтров для контейнеров</span><span class="sxs-lookup"><span data-stu-id="71e55-112">Implementing Filter Handlers for Containers</span></span>](#implementing-filter-handlers-for-containers)
-   [<span data-ttu-id="71e55-113">Установка и регистрация обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-113">Installing and Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="71e55-114">Рекомендации по регистрации обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-114">Guidelines for Registering a Protocol Handler</span></span>](#guidelines-for-registering-a-protocol-handler)
    -   [<span data-ttu-id="71e55-115">Регистрация обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-115">Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="71e55-116">Регистрация обработчика типа файла обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-116">Registering the Protocol Handler's File Type Handler</span></span>](#registering-the-protocol-handlers-file-type-handler)
-   [<span data-ttu-id="71e55-117">Проверка индексации элементов</span><span class="sxs-lookup"><span data-stu-id="71e55-117">Ensuring that Your Items are Indexed</span></span>](#ensuring-that-your-items-are-indexed)
-   [<span data-ttu-id="71e55-118">См. также</span><span class="sxs-lookup"><span data-stu-id="71e55-118">Related topics</span></span>](#related-topics)

## <a name="about-urls"></a><span data-ttu-id="71e55-119">Об URL-адресах</span><span class="sxs-lookup"><span data-stu-id="71e55-119">About URLs</span></span>

<span data-ttu-id="71e55-120">Поиск Windows использует URL-адреса для уникальной идентификации элементов в иерархии источника данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="71e55-120">Windows Search uses URLs to uniquely identify items in the hierarchy of your Shell data source.</span></span> <span data-ttu-id="71e55-121">URL-адрес, который является первым узлом в иерархии, называется [корнем поиска](-search-3x-wds-extidx-csm-searchroots.md). Поиск Windows начнет индексироваться в корне поиска, запрашивая, что обработчик протокола перечислит дочерние ссылки для каждого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="71e55-121">The URL that is the first node in the hierarchy is called the [search root](-search-3x-wds-extidx-csm-searchroots.md); Windows Search will begin indexing at the search root, requesting that the protocol handler enumerate child links for each URL.</span></span>

<span data-ttu-id="71e55-122">Типичная структура URL-адресов:</span><span class="sxs-lookup"><span data-stu-id="71e55-122">The typical URL structure is:</span></span>


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



<span data-ttu-id="71e55-123">Синтаксис URL-адреса описан в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="71e55-123">The URL syntax is described in the following table.</span></span>



| <span data-ttu-id="71e55-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71e55-124">Syntax</span></span>           | <span data-ttu-id="71e55-125">Описание</span><span class="sxs-lookup"><span data-stu-id="71e55-125">Description</span></span>                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | <span data-ttu-id="71e55-126">Определяет, какой обработчик протокола вызывать для URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="71e55-126">Identifies which protocol handler to invoke for the URL.</span></span>                                                                                                                                                           |
| <span data-ttu-id="71e55-127">{SID пользователя}</span><span class="sxs-lookup"><span data-stu-id="71e55-127">{user SID}</span></span>       | <span data-ttu-id="71e55-128">Определяет контекст безопасности пользователя, в котором вызывается обработчик протокола.</span><span class="sxs-lookup"><span data-stu-id="71e55-128">Identifies the user security context under which the protocol handler is called.</span></span> <span data-ttu-id="71e55-129">Если идентификатор безопасности (SID) пользователя не определен, обработчик протокола вызывается в контексте безопасности системной службы.</span><span class="sxs-lookup"><span data-stu-id="71e55-129">If no user security identifier (SID) is identified, the protocol handler is called in the security context of the system service.</span></span> |
| <path>     | <span data-ttu-id="71e55-130">Определяет иерархию хранилища, где каждая косая черта ("/") является разделителем между именами папок.</span><span class="sxs-lookup"><span data-stu-id="71e55-130">Defines the hierarchy of the store, where each forward slash ('/') is a separator between folder names.</span></span>                                                                                                            |
| <ItemID>   | <span data-ttu-id="71e55-131">Представляет уникальную строку, определяющую дочерний элемент (например, имя файла).</span><span class="sxs-lookup"><span data-stu-id="71e55-131">Represents a unique string that identifies the child item (for example, the file name).</span></span>                                                                                                                            |



 

<span data-ttu-id="71e55-132">Индексатор поиска Windows усекает окончательную косую черту по URL-адресам.</span><span class="sxs-lookup"><span data-stu-id="71e55-132">The Windows Search Indexer trims the final slash from URLs.</span></span> <span data-ttu-id="71e55-133">В результате нельзя полагаться на существование последней косой черты для определения каталога и элемента.</span><span class="sxs-lookup"><span data-stu-id="71e55-133">As a result you cannot rely on the existence of a final slash to identify a directory versus an item.</span></span> <span data-ttu-id="71e55-134">Обработчик протокола должен иметь возможность обрабатывать этот синтаксис URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="71e55-134">Your protocol handler must be able to handle this URL syntax.</span></span> <span data-ttu-id="71e55-135">Убедитесь, что имя протокола, выбранное для обнаружения источника данных оболочки, не конфликтует с текущими.</span><span class="sxs-lookup"><span data-stu-id="71e55-135">Ensure that the protocol name that you select to identify your Shell data source does not conflict with current ones.</span></span> <span data-ttu-id="71e55-136">Мы рекомендуем использовать такое соглашение об именовании: `companyName.scheme` .</span><span class="sxs-lookup"><span data-stu-id="71e55-136">We recommend this naming convention: `companyName.scheme`.</span></span>

<span data-ttu-id="71e55-137">Дополнительные сведения о создании источника данных оболочки см. в разделе [реализация базовых интерфейсов объекта папки](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71e55-137">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

## <a name="implementing-protocol-handler-interfaces"></a><span data-ttu-id="71e55-138">Реализация интерфейсов обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-138">Implementing Protocol Handler Interfaces</span></span>

<span data-ttu-id="71e55-139">Для создания обработчика протокола требуется реализация следующих трех интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="71e55-139">Creating a protocol handler requires the implementation of the following three interfaces:</span></span>

-   <span data-ttu-id="71e55-140">[**Исеарчпротокол**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) для управления объектами урлакцессор.</span><span class="sxs-lookup"><span data-stu-id="71e55-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects.</span></span>
-   <span data-ttu-id="71e55-141">[**Иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) , чтобы предоставить свойства и выявить соответствующие фильтры для элементов в источнике данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="71e55-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) to expose properties and identify appropriate filters for items in the Shell data source.</span></span>
-   <span data-ttu-id="71e55-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) для фильтрации собственных файлов или перечисления и фильтрации файлов, хранимых иерархически.</span><span class="sxs-lookup"><span data-stu-id="71e55-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span>

<span data-ttu-id="71e55-143">Кроме трех обязательных интерфейсов, другие интерфейсы являются необязательными, и вы в libertyе реализовывать, какие необязательные интерфейсы наиболее подходят для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="71e55-143">Other than the three mandatory interfaces listed, the other interfaces are optional, and you are at liberty to implement whichever optional interfaces are most appropriate for the task at hand.</span></span>

### <a name="isearchprotocol-and-isearchprotocol2"></a><span data-ttu-id="71e55-144">Исеарчпротокол и ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="71e55-144">ISearchProtocol and ISearchProtocol2</span></span>

<span data-ttu-id="71e55-145">Интерфейсы Сеарчпротокол инициализируют и управляют объектами Урлакцессор обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="71e55-145">The SearchProtocol interfaces initialize and manage your protocol handler UrlAccessor objects.</span></span> <span data-ttu-id="71e55-146">Интерфейс [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) является дополнительным расширением [**исеарчпротокол**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)и включает дополнительный метод для указания дополнительных сведений о пользователе и элементе.</span><span class="sxs-lookup"><span data-stu-id="71e55-146">The [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) interface is an optional extension of [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol), and includes an extra method to specify more information about the user and the item.</span></span>

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a><span data-ttu-id="71e55-147">Иурлакцессор, IUrlAccessor2, IUrlAccessor3 и IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="71e55-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>

<span data-ttu-id="71e55-148">Интерфейсы [**иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="71e55-148">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces are described in the following table.</span></span>



| <span data-ttu-id="71e55-149">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="71e55-149">Interface</span></span>                                                 | <span data-ttu-id="71e55-150">Описание</span><span class="sxs-lookup"><span data-stu-id="71e55-150">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71e55-151">**иурлакцессор**</span><span class="sxs-lookup"><span data-stu-id="71e55-151">**IUrlAccessor**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | <span data-ttu-id="71e55-152">Для указанного URL-адреса интерфейс [**иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) предоставляет доступ к свойствам элемента, предоставляемого в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="71e55-152">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interface provides access to the properties of the item that is exposed in the URL.</span></span> <span data-ttu-id="71e55-153">Он также может привязать эти свойства к фильтру, зависящему от обработчика протокола (т. е. к фильтру, отличному от того, который связан с именем файла).</span><span class="sxs-lookup"><span data-stu-id="71e55-153">It can also bind those properties to a protocol handler-specific filter (that is, a filter other than the one associated with the file name).</span></span> |
| <span data-ttu-id="71e55-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="71e55-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (optional)</span></span> | <span data-ttu-id="71e55-155">Интерфейс [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) расширяет [**иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) с помощью методов, которые получают кодовую страницу для свойств элемента и его отображаемого URL-адреса и получают тип элемента в URL-адресе (документ или каталог).</span><span class="sxs-lookup"><span data-stu-id="71e55-155">The [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) interface extends [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) with methods that get a code page for the item's properties and its display URL, and that get the type of item in the URL (document or directory).</span></span>                                    |
| <span data-ttu-id="71e55-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="71e55-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (optional)</span></span> | <span data-ttu-id="71e55-157">Интерфейс [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) расширяет [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) с помощью метода, который получает массив идентификаторов безопасности пользователя, позволяя узлу протокола поиска олицетворять этих пользователей для индексирования элемента.</span><span class="sxs-lookup"><span data-stu-id="71e55-157">The [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface extends [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) with a method that gets an array of user SIDs, enabling the search protocol host to impersonate these users to index the item.</span></span>                                                      |
| <span data-ttu-id="71e55-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="71e55-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (optional)</span></span> | <span data-ttu-id="71e55-159">Интерфейс [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) расширяет функциональные возможности интерфейса [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) с помощью метода, который определяет, следует ли индексировать содержимое элемента.</span><span class="sxs-lookup"><span data-stu-id="71e55-159">The [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) interface extends the functionality of the [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface with a method that identifies whether the content of the item should be indexed.</span></span>                                                                 |



 

<span data-ttu-id="71e55-160">Экземпляр объекта Урлакцессор создается и инициализируется объектом Сеарчпротокол.</span><span class="sxs-lookup"><span data-stu-id="71e55-160">The UrlAccessor object is instantiated and initialized by a SearchProtocol object.</span></span> <span data-ttu-id="71e55-161">Интерфейсы [**иурлакцессор**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) предоставляют доступ к важным сведениям с помощью методов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="71e55-161">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces provide access to important pieces of information through the methods described in the following table.</span></span>



| <span data-ttu-id="71e55-162">Метод</span><span class="sxs-lookup"><span data-stu-id="71e55-162">Method</span></span>                                                                                        | <span data-ttu-id="71e55-163">Описание</span><span class="sxs-lookup"><span data-stu-id="71e55-163">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71e55-164">**Иурлакцессор:: Жетластмодифиед**</span><span class="sxs-lookup"><span data-stu-id="71e55-164">**IUrlAccessor::GetLastModified**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | <span data-ttu-id="71e55-165">Возвращает время последнего изменения URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="71e55-165">Returns the time that the URL was last modified.</span></span> <span data-ttu-id="71e55-166">Если это время новее, чем последний раз, когда индексатор обработал этот URL-адрес, вызываются обработчики фильтров (реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) для извлечения (возможно) измененных данных для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="71e55-166">If this time is more recent than the last time the indexer processed this URL, filter handlers (implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) are called to extract the (possibly) changed data for that item.</span></span> <span data-ttu-id="71e55-167">Изменение времени для каталогов игнорируется.</span><span class="sxs-lookup"><span data-stu-id="71e55-167">Modified times for directories are ignored.</span></span> |
| [<span data-ttu-id="71e55-168">**Иурлакцессор:: подкаталог**</span><span class="sxs-lookup"><span data-stu-id="71e55-168">**IUrlAccessor::IsDirectory**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | <span data-ttu-id="71e55-169">Определяет, представляет ли URL-адрес папку, содержащую дочерние URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="71e55-169">Identifies whether the URL represents a folder containing a child URLs.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="71e55-170">**Иурлакцессор:: Биндтостреам**</span><span class="sxs-lookup"><span data-stu-id="71e55-170">**IUrlAccessor::BindToStream**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | <span data-ttu-id="71e55-171">Выполняет привязку к [интерфейсу IStream](/windows/win32/api/objidl/nn-objidl-istream) , который представляет данные файла в пользовательском хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="71e55-171">Binds to an [IStream interface](/windows/win32/api/objidl/nn-objidl-istream) that represents the data of a file in a custom data store.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="71e55-172">**Иурлакцессор:: Биндтофилтер**</span><span class="sxs-lookup"><span data-stu-id="71e55-172">**IUrlAccessor::BindToFilter**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | <span data-ttu-id="71e55-173">Привязывает к интерфейсу [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), зависящему от обработчика протокола, который может предоставлять свойства для элемента.</span><span class="sxs-lookup"><span data-stu-id="71e55-173">Binds to a protocol handler-specific [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), which can expose properties for the item.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="71e55-174">**IUrlAccessor4:: Шаулдиндекситемконтент**</span><span class="sxs-lookup"><span data-stu-id="71e55-174">**IUrlAccessor4::ShouldIndexItemContent**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | <span data-ttu-id="71e55-175">Определяет, следует ли индексировать содержимое элемента.</span><span class="sxs-lookup"><span data-stu-id="71e55-175">Identifies whether the content of the item should be indexed.</span></span>                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a><span data-ttu-id="71e55-176">ипротоколхандлерсите</span><span class="sxs-lookup"><span data-stu-id="71e55-176">IProtocolHandlerSite</span></span>

<span data-ttu-id="71e55-177">Интерфейс [**ипротоколхандлерсите**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) используется для создания экземпляра обработчика фильтра, который размещается в изолированном процессе.</span><span class="sxs-lookup"><span data-stu-id="71e55-177">The [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) interface is used to instantiate a filter handler, which is hosted in an isolated process.</span></span> <span data-ttu-id="71e55-178">Соответствующий обработчик фильтра получается для указанного идентификатора постоянного класса (CLSID), класса хранилища документов или расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="71e55-178">The appropriate filter handler is obtained for a specified persistent class identifier (CLSID), document storage class, or file name extension.</span></span> <span data-ttu-id="71e55-179">Преимущество запроса хост-процесса к [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) заключается в том, что ведущий процесс может управлять процессом поиска соответствующего обработчика фильтра и контролировать безопасность, связанную с вызовом обработчика.</span><span class="sxs-lookup"><span data-stu-id="71e55-179">The benefit of asking the host process to bind to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is that the host process can manage the process of locating an appropriate filter handler, and control the security involved in calling the handler.</span></span>

## <a name="implementing-filter-handlers-for-containers"></a><span data-ttu-id="71e55-180">Реализация обработчиков фильтров для контейнеров</span><span class="sxs-lookup"><span data-stu-id="71e55-180">Implementing Filter Handlers for Containers</span></span>

<span data-ttu-id="71e55-181">При реализации иерархического обработчика протокола необходимо реализовать обработчик фильтра для контейнера, который перечисляет дочерние URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="71e55-181">If you are implementing a hierarchical protocol handler, then you must implement a filter handler for a container that enumerates child URLs.</span></span> <span data-ttu-id="71e55-182">Обработчик фильтра является реализацией интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="71e55-182">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span> <span data-ttu-id="71e55-183">Процесс перечисления — это цикл по методам [**IFilter::-фрагмента**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) и [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) интерфейса **IFilter** . Каждый дочерний URL-адрес предоставляется как значение свойства.</span><span class="sxs-lookup"><span data-stu-id="71e55-183">The enumeration process is a loop through the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) and [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) methods of the **IFilter** interface; each child URL is exposed as the value of the property.</span></span>

<span data-ttu-id="71e55-184">[**IFilter:: "**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) Возвращает свойства контейнера.</span><span class="sxs-lookup"><span data-stu-id="71e55-184">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns the properties of the container.</span></span> <span data-ttu-id="71e55-185">Чтобы перечислить дочерние URL-адреса, **IFilter::** GetEnumerator возвращает один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="71e55-185">To enumerate child URLs, **IFilter::GetChunk** returns either of the following:</span></span>

-   <span data-ttu-id="71e55-186">[PKEY \_ Поиск \_ урлтоиндекс](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="71e55-186">[PKEY\_Search\_UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span></span>

    <span data-ttu-id="71e55-187">URL-адрес элемента без времени последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="71e55-187">The URL to the item without the last modified time.</span></span> <span data-ttu-id="71e55-188">[**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) возвращает пропвариант, содержащий дочерний URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="71e55-188">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing the child URL.</span></span>

-   <span data-ttu-id="71e55-189">[PKEY \_ Поиск \_ урлтоиндексвисмодификатионтиме](../properties/props-system-search-urltoindexwithmodificationtime.md):</span><span class="sxs-lookup"><span data-stu-id="71e55-189">[PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span></span>

    <span data-ttu-id="71e55-190">URL-адрес и время последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="71e55-190">The URL and the last modified time.</span></span> <span data-ttu-id="71e55-191">[**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) возвращает пропвариант, содержащий вектор URL-адреса дочернего элемента и время последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="71e55-191">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing a vector of the child URL and the last modified time.</span></span>

<span data-ttu-id="71e55-192">Возвращать [ \_ \_ урлтоиндексвисмодификатионтиме поиска PKEY](../properties/props-system-search-urltoindexwithmodificationtime.md) более эффективно, так как индексатор может немедленно определить, нужно ли индексировать элемент, не вызывая методы [**Исеарчпротокол:: CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) и [**иурлакцессор:: жетластмодифиед**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) .</span><span class="sxs-lookup"><span data-stu-id="71e55-192">Returning [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the [**ISearchProtocol::CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) and [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) methods.</span></span>

<span data-ttu-id="71e55-193">В следующем примере кода демонстрируется возврат свойства [PKEY \_ Search \_ урлтоиндексвисмодификатионтиме](../properties/props-system-search-urltoindexwithmodificationtime.md) .</span><span class="sxs-lookup"><span data-stu-id="71e55-193">The following example code demonstrates how to return the [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) property.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="71e55-194">(c) Корпорация Майкрософт (Microsoft Corporation). Все права защищены</span><span class="sxs-lookup"><span data-stu-id="71e55-194">Copyright (c) Microsoft Corporation.</span></span> <span data-ttu-id="71e55-195">Все права защищены.</span><span class="sxs-lookup"><span data-stu-id="71e55-195">All rights reserved.</span></span>

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> <span data-ttu-id="71e55-196">Компоненту [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) контейнера всегда следует перечислять все дочерние URL-адреса, даже если дочерние URL-адреса не изменялись, так как индексатор обнаруживает удаления с помощью процесса перечисления.</span><span class="sxs-lookup"><span data-stu-id="71e55-196">A container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) component should always enumerate all child URLs even if the child URLs have not changed, because the indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="71e55-197">Если выходные данные даты в [ \_ \_ урлтоиндексвисмодификатионтиме поиска PKEY](../properties/props-system-search-urltoindexwithmodificationtime.md) указывают на то, что данные не изменялись, индексатор не обновляет данные для этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="71e55-197">If the date output in a [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

## <a name="installing-and-registering-a-protocol-handler"></a><span data-ttu-id="71e55-198">Установка и регистрация обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-198">Installing and Registering a Protocol Handler</span></span>

<span data-ttu-id="71e55-199">Установка обработчиков протоколов включает копирование библиотек DLL в соответствующее расположение в каталоге Program Files, а затем регистрацию DLL-библиотек.</span><span class="sxs-lookup"><span data-stu-id="71e55-199">Installing protocol handlers involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the DLL(s).</span></span> <span data-ttu-id="71e55-200">Обработчики протоколов должны реализовать самостоятельную регистрацию для установки.</span><span class="sxs-lookup"><span data-stu-id="71e55-200">Protocol handlers should implement self-registration for installation.</span></span> <span data-ttu-id="71e55-201">Приложение установки может также добавить корень поиска и правила области, чтобы определить область обхода содержимого по умолчанию для источника данных оболочки, которая рассматривается в разделе [Проверка того, что элементы индексируются](#ensuring-that-your-items-are-indexed) в конце этого раздела.</span><span class="sxs-lookup"><span data-stu-id="71e55-201">The installation application can also add a search root, and scope rules to define a default crawl scope for the Shell data source, which is discussed in [Ensuring that Your Items are Indexed](#ensuring-that-your-items-are-indexed) at the end of this topic.</span></span>

### <a name="guidelines-for-registering-a-protocol-handler"></a><span data-ttu-id="71e55-202">Рекомендации по регистрации обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-202">Guidelines for Registering a Protocol Handler</span></span>

<span data-ttu-id="71e55-203">При регистрации обработчика протокола следует следовать приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="71e55-203">You should follow these guidelines when registering a protocol handler:</span></span>

-   <span data-ttu-id="71e55-204">Установщик должен использовать установщик EXE или MSI.</span><span class="sxs-lookup"><span data-stu-id="71e55-204">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="71e55-205">Необходимо указать заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="71e55-205">Release notes must be provided.</span></span>
-   <span data-ttu-id="71e55-206">Для каждой установленной надстройки необходимо создать запись «Установка и удаление программ».</span><span class="sxs-lookup"><span data-stu-id="71e55-206">An Add/Remove Programs entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="71e55-207">Установщик должен задействовать все параметры реестра для конкретного типа файлов или хранить данные, распознаваемые текущей надстройкой.</span><span class="sxs-lookup"><span data-stu-id="71e55-207">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="71e55-208">Если предыдущая надстройка перезаписывается, установщик должен уведомить пользователя.</span><span class="sxs-lookup"><span data-stu-id="71e55-208">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="71e55-209">Если более новая надстройка перезаписала предыдущую надстройку, то должна быть возможность восстановить функциональность предыдущей надстройки и сделать ее надстройкой по умолчанию для этого типа файлов.</span><span class="sxs-lookup"><span data-stu-id="71e55-209">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>
-   <span data-ttu-id="71e55-210">Установщик должен определить область обхода по умолчанию для индексатора, добавив корень поиска и правила области с помощью диспетчера области сканирования (CSM).</span><span class="sxs-lookup"><span data-stu-id="71e55-210">The installer should define a default crawl scope for the indexer by adding a search root, and scope rules using the Crawl Scope Manager (CSM).</span></span>

### <a name="registering-a-protocol-handler"></a><span data-ttu-id="71e55-211">Регистрация обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-211">Registering a Protocol Handler</span></span>

<span data-ttu-id="71e55-212">Для регистрации компонента обработчика протокола необходимо внести в реестр записи четырнадцать, где:</span><span class="sxs-lookup"><span data-stu-id="71e55-212">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="71e55-213">*Версия \_ Параметр \_* "DIB ProgID" — это независимый от версии идентификатор ProgID реализации обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="71e55-213">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="71e55-214">*Версия \_ DEP \_ ProgID* — это зависимый от версии идентификатор ProgID реализации обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="71e55-214">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="71e55-215">*CLSID \_ 1* — это CLSID реализации обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="71e55-215">*CLSID\_1* is the CLSID of the protocol handler implementation.</span></span>

<span data-ttu-id="71e55-216">**Чтобы зарегистрировать обработчик протокола, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="71e55-216">**To register a protocol handler:**</span></span>

1.  <span data-ttu-id="71e55-217">Зарегистрируйте независимый от версии идентификатор ProgID со следующими ключами и значениями:</span><span class="sxs-lookup"><span data-stu-id="71e55-217">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="71e55-218">Зарегистрируйте версию ProgID, зависимую от версии, со следующими ключами и значениями:</span><span class="sxs-lookup"><span data-stu-id="71e55-218">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="71e55-219">Зарегистрируйте CLSID обработчика протокола со следующими ключами и значениями:</span><span class="sxs-lookup"><span data-stu-id="71e55-219">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  <span data-ttu-id="71e55-220">Зарегистрируйте обработчик протокола в службе поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="71e55-220">Register the protocol handler with Windows Search.</span></span> <span data-ttu-id="71e55-221">В следующем примере <Protocol Name> — это имя самого протокола, например File, MAPI и т. д.</span><span class="sxs-lookup"><span data-stu-id="71e55-221">In the following example, <Protocol Name> is the name of the protocol itself, such as file, mapi, and so forth:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    <span data-ttu-id="71e55-222">До Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="71e55-222">Prior to Windows Vista:</span></span>

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a><span data-ttu-id="71e55-223">Регистрация обработчика типа файла обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-223">Registering the Protocol Handler's File Type Handler</span></span>

<span data-ttu-id="71e55-224">Для регистрации обработчика типа файла обработчика протокола (который также называется расширением оболочки) необходимо создать две записи в реестре.</span><span class="sxs-lookup"><span data-stu-id="71e55-224">You need to make two entries in the registry to register the protocol handler's file type handler (which is also known as a Shell extension).</span></span>

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a><span data-ttu-id="71e55-225">Проверка индексации элементов</span><span class="sxs-lookup"><span data-stu-id="71e55-225">Ensuring that Your Items are Indexed</span></span>

<span data-ttu-id="71e55-226">После реализации обработчика протокола необходимо указать, какие элементы оболочки должен индексировать обработчик протокола.</span><span class="sxs-lookup"><span data-stu-id="71e55-226">After you have implemented your protocol handler, you must specify which Shell items your protocol handler is to index.</span></span> <span data-ttu-id="71e55-227">Для инициации повторного индексирования можно использовать диспетчер каталогов (Дополнительные сведения см. [в разделе Использование диспетчера каталога](-search-3x-wds-mngidx-catalog-manager.md)).</span><span class="sxs-lookup"><span data-stu-id="71e55-227">You can use the Catalog Manager to initiate re-indexing (for more information, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md)).</span></span> <span data-ttu-id="71e55-228">Кроме того, можно использовать диспетчер области сканирования (CSM) для настройки правил по умолчанию, указывающих URL-адреса, которые должен обходить индексатор (Дополнительные сведения см. [в разделе Использование диспетчера области сканирования](-search-3x-wds-extidx-csm.md) и [Управление правилами области действия](-search-3x-wds-extidx-csm-scoperules.md)).</span><span class="sxs-lookup"><span data-stu-id="71e55-228">Or you can also use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl (for more information, see [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md) and [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md)).</span></span> <span data-ttu-id="71e55-229">Вы также можете добавить корень поиска (Дополнительные сведения см. в разделе [Управление корнями поиска](-search-3x-wds-extidx-csm-searchroots.md)).</span><span class="sxs-lookup"><span data-stu-id="71e55-229">You can also add a search root (for more information, see [Managing Search Roots](-search-3x-wds-extidx-csm-searchroots.md)).</span></span> <span data-ttu-id="71e55-230">Кроме того, можно выполнить процедуру, описанную в примере переиндексации в разделе [примеры пакета SDK для Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="71e55-230">Another option available to you is to follow the procedure in the ReIndex sample in [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="71e55-231">Интерфейс [**исеарчкравлскопеманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) предоставляет методы, которые уведомляют механизм поиска контейнеров для обхода и (или) просмотра, а также элементы в этих контейнерах для включения или исключения при обходе или просмотре.</span><span class="sxs-lookup"><span data-stu-id="71e55-231">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.</span></span> <span data-ttu-id="71e55-232">В Windows 7 и более поздних версиях [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) расширяет **исеарчкравлскопеманажер** с помощью метода [**ISearchCrawlScopeManager2::**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) Method, который получает версию, которая информирует клиентов о том, изменилось ли состояние CSM.</span><span class="sxs-lookup"><span data-stu-id="71e55-232">In Windows 7 and later, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extends **ISearchCrawlScopeManager** with the [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) method that gets the version, which informs clients whether the state of the CSM has changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71e55-233">См. также</span><span class="sxs-lookup"><span data-stu-id="71e55-233">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="71e55-234">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="71e55-234">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="71e55-235">Основные сведения о обработчиках протоколов</span><span class="sxs-lookup"><span data-stu-id="71e55-235">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="71e55-236">Разработка обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="71e55-236">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="71e55-237">Уведомление индекса изменений</span><span class="sxs-lookup"><span data-stu-id="71e55-237">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="71e55-238">Добавление значков и контекстных меню</span><span class="sxs-lookup"><span data-stu-id="71e55-238">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="71e55-239">Пример кода: расширения оболочки для обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="71e55-239">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="71e55-240">Создание соединителя поиска для обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="71e55-240">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="71e55-241">Обработчики протокола отладки</span><span class="sxs-lookup"><span data-stu-id="71e55-241">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
