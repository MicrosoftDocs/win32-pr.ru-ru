---
description: В этом разделе перечислены рекомендации, с помощью которых можно создать веб-хранилище данных, в котором можно выполнять поиск с помощью федеративного поиска Windows, а также интегрировать удаленные источники данных с проводником Windows без необходимости писать или развертывать код на стороне клиента Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Следующие рекомендации по использованию федеративного поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144140"
---
# <a name="following-best-practices-in-windows-federated-search"></a><span data-ttu-id="4fff2-103">Следующие рекомендации по использованию федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="4fff2-103">Following Best Practices in Windows Federated Search</span></span>

<span data-ttu-id="4fff2-104">В этом разделе перечислены рекомендации, с помощью которых можно создать веб-хранилище данных, в котором можно выполнять поиск с помощью федеративного поиска Windows, а также интегрировать удаленные источники данных с проводником Windows без необходимости писать или развертывать код на стороне клиента Windows.</span><span class="sxs-lookup"><span data-stu-id="4fff2-104">This topic lists the best practices through which you can build a web-based data store that can be searched using Windows federated search, and integrates your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="4fff2-105">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4fff2-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="4fff2-106">Рекомендации для федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="4fff2-106">Best Practices for Windows Federated Search</span></span>](#best-practices-for-windows-federated-search)
-   [<span data-ttu-id="4fff2-107">Рекомендации по созданию вывода RSS</span><span class="sxs-lookup"><span data-stu-id="4fff2-107">Best Practices for Creating RSS Output</span></span>](#best-practices-for-creating-rss-output)
-   [<span data-ttu-id="4fff2-108">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4fff2-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="4fff2-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4fff2-109">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a><span data-ttu-id="4fff2-110">Рекомендации для федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="4fff2-110">Best Practices for Windows Federated Search</span></span>

<span data-ttu-id="4fff2-111">Ниже приведены рекомендации по работе с [OpenSearch](https://github.com/dewitt/opensearch) в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4fff2-111">Best practices for working with [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 are as follows:</span></span>

-   <span data-ttu-id="4fff2-112">Поддерживают параметры *{startIndex}* и *{Count}* и обязательно возвращают количество запрошенных элементов, если только не будет возвращено Последнее из результатов.</span><span class="sxs-lookup"><span data-stu-id="4fff2-112">Support the *{startIndex}* and *{count}* parameters, and be sure to always return the number of items requested unless you are returning the last of the results.</span></span>
-   <span data-ttu-id="4fff2-113">Если известно расширение имени файла, сопоставьте его с свойством оболочки Windows [System. fileExtension](../properties/props-system-fileextension.md) .</span><span class="sxs-lookup"><span data-stu-id="4fff2-113">If you know the file name extension, map it to the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property.</span></span> <span data-ttu-id="4fff2-114">Использование расширений имен файлов — лучший способ обозначить тип файла, отличный от типа MIME.</span><span class="sxs-lookup"><span data-stu-id="4fff2-114">Using file name extensions is a better way to identify a file type than MIME type.</span></span>
-   <span data-ttu-id="4fff2-115">Убедитесь, что расширение типа MIME или имя файла, указанное в RSS, совпадает с именем файла и типом MIME, возвращаемым веб-сервером, на котором размещается элемент, при запросе содержимого элемента.</span><span class="sxs-lookup"><span data-stu-id="4fff2-115">Ensure that the MIME type or file name extension that you specify in the RSS matches the file name and MIME type returned in the HTTP header by the web server that hosts the item when the item content is requested.</span></span>
-   <span data-ttu-id="4fff2-116">При возврате файловых элементов по возможности верните размер файла.</span><span class="sxs-lookup"><span data-stu-id="4fff2-116">If you are returning file items, return a file size whenever possible.</span></span> <span data-ttu-id="4fff2-117">Это гарантирует точность диалогового окна «ход загрузки».</span><span class="sxs-lookup"><span data-stu-id="4fff2-117">This ensures that the download progress dialog box is accurate.</span></span>
-   <span data-ttu-id="4fff2-118">Убедитесь, что запросы элементов после конца набора результатов не возвращают результатов.</span><span class="sxs-lookup"><span data-stu-id="4fff2-118">Verify that requests for items beyond the end of the results set return no results.</span></span>
    > [!Note]  
    > <span data-ttu-id="4fff2-119">Не повторять результаты.</span><span class="sxs-lookup"><span data-stu-id="4fff2-119">Do not repeat results.</span></span>

     

-   <span data-ttu-id="4fff2-120">Не помещайте HTML-теги, если они не принадлежат.</span><span class="sxs-lookup"><span data-stu-id="4fff2-120">Do not put HTML tags where they don't belong.</span></span> <span data-ttu-id="4fff2-121">В соответствии со спецификацией RSS они действительны в поле Описание, но не в поле Title.</span><span class="sxs-lookup"><span data-stu-id="4fff2-121">Per the RSS specification, they are valid in the description field, but not in the title field.</span></span>
-   <span data-ttu-id="4fff2-122">Не создавайте вложения для элементов веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="4fff2-122">Do not create enclosures for webpage items.</span></span> <span data-ttu-id="4fff2-123">Например, если вы создаете корпус и сопоставляете расширение имени файла. aspx, файл скачивается проводником Windows в кэш Интернета и выполняется из него.</span><span class="sxs-lookup"><span data-stu-id="4fff2-123">For example, if you create an enclosure and map a file name extension of .aspx, the file is downloaded by Windows Explorer to the Internet cache and executed from there.</span></span> <span data-ttu-id="4fff2-124">Веб-браузеры не обрабатывали тип файла. aspx.</span><span class="sxs-lookup"><span data-stu-id="4fff2-124">Web browsers do not handle the .aspx file type.</span></span> <span data-ttu-id="4fff2-125">Пользователь получит диалоговое окно **Открыть с помощью** , или файл может быть открыт приложением, например Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4fff2-125">The user would get an **Open with** dialog box, or the file might be opened by an application like Microsoft Visual Studio.</span></span> <span data-ttu-id="4fff2-126">Избегайте этого, возвращая элемент ссылки только для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="4fff2-126">Avoid this by returning a link element only for webpages.</span></span>
-   <span data-ttu-id="4fff2-127">Укажите URL-адрес перехода в Интернете в файле OSDX-, используя шаблон URL-адреса с `format="text\html"` .</span><span class="sxs-lookup"><span data-stu-id="4fff2-127">Provide a web roll-over URL in the .osdx file using a URL template with `format="text\html"`.</span></span>
-   <span data-ttu-id="4fff2-128">Укажите URL-адрес родительской папки, контейнера или веб-страницы путем сопоставления значения URL-адреса пользовательского элемента со свойством оболочки Windows [System. итемфолдерпасдисплай](../properties/props-system-itempathdisplay.md) .</span><span class="sxs-lookup"><span data-stu-id="4fff2-128">Provide a URL to the parent folder, container, or webpage by mapping a custom element URL value to the [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell property.</span></span>

## <a name="best-practices-for-creating-rss-output"></a><span data-ttu-id="4fff2-129">Рекомендации по созданию вывода RSS</span><span class="sxs-lookup"><span data-stu-id="4fff2-129">Best Practices for Creating RSS Output</span></span>

<span data-ttu-id="4fff2-130">Ниже приведены рекомендации по созданию выходных данных RSS.</span><span class="sxs-lookup"><span data-stu-id="4fff2-130">Best practices for creating RSS output are as follows:</span></span>

-   <span data-ttu-id="4fff2-131">Каждый элемент должен возвращать URL-адрес `link` или `enclosure` значение (или эквивалентное, например `media:content` ).</span><span class="sxs-lookup"><span data-stu-id="4fff2-131">Each item MUST return a URL `link` or `enclosure` value (or equivalent, such as `media:content`)</span></span>
-   <span data-ttu-id="4fff2-132">Не включайте Теги форматирования HTML в атрибут **Title** , или эти теги отображаются в заголовке и отображаются в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="4fff2-132">Do not include any HTML formatting tags in the **title** attribute, or those tags will appear in the title and be displayed in Windows Explorer.</span></span>
-   <span data-ttu-id="4fff2-133">Для элемента **Description** :</span><span class="sxs-lookup"><span data-stu-id="4fff2-133">For the **description** element:</span></span>
    -   <span data-ttu-id="4fff2-134">Отображение достаточной информации, чтобы пользователь знал, почему этот результат может быть релевантным.</span><span class="sxs-lookup"><span data-stu-id="4fff2-134">Show enough information so that the user knows why this result might be relevant.</span></span>
    -   <span data-ttu-id="4fff2-135">Не включайте форматирование HTML.</span><span class="sxs-lookup"><span data-stu-id="4fff2-135">Do not include HTML formatting.</span></span> <span data-ttu-id="4fff2-136">Поставщик [OpenSearch](https://github.com/dewitt/opensearch) удаляет форматирование, что может привести к нежелательным результатам для описания.</span><span class="sxs-lookup"><span data-stu-id="4fff2-136">The [OpenSearch](https://github.com/dewitt/opensearch) provider removes the formatting, which might result in less than desirable results for your description.</span></span>
    -   <span data-ttu-id="4fff2-137">Не включайте метаданные, которые уже предоставлены в других элементах, такие как имя файла, размер, Дата изменения и т. д., так как проводник уже отображает метаданные.</span><span class="sxs-lookup"><span data-stu-id="4fff2-137">Do not include metadata that is already provided in other elements, such as enclosure file name, size, modified date, and so forth, because Windows Explorer already displays the metadata.</span></span> <span data-ttu-id="4fff2-138">Его отображение в элементе **Description** будет избыточным.</span><span class="sxs-lookup"><span data-stu-id="4fff2-138">Displaying it in the **description** element would be redundant.</span></span>
-   <span data-ttu-id="4fff2-139">Для URL-адресов корпуса или содержимого:</span><span class="sxs-lookup"><span data-stu-id="4fff2-139">For enclosure or content URLs:</span></span>
    -   <span data-ttu-id="4fff2-140">Укажите атрибут Type в качестве допустимого типа MIME.</span><span class="sxs-lookup"><span data-stu-id="4fff2-140">Specify the type attribute as a valid MIME type.</span></span>
    -   <span data-ttu-id="4fff2-141">Укажите размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="4fff2-141">Specify the file size in bytes.</span></span>
-   <span data-ttu-id="4fff2-142">Если вы реализуете вывод RSS в среде .NET с помощью `DateTime` , протестируйте веб-канал в Microsoft Internet Explorer, чтобы проверить, является ли он допустимым перед развертыванием в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="4fff2-142">If you are implementing RSS output in .NET using `DateTime`, test your feed in Microsoft Internet Explorer to see if it is valid before deploying it to Windows Explorer.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4fff2-143">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4fff2-143">Additional Resources</span></span>

<span data-ttu-id="4fff2-144">Дополнительные сведения о реализации Федерации поиска в удаленных хранилищах данных с помощью технологий OpenSearch в Windows 7 и более поздних версиях см. в разделе "дополнительные ресурсы" в [Федеративной функции поиска в Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4fff2-144">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fff2-145">См. также</span><span class="sxs-lookup"><span data-stu-id="4fff2-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fff2-146">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="4fff2-146">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="4fff2-147">начало работы с федеративными поиском в Windows</span><span class="sxs-lookup"><span data-stu-id="4fff2-147">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="4fff2-148">Подключение веб-службы в Федеративной службе поиска Windows</span><span class="sxs-lookup"><span data-stu-id="4fff2-148">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="4fff2-149">Включение хранилища данных в федеративный поиск Windows</span><span class="sxs-lookup"><span data-stu-id="4fff2-149">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="4fff2-150">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="4fff2-150">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="4fff2-151">Развертывание соединителей поиска в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="4fff2-151">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> <dt>

[<span data-ttu-id="4fff2-152">Расширение индекса</span><span class="sxs-lookup"><span data-stu-id="4fff2-152">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
