---
description: В этом разделе объясняется, как пользователь регистрирует новое удаленное хранилище данных с помощью федеративного поиска, открыв файл описания OpenSearch (. OSDX-), как развернуть OSDX--файл и как отслеживание использования службы OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Развертывание соединителей поиска в федеративного поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497082"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a><span data-ttu-id="3fee2-103">Развертывание соединителей поиска в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="3fee2-103">Deploying Search Connectors in Windows Federated Search</span></span>

<span data-ttu-id="3fee2-104">В этом разделе объясняется, как пользователь регистрирует новое удаленное хранилище данных с помощью федеративного поиска, открыв файл описания OpenSearch (. OSDX-), как развернуть OSDX--файл и как отслеживание использования службы [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="3fee2-104">This topic explains how a user registers a new remote data store with federated search by opening an OpenSearch Description (.osdx) file, how to deploy an .osdx file, and how to track usage of your [OpenSearch](https://github.com/dewitt/opensearch) service.</span></span>

<span data-ttu-id="3fee2-105">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3fee2-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="3fee2-106">Файл. сеарчконнектор-MS (поисковый соединитель)</span><span class="sxs-lookup"><span data-stu-id="3fee2-106">The .searchconnector-ms (Search Connector) File</span></span>](#the-searchconnector-ms-search-connector-file)
-   [<span data-ttu-id="3fee2-107">Методы развертывания</span><span class="sxs-lookup"><span data-stu-id="3fee2-107">Deployment Methods</span></span>](#deployment-methods)
    -   [<span data-ttu-id="3fee2-108">Развертывание по запросу</span><span class="sxs-lookup"><span data-stu-id="3fee2-108">Pull Deployment</span></span>](#pull-deployment)
    -   [<span data-ttu-id="3fee2-109">Принудительное развертывание</span><span class="sxs-lookup"><span data-stu-id="3fee2-109">Push Deployment</span></span>](#push-deployment)
-   [<span data-ttu-id="3fee2-110">Отслеживание использования</span><span class="sxs-lookup"><span data-stu-id="3fee2-110">Tracking Usage</span></span>](#tracking-usage)
-   [<span data-ttu-id="3fee2-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3fee2-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="3fee2-112">См. также</span><span class="sxs-lookup"><span data-stu-id="3fee2-112">Related topics</span></span>](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a><span data-ttu-id="3fee2-113">Файл. сеарчконнектор-MS (поисковый соединитель)</span><span class="sxs-lookup"><span data-stu-id="3fee2-113">The .searchconnector-ms (Search Connector) File</span></span>

<span data-ttu-id="3fee2-114">Просто откройте файл. OSDX-, который описывает, как подключиться к веб-службе и как сопоставлять любые настраиваемые элементы в RSS или Atom XML, регистрирует новое удаленное хранилище данных с помощью федеративного поиска.</span><span class="sxs-lookup"><span data-stu-id="3fee2-114">Merely opening the .osdx file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML registers your new remote data store with federated search.</span></span> <span data-ttu-id="3fee2-115">Хранилище данных, в котором уже есть веб-служба [OpenSearch](https://github.com/dewitt/opensearch) , совместимая с федеративным поиском, может быть добавлена в проводник Windows, когда пользователь открывает файл OSDX-.</span><span class="sxs-lookup"><span data-stu-id="3fee2-115">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with federated search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

<span data-ttu-id="3fee2-116">После того как вы предоставили пользователю. OSDX-, и пользователь откроет OSDX-файл, происходят следующие события.</span><span class="sxs-lookup"><span data-stu-id="3fee2-116">After you have given the .osdx to your user and the user opens the .osdx file, the following events occur.</span></span>

1.  <span data-ttu-id="3fee2-117">Файл. сеарчконнектор-MS создается в папке **поиска Windows** (% UserProfile%/сеарчес).</span><span class="sxs-lookup"><span data-stu-id="3fee2-117">A .searchconnector-ms file is created in the **Windows Searches** folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="3fee2-118">Ярлык для файла. сеарчконнектор-MS создается в папке **ссылок** (% UserProfile%/Линкс).</span><span class="sxs-lookup"><span data-stu-id="3fee2-118">A shortcut to the .searchconnector-ms file is created in the **Links** folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="3fee2-119">Ярлык отображается в области **"Избранное"** навигации проводника Windows, позволяя пользователю перейти в новое хранилище данных и запросить веб-службу.</span><span class="sxs-lookup"><span data-stu-id="3fee2-119">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store and query the web service.</span></span>

## <a name="deployment-methods"></a><span data-ttu-id="3fee2-120">Методы развертывания</span><span class="sxs-lookup"><span data-stu-id="3fee2-120">Deployment Methods</span></span>

<span data-ttu-id="3fee2-121">Существует два способа развертывания соединителей поиска, извлечения и принудительного развертывания.</span><span class="sxs-lookup"><span data-stu-id="3fee2-121">There are two ways to deploy search connectors, pull deployment and push deployment.</span></span>

### <a name="pull-deployment"></a><span data-ttu-id="3fee2-122">Развертывание по запросу</span><span class="sxs-lookup"><span data-stu-id="3fee2-122">Pull Deployment</span></span>

<span data-ttu-id="3fee2-123">Развертывание по запросу описывает любой тип развертывания, в котором конечный пользователь выполняет инициативу по установке соединителей поиска.</span><span class="sxs-lookup"><span data-stu-id="3fee2-123">Pull deployment describes any type of deployment in which the end user takes the initiative to install the search connectors.</span></span> <span data-ttu-id="3fee2-124">Распространенные методы развертывания по запросу:</span><span class="sxs-lookup"><span data-stu-id="3fee2-124">Common methods of pull deployment are:</span></span>

-   <span data-ttu-id="3fee2-125">Присоединение файла. OSDX-в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3fee2-125">Attaching the .osdx file in an email.</span></span>
-   <span data-ttu-id="3fee2-126">Публикация файла на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="3fee2-126">Posting the file on a webpage.</span></span>
-   <span data-ttu-id="3fee2-127">Предоставление динамической ссылки на сайт интрасети; Например, одна из них создает пользовательские файлы. OSDX-на основе выбора пользователя или текущей области в пределах сайта.</span><span class="sxs-lookup"><span data-stu-id="3fee2-127">Providing a dynamic link on your intranet site; for example, one that generates custom .osdx files based on user choices or the current scope within the site.</span></span>

<span data-ttu-id="3fee2-128">Чтобы файл загружался, когда пользователь щелкает ссылку в браузере, веб-сервер, на котором размещена веб-служба, должен быть настроен для доставки OSDX-в виде файла.</span><span class="sxs-lookup"><span data-stu-id="3fee2-128">For the file to be downloaded when the user clicks the link in their browser, the web server hosting the web service must be configured to deliver the .osdx as a file.</span></span> <span data-ttu-id="3fee2-129">Поэтому необходимо настроить типы MIME на веб-сервере, чтобы обрабатывать файлы OSDX-как `"application/opensearchdescription+xml"` .</span><span class="sxs-lookup"><span data-stu-id="3fee2-129">Hence, you must configure the MIME Types on the web server to treat .osdx files as `"application/opensearchdescription+xml"`.</span></span> <span data-ttu-id="3fee2-130">При необходимости можно использовать значок, предоставленный корпорацией Майкрософт для обнаружения соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="3fee2-130">Optionally, you can use the icon supplied by Microsoft to identify search connector link.</span></span>

### <a name="push-deployment"></a><span data-ttu-id="3fee2-131">Принудительное развертывание</span><span class="sxs-lookup"><span data-stu-id="3fee2-131">Push Deployment</span></span>

<span data-ttu-id="3fee2-132">Принудительное развертывание описывает любой тип развертывания, который не зависит от инициативы пользователя по установке соединителей поиска.</span><span class="sxs-lookup"><span data-stu-id="3fee2-132">Push deployment describes any type of deployment that does not depend on user initiative to install the search connectors.</span></span> <span data-ttu-id="3fee2-133">Распространенные методы принудительного развертывания:</span><span class="sxs-lookup"><span data-stu-id="3fee2-133">Common methods of push deployment are:</span></span>

-   <span data-ttu-id="3fee2-134">Параметры групповая политика (GPP)</span><span class="sxs-lookup"><span data-stu-id="3fee2-134">Group Policy Preferences (GPP)</span></span>
-   <span data-ttu-id="3fee2-135">Сценарий входа</span><span class="sxs-lookup"><span data-stu-id="3fee2-135">Logon script</span></span>
-   <span data-ttu-id="3fee2-136">Перемещаемые профили</span><span class="sxs-lookup"><span data-stu-id="3fee2-136">Roaming profiles</span></span>
-   <span data-ttu-id="3fee2-137">Создание образов</span><span class="sxs-lookup"><span data-stu-id="3fee2-137">Imaging</span></span>

## <a name="tracking-usage"></a><span data-ttu-id="3fee2-138">Отслеживание использования</span><span class="sxs-lookup"><span data-stu-id="3fee2-138">Tracking Usage</span></span>

<span data-ttu-id="3fee2-139">Чтобы отвести журнал использования службы [OpenSearch](https://github.com/dewitt/opensearch) пользователями, выполняющими Поиск в проводнике Windows, отфильтруйте файлы журнала веб-сервера для этой строки агента пользователя: `Windows-Search+(Windows+NT+6.1)` .</span><span class="sxs-lookup"><span data-stu-id="3fee2-139">To track the usage of your [OpenSearch](https://github.com/dewitt/opensearch) service by users searching from Windows Explorer, filter your web server log files for this user agent string: `Windows-Search+(Windows+NT+6.1)`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3fee2-140">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3fee2-140">Additional Resources</span></span>

<span data-ttu-id="3fee2-141">Дополнительные сведения о реализации Федерации поиска в удаленных хранилищах данных с помощью технологий OpenSearch в Windows 7 и более поздних версиях см. в разделе "дополнительные ресурсы" в [Федеративной функции поиска в Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3fee2-141">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fee2-142">См. также</span><span class="sxs-lookup"><span data-stu-id="3fee2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fee2-143">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="3fee2-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="3fee2-144">начало работы с федеративными поиском в Windows</span><span class="sxs-lookup"><span data-stu-id="3fee2-144">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="3fee2-145">Подключение веб-службы в Федеративной службе поиска Windows</span><span class="sxs-lookup"><span data-stu-id="3fee2-145">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="3fee2-146">Включение хранилища данных в федеративный поиск Windows</span><span class="sxs-lookup"><span data-stu-id="3fee2-146">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="3fee2-147">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="3fee2-147">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="3fee2-148">Следующие рекомендации по использованию федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="3fee2-148">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> </dl>

 

 
