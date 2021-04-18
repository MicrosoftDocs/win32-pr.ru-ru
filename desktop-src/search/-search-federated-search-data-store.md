---
description: В этой статье объясняется, как разрешить доступ к хранилищу данных через веб-службу OpenSearch и как избежать потенциальных препятствий для этого.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Включение хранилища данных в федеративный поиск Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cef227cb82c64f391ec61b2a7fef0fe35acf131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719318"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a><span data-ttu-id="a577b-103">Включение хранилища данных в федеративный поиск Windows</span><span class="sxs-lookup"><span data-stu-id="a577b-103">Enabling Your Data Store in Windows Federated Search</span></span>

<span data-ttu-id="a577b-104">В этой статье объясняется, как разрешить доступ к хранилищу данных через веб-службу [OpenSearch](https://github.com/dewitt/opensearch) и как избежать потенциальных препятствий для этого.</span><span class="sxs-lookup"><span data-stu-id="a577b-104">Explains how to enable your data store to be accessed by an [OpenSearch](https://github.com/dewitt/opensearch) web service, and how to avoid potential barriers for doing so.</span></span>

<span data-ttu-id="a577b-105">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a577b-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a577b-106">Условия принятия запроса поиска</span><span class="sxs-lookup"><span data-stu-id="a577b-106">Conditions for Search Request Acceptance</span></span>](#conditions-for-search-request-acceptance)
    -   [<span data-ttu-id="a577b-107">Поддерживаемый синтаксис запросов</span><span class="sxs-lookup"><span data-stu-id="a577b-107">Supported Query Syntax</span></span>](#supported-query-syntax)
    -   [<span data-ttu-id="a577b-108">Поддерживаемые протоколы проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="a577b-108">Supported Authentication Protocols</span></span>](#supported-authentication-protocols)
-   [<span data-ttu-id="a577b-109">Отправка запросов и возврат результатов поиска в RSS или Atom</span><span class="sxs-lookup"><span data-stu-id="a577b-109">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [<span data-ttu-id="a577b-110">Пример выходных данных RSS-канала</span><span class="sxs-lookup"><span data-stu-id="a577b-110">Example of an RSS Feed Output</span></span>](#example-of-an-rss-feed-output)
-   [<span data-ttu-id="a577b-111">Автоматическое сопоставление свойств оболочки Windows</span><span class="sxs-lookup"><span data-stu-id="a577b-111">Automatic Mapping to Windows Shell Properties</span></span>](#automatic-mapping-to-windows-shell-properties)
-   [<span data-ttu-id="a577b-112">Общие сведения о том, как Windows сопоставляет элементы с типами файлов</span><span class="sxs-lookup"><span data-stu-id="a577b-112">Understanding How Windows Maps Items to File Types</span></span>](#understanding-how-windows-maps-items-to-file-types)
-   [<span data-ttu-id="a577b-113">Предотвращение потенциальных препятствий для включения хранилища данных</span><span class="sxs-lookup"><span data-stu-id="a577b-113">Avoiding Potential Barriers to Enabling a Data Store</span></span>](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [<span data-ttu-id="a577b-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a577b-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="a577b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a577b-115">Related topics</span></span>](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a><span data-ttu-id="a577b-116">Условия принятия запроса поиска</span><span class="sxs-lookup"><span data-stu-id="a577b-116">Conditions for Search Request Acceptance</span></span>

<span data-ttu-id="a577b-117">Веб-служба [OpenSearch](https://github.com/dewitt/opensearch) , созданная на веб-сервере, **должна** удовлетворять следующим двум требованиям.</span><span class="sxs-lookup"><span data-stu-id="a577b-117">The [OpenSearch](https://github.com/dewitt/opensearch) web service you create on your web server **must** fulfill the following two requirements:</span></span>

-   <span data-ttu-id="a577b-118">Возможность принимать `GET URL` запрос от клиента.</span><span class="sxs-lookup"><span data-stu-id="a577b-118">Be able to accept a `GET URL` query from the client.</span></span>
-   <span data-ttu-id="a577b-119">Позволяет внедрять условия поиска в URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a577b-119">Permit the search terms to be embedded in the URL.</span></span>

    <span data-ttu-id="a577b-120">В следующем примере показано, как условие поиска может быть внедрено в URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a577b-120">The following example shows how a search term can be embedded in a URL.</span></span>

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> <span data-ttu-id="a577b-121">Федеративный поиск не поддерживает отправку `POST` запросов к веб-службе.</span><span class="sxs-lookup"><span data-stu-id="a577b-121">Federated search does not support sending `POST` requests to a web service.</span></span>

 

<span data-ttu-id="a577b-122">Дополнительные сведения о создании URL-адреса см. в разделе "Параметры шаблона URL-адреса" раздела [Создание файла описания OpenSearch в Федеративной службы Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="a577b-122">For more information about constructing a URL, see "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

### <a name="supported-query-syntax"></a><span data-ttu-id="a577b-123">Поддерживаемый синтаксис запросов</span><span class="sxs-lookup"><span data-stu-id="a577b-123">Supported Query Syntax</span></span>

<span data-ttu-id="a577b-124">В Windows 7 не ожидался Специальный синтаксис запроса.</span><span class="sxs-lookup"><span data-stu-id="a577b-124">There is no specific query syntax expected in Windows 7.</span></span> <span data-ttu-id="a577b-125">Поставщик OpenSearch принимает любые термины, которые пользователь вводит в поле ввода в проводнике Windows, и кодирует его в URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a577b-125">The OpenSearch provider accepts whatever terms the user enters in the input box in Windows Explorer, and encodes it into the URL.</span></span> <span data-ttu-id="a577b-126">Это делается в соответствии с шаблоном URL-адреса, описанным в разделе "Параметры шаблона URL-адреса", в разделе [Создание файла описания OpenSearch в приложении федеративного поиска Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="a577b-126">It does so according to the URL template described in "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

<span data-ttu-id="a577b-127">Пользователи предполагают, что отдельные термины рассматриваются как неявно and вместе.</span><span class="sxs-lookup"><span data-stu-id="a577b-127">Users expect that separate terms are treated as implicitly ANDed together.</span></span> <span data-ttu-id="a577b-128">Например, запрос "Microsoft Windows" должен возвращать только результаты, содержащие "Windows" и "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="a577b-128">For example, a query for "Microsoft Windows" should return only results that contain both "Windows" and "Microsoft".</span></span>

### <a name="supported-authentication-protocols"></a><span data-ttu-id="a577b-129">Поддерживаемые протоколы проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="a577b-129">Supported Authentication Protocols</span></span>

<span data-ttu-id="a577b-130">Федеративный поиск Windows поддерживает проверку подлинности на основе Windows и может предоставлять учетные данные веб-службам с помощью следующих протоколов:</span><span class="sxs-lookup"><span data-stu-id="a577b-130">Windows Federated Search supports Windows-based authentication, and can provide credentials to web services via the following protocols:</span></span>

-   <span data-ttu-id="a577b-131">NTLM.</span><span class="sxs-lookup"><span data-stu-id="a577b-131">NTLM.</span></span>
-   <span data-ttu-id="a577b-132">Kerberos —</span><span class="sxs-lookup"><span data-stu-id="a577b-132">Kerberos.</span></span>
-   <span data-ttu-id="a577b-133">Basic (только по протоколу HTTPS).</span><span class="sxs-lookup"><span data-stu-id="a577b-133">Basic (only over https).</span></span>
-   <span data-ttu-id="a577b-134">Другие поставщики поддержки безопасности (SSP), установленные в Windows, которые обеспечивают дополнительную производительность запросов.</span><span class="sxs-lookup"><span data-stu-id="a577b-134">Other Security Support Providers (SSPs) installed on Windows that provide additional querying capacity.</span></span> <span data-ttu-id="a577b-135">Сведения о потенциальном добавлении других SSP см. в документации по пакету SDK для [интерфейса SSP](../secauthn/sspi.md) .</span><span class="sxs-lookup"><span data-stu-id="a577b-135">See the [SSP Interface](../secauthn/sspi.md) SDK documentation to keep abreast of the potential addition of other SSPs.</span></span>

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="a577b-136">Отправка запросов и возврат результатов поиска в RSS или Atom</span><span class="sxs-lookup"><span data-stu-id="a577b-136">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="a577b-137">Поставщик [OpenSearch](https://github.com/dewitt/opensearch) отвечает за сопоставление значений XML-элементов с системными свойствами оболочки Windows, которые могут использоваться приложениями Windows.</span><span class="sxs-lookup"><span data-stu-id="a577b-137">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span> <span data-ttu-id="a577b-138">Но вы не ограничены сопоставлениями по умолчанию для стандартных элементов RSS или Atom и могут содержать пользовательские XML-элементы в пространстве имен Windows для каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="a577b-138">But you are not limited to the default mappings of standard RSS or Atom elements, and can include custom XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="a577b-139">Например, можно добавить собственные пользовательские XML-элементы в элемент **Item** для предоставления дополнительных метаданных в Windows.</span><span class="sxs-lookup"><span data-stu-id="a577b-139">For example, you can add your own custom XML elements within the **item** element to provide additional metadata to Windows.</span></span> <span data-ttu-id="a577b-140">Можно также сопоставлять элементы из других пространств имен XML, например iTunes</span><span class="sxs-lookup"><span data-stu-id="a577b-140">You can also map elements from other XML namespaces, such as iTunes</span></span>

### <a name="example-of-an-rss-feed-output"></a><span data-ttu-id="a577b-141">Пример выходных данных RSS-канала</span><span class="sxs-lookup"><span data-stu-id="a577b-141">Example of an RSS Feed Output</span></span>

<span data-ttu-id="a577b-142">Следующий пример вывода RSS-канала возвращает один элемент.</span><span class="sxs-lookup"><span data-stu-id="a577b-142">The following example RSS feed output returns one item.</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, you'd be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="a577b-143">Дополнительные сведения о сопоставлении свойств см. в разделах "Расширенные элементы в федеративного поиска WIndows" и "сопоставления настраиваемых свойств" раздела [Создание файла описания OpenSearch в федеративной системе Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="a577b-143">For more detailed information about property mapping, see the "Extended Elements in WIndows Federated Search" and "Custom Property Mappings" sections in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="automatic-mapping-to-windows-shell-properties"></a><span data-ttu-id="a577b-144">Автоматическое сопоставление свойств оболочки Windows</span><span class="sxs-lookup"><span data-stu-id="a577b-144">Automatic Mapping to Windows Shell Properties</span></span>

<span data-ttu-id="a577b-145">В элементах RSS-канала можно выбрать включение других элементов XML, которые автоматически сопоставляются с системными свойствами оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="a577b-145">Within the items in your RSS feed, you can choose to include other XML elements that automatically map to Windows Shell system properties.</span></span> <span data-ttu-id="a577b-146">Для этого включите элемент с именем после свойства оболочки Windows и предваряя его пространством имен системы оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="a577b-146">To do so, include an element named after the Windows Shell property and prefixed with the Windows Shell system namespace.</span></span> <span data-ttu-id="a577b-147">В следующем примере показано объявление пространства имен `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` и включение элемента для сопоставления свойств `win:System.Contact.PrimaryEmailAddress` .</span><span class="sxs-lookup"><span data-stu-id="a577b-147">The following example illustrates the namespace declaration `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` and the inclusion of an element for the property mapping `win:System.Contact.PrimaryEmailAddress`:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



<span data-ttu-id="a577b-148">Префикс пространства имен, используемый здесь ( `"win"` ), является предложением; можно использовать любой префикс.</span><span class="sxs-lookup"><span data-stu-id="a577b-148">The namespace prefix used here (`"win"`) is a suggestion; you can use any prefix.</span></span> <span data-ttu-id="a577b-149">Однако необходимо использовать точные имена свойств оболочки Windows, а также указать точный универсальный код ресурса (URI), как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="a577b-149">However, you must use the exact Windows Shell property names, and must include the exact Uniform Resource Identifier (URI), as shown in the following example:</span></span>


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



<span data-ttu-id="a577b-150">**О свойствах системы оболочки Windows**</span><span class="sxs-lookup"><span data-stu-id="a577b-150">**About Windows Shell System Properties**</span></span>

<span data-ttu-id="a577b-151">Windows определяет полный список [системных свойств](../properties/props.md) и формат типа значения, необходимый для каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="a577b-151">Windows defines a complete list of [System Properties](../properties/props.md) and the value type format required for each property.</span></span> <span data-ttu-id="a577b-152">В документации для свойства оболочки [System. fileExtension](../properties/props-system-fileextension.md) указано, что значение должно содержать начальную точку (". docx", а не "docx").</span><span class="sxs-lookup"><span data-stu-id="a577b-152">The documentation for the [System.FileExtension](../properties/props-system-fileextension.md) Window Shell property, for example, specifies that the value must contain the leading dot (".docx" and not "docx").</span></span>

<span data-ttu-id="a577b-153">**Значения даты и времени**</span><span class="sxs-lookup"><span data-stu-id="a577b-153">**Date and Time Values**</span></span>

<span data-ttu-id="a577b-154">Предпочтительный формат даты и времени — ISO-8601, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="a577b-154">The preferred date and time format is ISO-8601, as shown in the following example:</span></span>


```
2008-01-16T 19:20:30:.45+01:00
```



<span data-ttu-id="a577b-155">Разработчики .NET должны использовать класс DateTime с `ToString("R") ` для вывода правильного формата.</span><span class="sxs-lookup"><span data-stu-id="a577b-155">.NET developers should use the DateTime class with `ToString("R") `to output the correct format.</span></span>

<span data-ttu-id="a577b-156">Дополнительные сведения о сопоставлении свойств см. в разделе "Расширенные элементы в федеративного поиска Windows" статьи [Создание файла описания OpenSearch в приложении федеративного поиска Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="a577b-156">For more detailed information about property mapping, see "Extended Elements in Windows Federated Search" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="understanding-how-windows-maps-items-to-file-types"></a><span data-ttu-id="a577b-157">Общие сведения о том, как Windows сопоставляет элементы с типами файлов</span><span class="sxs-lookup"><span data-stu-id="a577b-157">Understanding How Windows Maps Items to File Types</span></span>

<span data-ttu-id="a577b-158">Поиск в пользовательском интерфейсе проводника Windows позволяет пользователям обрабатывать результаты в виде файлов, когда элемент RSS указывает на файл, хранящийся удаленно.</span><span class="sxs-lookup"><span data-stu-id="a577b-158">Searching within the Windows Explorer UI permits users to treat results as files when an RSS item points to a file stored remotely.</span></span> <span data-ttu-id="a577b-159">Пользователь может перетаскивать элементы на Рабочий стол, а пользовательский интерфейс проводника Windows отображает правильный значок и предоставляет соответствующее контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="a577b-159">The user can drag and drop items to the desktop, and the Windows Explorer UI displays the correct icon and provides the appropriate shortcut menu.</span></span> <span data-ttu-id="a577b-160">Если элемент RSS не указывает на удаленный файл, файл рассматривается как ссылка, и пользователи могут выполнять над ним такие действия, как создание ярлыка или открытие его в браузере.</span><span class="sxs-lookup"><span data-stu-id="a577b-160">If the RSS item does not point to a remotely stored file, the file is treated as a link, and users can perform actions on it such as creating a shortcut or opening it in the browser.</span></span>

<span data-ttu-id="a577b-161">В следующей блок-схеме показано, как Windows определяет тип файла элемента.</span><span class="sxs-lookup"><span data-stu-id="a577b-161">The following flowchart shows how Windows determines an item's file type.</span></span>

![Блок-схема, показывающая пути от элемента к решениям, которые обрабатывают его как элемент типа Web Link или как тип файла](images/determineanitemfiletype.png)

<span data-ttu-id="a577b-163">Поставщик [OpenSearch](https://github.com/dewitt/opensearch) выполняет следующие действия по сопоставлению элемента с типом файла:</span><span class="sxs-lookup"><span data-stu-id="a577b-163">The [OpenSearch](https://github.com/dewitt/opensearch) provider performs the following steps to map an item to a file type:</span></span>

-   <span data-ttu-id="a577b-164">Определить, следует ли обрабатывать элемент как файл или как веб-ссылку.</span><span class="sxs-lookup"><span data-stu-id="a577b-164">Identify whether the item should be treated as a file or a web link.</span></span>
-   <span data-ttu-id="a577b-165">Укажите правильное используемое расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="a577b-165">Identify the correct file name extension to use.</span></span>

<span data-ttu-id="a577b-166">Например, если у элемента есть URL-адрес ссылки, который использует путь к файловой системе (например `file:///\\server\share\etc\item.ext` ,), поставщик [OpenSearch](https://github.com/dewitt/opensearch) рассматривает ссылку как файл и определяет тип по расширению имени файла, используемому в пути (расширение ext в этом примере).</span><span class="sxs-lookup"><span data-stu-id="a577b-166">For example, if the item has a link URL that uses a file system path (such as `file:///\\server\share\etc\item.ext`), the [OpenSearch](https://github.com/dewitt/opensearch) provider treats the link as a file and determines the type by the file name extension used in the path (.ext in this example).</span></span>

<span data-ttu-id="a577b-167">Если элемент использует стандартный RSS-корпус или **медиарсс Media: Content** , поставщик [OpenSearch](https://github.com/dewitt/opensearch) предполагает, что элемент является файлом, и определяет расширение имени файла следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a577b-167">If the item uses the standard RSS enclosure or **MediaRSS media:content** element, the [OpenSearch](https://github.com/dewitt/opensearch) provider assumes that the item is a file and identifies the file name extension as follows:</span></span>

-   <span data-ttu-id="a577b-168">Если для элемента было сопоставлено свойство оболочки Windows [System. fileExtension](../properties/props-system-fileextension.md) , поставщик использует это расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="a577b-168">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has been mapped for the item, the provider uses that file name extension.</span></span>
-   <span data-ttu-id="a577b-169">Если свойство оболочки Windows [System. fileExtension](../properties/props-system-fileextension.md) не сопоставлено, поставщик использует атрибут **Type** , указанный в элементе enclosure или Content.</span><span class="sxs-lookup"><span data-stu-id="a577b-169">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has not been mapped, the provider uses the **Type** attribute specified in the enclosure or content element.</span></span> <span data-ttu-id="a577b-170">Этот элемент должен содержать `MIMEType` строку, например `"image/jpeg"` .</span><span class="sxs-lookup"><span data-stu-id="a577b-170">This element should contain a `MIMEType` string, such as `"image/jpeg"`.</span></span> <span data-ttu-id="a577b-171">Если объект `MIMEType` связан с расширением имени файла, зарегистрированным на клиентском компьютере, элемент считается файлом этого типа.</span><span class="sxs-lookup"><span data-stu-id="a577b-171">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the item is regarded as a file of that type.</span></span> <span data-ttu-id="a577b-172">Если объект `MIMEType` не связан с расширением имени файла, зарегистрированным на клиентском компьютере, элемент рассматривается как тип веб-ссылки.</span><span class="sxs-lookup"><span data-stu-id="a577b-172">If the `MIMEType` is not associated with a file name extension registered on the client computer, the item is treated as a web link type.</span></span> <span data-ttu-id="a577b-173">Поставщик [OpenSearch](https://github.com/dewitt/opensearch) не пытается проанализировать атрибут **URL-адреса** , чтобы определить расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="a577b-173">The [OpenSearch](https://github.com/dewitt/opensearch) provider does not attempt to parse the **Url** attribute to locate the file name extension.</span></span>
-   <span data-ttu-id="a577b-174">Если объект `MIMEType` связан с расширением имени файла, зарегистрированным на клиентском компьютере, поставщик определяет, является ли расширение имени файла известным типом веб-файла (. htm,. HTML,. ASP,. aspx,. php,. SWF,. stm).</span><span class="sxs-lookup"><span data-stu-id="a577b-174">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the provider determines whether the file name extension is a known web file type (.htm, .html, .asp, .aspx, .php, .swf, .stm).</span></span> <span data-ttu-id="a577b-175">Если да, то тип файла рассматривается как тип веб-ссылки. в противном случае он рассматривается как тип файла.</span><span class="sxs-lookup"><span data-stu-id="a577b-175">If so, the file type is regarded as a web link type; otherwise, it is regarded as a file type.</span></span> <span data-ttu-id="a577b-176">Например, если объект `MIMEType "text/html"` связан с расширением htm, этот элемент рассматривается как веб-ссылка, а не как файл. htm.</span><span class="sxs-lookup"><span data-stu-id="a577b-176">For example, if the `MIMEType "text/html"` is associated with the .htm file name extension, that item is regarded as a web link instead of as an .htm file type.</span></span>

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a><span data-ttu-id="a577b-177">Предотвращение потенциальных препятствий для включения хранилища данных</span><span class="sxs-lookup"><span data-stu-id="a577b-177">Avoiding Potential Barriers to Enabling a Data Store</span></span>

<span data-ttu-id="a577b-178">Некоторые хранилища данных не предоставляют веб-службу, совместимую с [OpenSearch](https://github.com/dewitt/opensearch), но по-прежнему могут быть подключены к федеративным поиску Windows.</span><span class="sxs-lookup"><span data-stu-id="a577b-178">Some data stores do not provide an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service but can still be connected to Windows Federated Search.</span></span> <span data-ttu-id="a577b-179">К таким хранилищам данных относятся:</span><span class="sxs-lookup"><span data-stu-id="a577b-179">Such data stores include:</span></span>

-   <span data-ttu-id="a577b-180">Удаленные индексы с методами проверки подлинности, которые не поддерживаются в Федеративной службе поиска Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a577b-180">Remote indexes with authentication methods that are not supported in Windows 7 Federated Search.</span></span>

    <span data-ttu-id="a577b-181">Примеры включают проверку подлинности на основе форм и другие пользовательские методы проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a577b-181">Examples include forms-based authentication and other custom authentication methods.</span></span>

-   <span data-ttu-id="a577b-182">Если общедоступное хранилище высокой ценности содержит общедоступные веб-API, любой пользователь может написать другую веб-службу, совместимую с [OpenSearch](https://github.com/dewitt/opensearch), и вызвать эти API в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="a577b-182">If a high-value public store has public web APIs, anyone can write another web service that is [OpenSearch](https://github.com/dewitt/opensearch)-compatible and calls those APIs behind the scenes.</span></span>

    <span data-ttu-id="a577b-183">Примеры включают библиотеку Congress и базы данных медицинских исследований.</span><span class="sxs-lookup"><span data-stu-id="a577b-183">Examples include the Library of Congress, and medical research databases.</span></span>

-   <span data-ttu-id="a577b-184">Частные хранилища данных предприятия или индексы, а также устаревшие хранилища управления содержимым, для которых невозможно реализовать внешний интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a577b-184">Proprietary enterprise data stores or indexes, and legacy content management stores, for which it might be impossible to implement a front end.</span></span>

<span data-ttu-id="a577b-185">Однако существуют альтернативные варианты, позволяющие избежать барьеров при включении хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="a577b-185">However, there are alternatives that can avoid barriers to enabling a data store.</span></span> <span data-ttu-id="a577b-186">Ниже приведены некоторые из этих вариантов.</span><span class="sxs-lookup"><span data-stu-id="a577b-186">The following are some of those alternatives:</span></span>

<span data-ttu-id="a577b-187">**Для создания веб-службы среднего звена, когда нельзя изменить веб-службу для существующего источника данных, или веб-служба предоставляет настраиваемый API:**</span><span class="sxs-lookup"><span data-stu-id="a577b-187">**To write a middle-man web service when you cannot modify the web service for the existing data source, or the web service provides a custom API:**</span></span>

1.  <span data-ttu-id="a577b-188">Напишите веб-службу среднего звена, которая может принимать запрос Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a577b-188">Write a middle-man web service that can accept a Windows 7 query.</span></span>
2.  <span data-ttu-id="a577b-189">Подключитесь к источнику данных и получите результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="a577b-189">Connect to your data source, and retrieve the query results.</span></span>
3.  <span data-ttu-id="a577b-190">Переформатируйте результаты в формате RSS или Atom.</span><span class="sxs-lookup"><span data-stu-id="a577b-190">Reformat the results in RSS or Atom format.</span></span>
4.  <span data-ttu-id="a577b-191">Возврат результатов в клиент Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a577b-191">Return the results to the Windows 7 client.</span></span>
5.  <span data-ttu-id="a577b-192">Обратите внимание, что для служб корпоративных данных и многих служб данных Интернета может потребоваться передать учетные данные пользователя от имени веб-службы, чтобы выполнить усечение результатов на основе разрешений пользователя.</span><span class="sxs-lookup"><span data-stu-id="a577b-192">Note that for enterprise data services and many Internet data services, you may need to pass the user credentials through on behalf of the web service to perform result trimming based on the user's permissions.</span></span>

<span data-ttu-id="a577b-193">**Чтобы использовать существующую поисковую подсистему, если не удается включить общедоступное хранилище данных:**</span><span class="sxs-lookup"><span data-stu-id="a577b-193">**To use an existing search engine when you cannot enable a public data store:**</span></span>

1.  <span data-ttu-id="a577b-194">Используйте общедоступную поисковую подсистемку, которая уже поддерживает [OpenSearch](https://github.com/dewitt/opensearch) с RSS.</span><span class="sxs-lookup"><span data-stu-id="a577b-194">Use a public search engine that already supports [OpenSearch](https://github.com/dewitt/opensearch) with RSS.</span></span> <span data-ttu-id="a577b-195">Это можно сделать, предоставив пользователям файл с расширением OSDX-с шаблоном URL-адреса, который будет ограничивать результаты только теми, которые относятся к конкретному домену.</span><span class="sxs-lookup"><span data-stu-id="a577b-195">You can do so by providing your users with an .osdx file that has a URL template that restricts results to only those for your specific domain.</span></span>
2.  <span data-ttu-id="a577b-196">См. Следующий пример описания [OpenSearch](https://github.com/dewitt/opensearch) для поиска только содержимого справки для Windows с помощью запроса к Live.com.</span><span class="sxs-lookup"><span data-stu-id="a577b-196">See the following example of an [OpenSearch](https://github.com/dewitt/opensearch) description for searching only the Help content for Windows by using a query against live.com.</span></span>

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
      <ShortName>Windows Help</ShortName>
      <Description>Search Windows Help using the live.com search engine</Description>
      <Language></Language>
      <Url type="text/html" template="https://windowshelp.microsoft.com/windows/search.aspx?=&amp;qu={searchTerms}"/>
      <Url type="application/rss+xml" template="https://api.search.live.com/rss.aspx?source=web&amp;query={searchTerms} site:windowshelp.microsoft.com&amp;web.count=50"/>
    </OpenSearchDescription>
    ```

    

<span data-ttu-id="a577b-197">**Чтобы использовать существующий сервер индексирования, поддерживающий OpenSearch, если не удается включить собственные корпоративные хранилища данных или индексы, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="a577b-197">**To use an existing indexing server that supports OpenSearch when you cannot enable proprietary enterprise data stores or indexes:**</span></span>

1.  <span data-ttu-id="a577b-198">Выберите существующий сервер индексирования, который поддерживает [OpenSearch](https://github.com/dewitt/opensearch) для индексирования содержимого, например SharePoint Search Server.</span><span class="sxs-lookup"><span data-stu-id="a577b-198">Select an existing indexing server that supports [OpenSearch](https://github.com/dewitt/opensearch) to index your content, such as the SharePoint Search Server.</span></span>
2.  <span data-ttu-id="a577b-199">Создайте OSDX--файл, который будет ограничивать результаты в индексе SharePoint только теми, которые относятся к серверу, используя синтаксис ключевых слов в шаблоне URL.</span><span class="sxs-lookup"><span data-stu-id="a577b-199">Create an .osdx file that restricts the results from the SharePoint index to only those from your server by using their KeyWord syntax within the URL template.</span></span>

<span data-ttu-id="a577b-200">**Чтобы создать хранилище данных на стороне клиента, если не работает решение на стороне сервера:**</span><span class="sxs-lookup"><span data-stu-id="a577b-200">**To write a client-side data store if a server-side-only solution does not work:**</span></span>

1.  <span data-ttu-id="a577b-201">Напишите Клиентский источник данных [OpenSearch](https://github.com/dewitt/opensearch) , расположенный между поставщиком Windows [OpenSearch](https://github.com/dewitt/opensearch) и внешним источником данных.</span><span class="sxs-lookup"><span data-stu-id="a577b-201">Write a client-side [OpenSearch](https://github.com/dewitt/opensearch) data source that sits between the Windows [OpenSearch](https://github.com/dewitt/opensearch) provider and the external data source.</span></span>
2.  <span data-ttu-id="a577b-202">Используйте API [интерфейса иопенсеарчсаурце](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) в Windows SDK, чтобы создать соответствующий файл. сеарчконнектор-MS, через который проводник Windows может вызвать реализацию с параметрами запроса.</span><span class="sxs-lookup"><span data-stu-id="a577b-202">Use the [IOpenSearchSource Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) API in the Windows SDK to create an appropriately configured .searchconnector-ms file through which Windows Explorer can call your implementation with the query parameters.</span></span> <span data-ttu-id="a577b-203">Затем ваша реализация может вернуть результаты в формате RSS или Atom.</span><span class="sxs-lookup"><span data-stu-id="a577b-203">Your implementation can then return results formatted in RSS or Atom format.</span></span> <span data-ttu-id="a577b-204">Это позволит вашей реализации предоставлять пользовательский пользовательский интерфейс проверки подлинности и подключаться к источнику данных с помощью собственного API-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a577b-204">Doing so enables your implementation to provide custom authentication UI and to connect to the data source using its proprietary API.</span></span>

> [!Note]  
> <span data-ttu-id="a577b-205">При открытии файла. OSDX-в каталоге% UserProfile%/сеарчес создается файл. сеарчконнектор-MS (соединитель поиска), который помещает ссылку на него в каталог% UserProfile%/Линкс.</span><span class="sxs-lookup"><span data-stu-id="a577b-205">Opening an .osdx file creates a .searchconnector-ms file (search connector) in the %userprofile%/searches directory and places a link to it in the %userprofile%/links directory.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="a577b-206">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a577b-206">Additional Resources</span></span>

<span data-ttu-id="a577b-207">Дополнительные сведения о реализации Федерации поиска в удаленных хранилищах данных с помощью технологий OpenSearch в Windows 7 и более поздних версиях см. в разделе "дополнительные ресурсы" в [Федеративной функции поиска в Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a577b-207">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a577b-208">См. также</span><span class="sxs-lookup"><span data-stu-id="a577b-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a577b-209">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="a577b-209">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="a577b-210">начало работы с федеративными поиском в Windows</span><span class="sxs-lookup"><span data-stu-id="a577b-210">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="a577b-211">Подключение веб-службы в Федеративной службе поиска Windows</span><span class="sxs-lookup"><span data-stu-id="a577b-211">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="a577b-212">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="a577b-212">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="a577b-213">Следующие рекомендации по использованию федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="a577b-213">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="a577b-214">Развертывание соединителей поиска в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="a577b-214">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
