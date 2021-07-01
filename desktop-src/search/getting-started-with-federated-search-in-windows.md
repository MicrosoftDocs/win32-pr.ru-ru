---
description: Сведения о федеративной службе поиска, которая позволяет пользователям получать доступ к удаленным данным и взаимодействовать с ними в проводнике Windows.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: начало работы с федеративными поиском в Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de3fc42686e94f2edc1c5d45bbb0374afe79535
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119069"
---
# <a name="getting-started-with-federated-search-in-windows"></a><span data-ttu-id="ef72c-103">начало работы с федеративными поиском в Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-103">Getting Started with Federated Search in Windows</span></span>

<span data-ttu-id="ef72c-104">Поддержка интеграции поиска в Windows 7 с удаленными хранилищами данных с помощью технологий OpenSearch позволяет пользователям получать доступ к удаленным данным и взаимодействовать с ними в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="ef72c-105">Вы можете создать веб-хранилище данных, в котором можно выполнять поиск с помощью федеративного поиска Windows, и обеспечить широкие возможности интеграции удаленных источников данных с проводником Windows без необходимости писать или развертывать код на стороне клиента Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-105">You can build a web-based data store that can be searched using Windows federated search and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="ef72c-106">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ef72c-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ef72c-107">Что такое федеративный поиск?</span><span class="sxs-lookup"><span data-stu-id="ef72c-107">What is Federated Search?</span></span>](#what-is-federated-search)
-   [<span data-ttu-id="ef72c-108">Шаги для создания федеративного поиска</span><span class="sxs-lookup"><span data-stu-id="ef72c-108">Steps for Building Federated Search</span></span>](#steps-for-building-federated-search)
-   [<span data-ttu-id="ef72c-109">Принцип работы федеративного поиска</span><span class="sxs-lookup"><span data-stu-id="ef72c-109">How Federated Search Works</span></span>](#how-federated-search-works)
-   [<span data-ttu-id="ef72c-110">Отправка запросов и возврат результатов поиска в RSS или Atom</span><span class="sxs-lookup"><span data-stu-id="ef72c-110">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [<span data-ttu-id="ef72c-111">Примеры федеративного поиска</span><span class="sxs-lookup"><span data-stu-id="ef72c-111">Federated Search Examples</span></span>](#federated-search-examples)
-   [<span data-ttu-id="ef72c-112">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ef72c-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="ef72c-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ef72c-113">Related topics</span></span>](#related-topics)

## <a name="what-is-federated-search"></a><span data-ttu-id="ef72c-114">Что такое федеративный поиск?</span><span class="sxs-lookup"><span data-stu-id="ef72c-114">What is Federated Search?</span></span>

<span data-ttu-id="ef72c-115">Windows 7 поддерживает подключение внешних источников к клиенту Windows через протокол [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="ef72c-115">Windows 7 supports the connection of external sources to the Windows client through the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="ef72c-116">Это позволяет пользователям выполнять поиск в удаленном хранилище данных и просматривать результаты в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-116">This enables users to search a remote data store and view results from within Windows Explorer.</span></span> <span data-ttu-id="ef72c-117">Стандарт [OpenSearch](https://github.com/dewitt/opensearch) версии 1.1 определяет простые форматы файлов, которые можно использовать для описания того, как клиент должен запрашивать веб-службу для хранилища данных и как служба должна возвращать результаты, отображаемые клиентом.</span><span class="sxs-lookup"><span data-stu-id="ef72c-117">The [OpenSearch](https://github.com/dewitt/opensearch) v1.1 standard defines simple file formats that can be used to describe how a client should query the web service for the data store and how the service should return results to be rendered by the client.</span></span> <span data-ttu-id="ef72c-118">Федеративный поиск Windows подключается к веб-службам, получающим запросы [OpenSearch](https://github.com/dewitt/opensearch) , и возвращает результаты в формате RSS или Atom XML.</span><span class="sxs-lookup"><span data-stu-id="ef72c-118">Windows federated search connects to web services that receive [OpenSearch](https://github.com/dewitt/opensearch) queries, and returns results in either the RSS or Atom XML format.</span></span>

<span data-ttu-id="ef72c-119">На следующем снимке экрана показаны результаты поиска, полученные после удаленного поиска на сайте SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ef72c-119">The following screen shot illustrates the search results obtained after remotely searching a SharePoint site.</span></span>

![снимок экрана, на котором показаны результаты поиска с сайта SharePoint, отображаемые в проводнике Windows](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a><span data-ttu-id="ef72c-121">Шаги для создания федеративного поиска</span><span class="sxs-lookup"><span data-stu-id="ef72c-121">Steps for Building Federated Search</span></span>

<span data-ttu-id="ef72c-122">Чтобы создать федеративный поиск, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ef72c-122">To build federated search, perform the following steps:</span></span>

1.  <span data-ttu-id="ef72c-123">Включите Поиск в хранилище данных в проводнике Windows, предоставив веб-службу, совместимую с [OpenSearch](https://github.com/dewitt/opensearch), которая может возвращать результаты в формате RSS или Atom.</span><span class="sxs-lookup"><span data-stu-id="ef72c-123">Enable your data store to be searched from Windows Explorer by providing an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service that can return results in RSS or Atom format.</span></span>
2.  <span data-ttu-id="ef72c-124">Создайте файл описания OpenSearch (. OSDX-), в котором описывается, как подключиться к веб-службе и как сопоставлять пользовательские элементы в RSS-или Atom XML.</span><span class="sxs-lookup"><span data-stu-id="ef72c-124">Create an OpenSearch Description (.osdx) file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML.</span></span>
3.  <span data-ttu-id="ef72c-125">Разверните соединители поиска на клиентских компьютерах Windows с помощью файла OSDX-.</span><span class="sxs-lookup"><span data-stu-id="ef72c-125">Deploy the search connectors to Windows client computers with an .osdx file.</span></span>

<span data-ttu-id="ef72c-126">На следующей схеме показаны шаги для создания федеративного поиска.</span><span class="sxs-lookup"><span data-stu-id="ef72c-126">The following diagram illustrates the steps for building federated search.</span></span>

![Схема процесса создания федеративного поиска](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a><span data-ttu-id="ef72c-128">Принцип работы федеративного поиска</span><span class="sxs-lookup"><span data-stu-id="ef72c-128">How Federated Search Works</span></span>

<span data-ttu-id="ef72c-129">Взаимодействие между проводником Windows и веб-службой [OpenSearch](https://github.com/dewitt/opensearch) осуществляется через уровень данных Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-129">Communication between Windows Explorer and your [OpenSearch](https://github.com/dewitt/opensearch) web service is performed through the Windows Data Layer.</span></span> <span data-ttu-id="ef72c-130">Уровень данных Windows может взаимодействовать с различными типами хранилищ данных с помощью поставщиков магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-130">The Windows Data Layer can communicate with different types of data stores through Windows Store Providers.</span></span> <span data-ttu-id="ef72c-131">Каждый поставщик специализируется на взаимодействии с хранилищами данных, которые поддерживают конкретный протокол и имеют определенные возможности.</span><span class="sxs-lookup"><span data-stu-id="ef72c-131">Each provider specializes in communicating with data stores that support a particular protocol and have specific capabilities.</span></span> <span data-ttu-id="ef72c-132">Например, на следующем рисунке СОВС, как поставщик [OpenSearch](https://github.com/dewitt/opensearch) взаимодействует с хранилищами данных, которые предоставляют веб-службу, поддерживающую стандарт [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="ef72c-132">For example, the following illustration sows how the [OpenSearch](https://github.com/dewitt/opensearch) provider communicates with data stores that provide a web service that supports the [OpenSearch](https://github.com/dewitt/opensearch) standard.</span></span>

![Схема, показывающая взаимодействие из проводника Windows на клиенте через хранилище данных OpenSearch на удаленном сервере](images/windowssearchfederationfunctionality.png)

<span data-ttu-id="ef72c-134">Чтобы обеспечить поддержку федеративного поиска в Windows 7 для хранилища данных, необходимо выполнить ряд задач.</span><span class="sxs-lookup"><span data-stu-id="ef72c-134">To enable your data store to support federated search in Windows 7, you must perform a number of tasks.</span></span> <span data-ttu-id="ef72c-135">В следующей таблице перечислены задачи для включения хранилища данных, необходимые для выполнения каждой задачи и место поиска документации.</span><span class="sxs-lookup"><span data-stu-id="ef72c-135">The following table lists tasks for enabling your data store, what is required to accomplish each task, and where to find documentation.</span></span>



| <span data-ttu-id="ef72c-136">Задача</span><span class="sxs-lookup"><span data-stu-id="ef72c-136">Task</span></span>                                                                                                     | <span data-ttu-id="ef72c-137">Требование</span><span class="sxs-lookup"><span data-stu-id="ef72c-137">Requirement</span></span>                                                                                                                                                                                            | <span data-ttu-id="ef72c-138">Документация</span><span class="sxs-lookup"><span data-stu-id="ef72c-138">Documentation</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef72c-139">Включение поиска в хранилище данных в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-139">Enable your data store to be searched by Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="ef72c-140">Создайте веб-службу, совместимую с OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="ef72c-140">Build an OpenSearch-compatible web service.</span></span><br/> <span data-ttu-id="ef72c-141">Создайте файл описания OpenSearch (. OSDX-).</span><span class="sxs-lookup"><span data-stu-id="ef72c-141">Create an OpenSearch Description (.osdx) file.</span></span><br/>                                                                                       | [<span data-ttu-id="ef72c-142">Подключение веб-службы в Федеративной службе поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-142">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/> [<span data-ttu-id="ef72c-143">Включение хранилища данных в федеративный поиск Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-143">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/> |
| <span data-ttu-id="ef72c-144">Активно разверните веб-службу для пользователей на предприятии.</span><span class="sxs-lookup"><span data-stu-id="ef72c-144">Actively deploy your web service to users within an enterprise.</span></span><br/>                               | <span data-ttu-id="ef72c-145">Предоставьте OSDX--файл пользователям, скопируйте его локально и сделайте его доступным для пользователя с помощью ярлыка.</span><span class="sxs-lookup"><span data-stu-id="ef72c-145">Supply an .osdx file to your users, copy it locally, and make it accessible to the user via a shortcut.</span></span><br/>                                                                                     | [<span data-ttu-id="ef72c-146">Развертывание соединителей поиска в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-146">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)<br/>                                                                                                              |
| <span data-ttu-id="ef72c-147">Перечислите результаты поиска в проводнике Windows в ответ на запрос.</span><span class="sxs-lookup"><span data-stu-id="ef72c-147">Enumerate search results in Windows Explorer in response to a query.</span></span><br/>                          | <span data-ttu-id="ef72c-148">Реализуйте веб-службу, которая принимает строку запроса и возвращает результаты в формате RSS или Atom.</span><span class="sxs-lookup"><span data-stu-id="ef72c-148">Implement a web service that accepts a query string and returns results in RSS or Atom format.</span></span><br/>                                                                                              | [<span data-ttu-id="ef72c-149">Подключение веб-службы в Федеративной службе поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-149">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/>                                                                                                            |
| <span data-ttu-id="ef72c-150">Разрешить пользователям добавлять хранилище данных в проводник Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-150">Enable users to add your data store to their Windows Explorer.</span></span><br/>                                | <span data-ttu-id="ef72c-151">Создайте файл OSDX-и предоставьте его пользователям.</span><span class="sxs-lookup"><span data-stu-id="ef72c-151">Create an .osdx file and supply it to your users.</span></span><br/>                                                                                                                                           | [<span data-ttu-id="ef72c-152">Включение хранилища данных в федеративный поиск Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-152">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="ef72c-153">Отображение элементов в виде элементов, сходных с файлами, в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-153">Display your items as file-like items in Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="ef72c-154">Возврат URL-адреса файла или потока содержимого с помощью **корпуса** или **носителя: элементы содержимого**</span><span class="sxs-lookup"><span data-stu-id="ef72c-154">Return a URL to the file or content stream by using **enclosure** or **media:content** elements</span></span><br/> <span data-ttu-id="ef72c-155">Укажите расширение имени файла или тип MIME, распознаваемый клиентским компьютером.</span><span class="sxs-lookup"><span data-stu-id="ef72c-155">Supply a file name extension or a MIME type that the client computer recognizes.</span></span><br/> | [<span data-ttu-id="ef72c-156">Включение хранилища данных в федеративный поиск Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-156">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="ef72c-157">Отображение пользовательских свойств в проводнике Windows, кроме тех, которые определены в стандартах RSS или Atom.</span><span class="sxs-lookup"><span data-stu-id="ef72c-157">Display custom properties in Windows Explorer, beyond those defined in RSS or Atom standards.</span></span><br/> | <span data-ttu-id="ef72c-158">Укажите дополнительные метаданные, используя другое пространство имен XML в выходных данных RSS/Atom.</span><span class="sxs-lookup"><span data-stu-id="ef72c-158">Provide additional metadata by using another XML namespace in your RSS/Atom output.</span></span><br/> <span data-ttu-id="ef72c-159">Добавьте карту свойств в OSDX--файл.</span><span class="sxs-lookup"><span data-stu-id="ef72c-159">Add a property map to your .osdx file.</span></span><br/>                                                       | [<span data-ttu-id="ef72c-160">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-160">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="ef72c-161">Настройка свойств, отображаемых для элементов в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-161">Customize the properties that are displayed for your items in Windows Explorer.</span></span><br/>               | <span data-ttu-id="ef72c-162">Добавьте сопоставления проплист в файл OSDX-.</span><span class="sxs-lookup"><span data-stu-id="ef72c-162">Add proplist mappings to your .osdx file.</span></span><br/>                                                                                                                                                   | [<span data-ttu-id="ef72c-163">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-163">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="ef72c-164">Отображение настраиваемого представления веб-страницы для элементов в области просмотра.</span><span class="sxs-lookup"><span data-stu-id="ef72c-164">Display a custom webpage view of your items in the preview pane.</span></span><br/>                              | <span data-ttu-id="ef72c-165">Возвращают уникальные значения ссылок и вложений.</span><span class="sxs-lookup"><span data-stu-id="ef72c-165">Return distinct link and enclosure values.</span></span><br/> <span data-ttu-id="ef72c-166">Сопоставьте значение URL-адреса со свойством оболочки Windows **System. вебпревиевурл** .</span><span class="sxs-lookup"><span data-stu-id="ef72c-166">Map a URL value to the **System.WebPreviewUrl** Windows Shell property.</span></span><br/>                                                               | [<span data-ttu-id="ef72c-167">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-167">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="ef72c-168">Отображение кнопки панели команд в проводнике Windows, которая выполняет накат запроса к веб-сайту.</span><span class="sxs-lookup"><span data-stu-id="ef72c-168">Display a command bar button in Windows Explorer that rolls the query over to your website.</span></span><br/>   | <span data-ttu-id="ef72c-169">Укажите `Url format="text/html"` шаблон в OSDX--файле.</span><span class="sxs-lookup"><span data-stu-id="ef72c-169">Provide a `Url format="text/html"` template in the .osdx file.</span></span><br/>                                                                                                                              | [<span data-ttu-id="ef72c-170">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-170">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="ef72c-171">Отправка запросов и возврат результатов поиска в RSS или Atom</span><span class="sxs-lookup"><span data-stu-id="ef72c-171">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="ef72c-172">Когда пользователь вводит термин в поле поиска в правом верхнем углу окна проводника, запрос отправляется поставщику [OpenSearch](https://github.com/dewitt/opensearch) , который затем отправляет запрос в удаленное хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="ef72c-172">When the user types a term into the search box in the upper-right corner of Windows Explorer, the query is sent to the [OpenSearch](https://github.com/dewitt/opensearch) provider, which then sends the query to the remote data store.</span></span> <span data-ttu-id="ef72c-173">Удаленная веб-служба реагирует на запрос, предоставляя результаты в виде XML-документа, обычно называемого каналом, в одном из двух поддерживаемых форматов (RSS или Atom).</span><span class="sxs-lookup"><span data-stu-id="ef72c-173">The remote web service responds to the query by providing results in an XML document, typically referred to as a feed, in one of two supported formats (RSS or Atom).</span></span> <span data-ttu-id="ef72c-174">Каждый результирующий элемент в веб-канале включает дочерние элементы XML для представления или описания метаданных элементов, таких как заголовок, URL-адрес, описание, изображение эскиза и т. д.</span><span class="sxs-lookup"><span data-stu-id="ef72c-174">Each result item in the feed includes XML child elements to represent or describe item metadata, such as the title, URL, description, thumbnail image, and so forth.</span></span> <span data-ttu-id="ef72c-175">Поставщик [OpenSearch](https://github.com/dewitt/opensearch) отвечает за сопоставление значений XML-элементов с системными свойствами оболочки Windows, которые могут использоваться приложениями Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-175">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span>

## <a name="federated-search-examples"></a><span data-ttu-id="ef72c-176">Примеры федеративного поиска</span><span class="sxs-lookup"><span data-stu-id="ef72c-176">Federated Search Examples</span></span>

<span data-ttu-id="ef72c-177">Следующий пример файла описания OpenSearch (. OSDX-) состоит из `ShortName` элементов и `Url` , которые являются минимальными необходимыми дочерними элементами для подключения внешнего хранилища данных к клиенту Windows через протокол OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="ef72c-177">The following example OpenSearch Description (.osdx) file consists of `ShortName` and `Url` elements, which are the minimum required child elements to connect an external data store to the Windows client through the OpenSearch protocol.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



<span data-ttu-id="ef72c-178">В следующем примере показано, как сделать хранилище данных с поддержкой веб-сайта доступным в формате RSS и как указать, что должен возвращаться один элемент поиска:</span><span class="sxs-lookup"><span data-stu-id="ef72c-178">The following example illustrates how to make a web-enabled data store searchable in RSS format, and how to specify that one search item be returned:</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, then you would be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="ef72c-179">В следующем примере показано, как сопоставлять свойства со свойствами системы по умолчанию, чтобы отображаемые элементы были отсортированы и сгруппированы:</span><span class="sxs-lookup"><span data-stu-id="ef72c-179">The following example illustrates how to map properties to default system properties so that displayed items are sorted and grouped:</span></span>


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



<span data-ttu-id="ef72c-180">В следующем примере показано, как добавить отображение эскиза к каждому элементу в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ef72c-180">The following example illustrates how to adds a thumbnail image display to each item in Windows Explorer:</span></span>


```
<media:thumbnail>    
```



## <a name="additional-resources"></a><span data-ttu-id="ef72c-181">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ef72c-181">Additional Resources</span></span>

<span data-ttu-id="ef72c-182">Дополнительные сведения о реализации Федерации поиска в удаленных хранилищах данных с помощью технологий OpenSearch в Windows 7 и более поздних версиях см. в разделе "дополнительные ресурсы" в [Федеративной функции поиска в Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ef72c-182">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef72c-183">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ef72c-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef72c-184">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-184">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="ef72c-185">Подключение веб-службы в Федеративной службе поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-185">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="ef72c-186">Включение хранилища данных в федеративный поиск Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-186">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="ef72c-187">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-187">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="ef72c-188">Следующие рекомендации по использованию федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-188">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="ef72c-189">Развертывание соединителей поиска в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ef72c-189">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 




