---
description: В этом разделе описываются шаги, связанные с подключением веб-службы между хранилищем данных и федеративным поиском Windows, а также отправкой запросов и возвратом результатов поиска в RSS или Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Подключение веб-службы в Федеративной службе поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144143"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a><span data-ttu-id="9920f-103">Подключение веб-службы в Федеративной службе поиска Windows</span><span class="sxs-lookup"><span data-stu-id="9920f-103">Connecting Your Web Service in Windows Federated Search</span></span>

<span data-ttu-id="9920f-104">В этом разделе описываются шаги, связанные с подключением веб-службы между хранилищем данных и федеративным поиском Windows, а также отправкой запросов и возвратом результатов поиска в RSS или Atom.</span><span class="sxs-lookup"><span data-stu-id="9920f-104">This topic describes the steps involved in connecting a web service between your data store and Windows Federated Search, and how to send queries and return search results in RSS or Atom.</span></span>

<span data-ttu-id="9920f-105">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9920f-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="9920f-106">Подключение веб-службы</span><span class="sxs-lookup"><span data-stu-id="9920f-106">Connect Your web Service</span></span>](#connect-your-web-service)
-   [<span data-ttu-id="9920f-107">Регистрация существующего удаленного хранилища данных</span><span class="sxs-lookup"><span data-stu-id="9920f-107">Register an Existing Remote Data Store</span></span>](#register-an-existing-remote-data-store)
-   [<span data-ttu-id="9920f-108">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9920f-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="9920f-109">См. также</span><span class="sxs-lookup"><span data-stu-id="9920f-109">Related topics</span></span>](#related-topics)

## <a name="connect-your-web-service"></a><span data-ttu-id="9920f-110">Подключение веб-службы</span><span class="sxs-lookup"><span data-stu-id="9920f-110">Connect Your web Service</span></span>

<span data-ttu-id="9920f-111">**Чтобы подключить веб-службу хранилища данных к федеративным поиску, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="9920f-111">**To connect the web service of your data store to federated search, perform the following steps:**</span></span>

1.  <span data-ttu-id="9920f-112">Создайте файл OSDX-.</span><span class="sxs-lookup"><span data-stu-id="9920f-112">Create an .osdx file.</span></span>
2.  <span data-ttu-id="9920f-113">Предоставьте OSDX-файл пользователям, чтобы они могли добавлять службу по запросу, открыв файл OSDX-.</span><span class="sxs-lookup"><span data-stu-id="9920f-113">Supply the .osdx file to users so that they can add the service on demand by opening the .osdx file.</span></span>
3.  <span data-ttu-id="9920f-114">Создание соединителя поиска и его активное развертывание на предприятии.</span><span class="sxs-lookup"><span data-stu-id="9920f-114">Generate a search connector and actively deploy it in your enterprise.</span></span>

## <a name="register-an-existing-remote-data-store"></a><span data-ttu-id="9920f-115">Регистрация существующего удаленного хранилища данных</span><span class="sxs-lookup"><span data-stu-id="9920f-115">Register an Existing Remote Data Store</span></span>

<span data-ttu-id="9920f-116">Пользователь регистрирует новое удаленное хранилище данных с помощью федеративного поиска Windows, открыв файл описания OpenSearch (. OSDX-).</span><span class="sxs-lookup"><span data-stu-id="9920f-116">A user registers a new remote data store with Windows Federated Search by opening an OpenSearch Description (.osdx) file.</span></span> <span data-ttu-id="9920f-117">Когда пользователь делает это, происходят следующие события:</span><span class="sxs-lookup"><span data-stu-id="9920f-117">When the user does so, the following events occur:</span></span>

1.  <span data-ttu-id="9920f-118">Файл. сеарчконнектор-MS (соединитель поиска) создается в папке поиска Windows (% UserProfile%/Сеарчес).</span><span class="sxs-lookup"><span data-stu-id="9920f-118">A .searchconnector-ms file (search connector) is created in the Windows Searches folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="9920f-119">Ярлык для файла. сеарчконнектор-MS создается в папке ссылок (% UserProfile%/Линкс).</span><span class="sxs-lookup"><span data-stu-id="9920f-119">A shortcut to the .searchconnector-ms file is created in the Links folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="9920f-120">Ярлык отображается в области **"Избранное"** навигации проводника Windows, позволяя пользователю перейти в новое хранилище данных и выполнить запрос к веб-службе.</span><span class="sxs-lookup"><span data-stu-id="9920f-120">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store, and query the web service.</span></span>

> [!Note]  
> <span data-ttu-id="9920f-121">Хранилище данных, в котором уже есть веб-служба [OpenSearch](https://github.com/dewitt/opensearch) , совместимая с федеративным поиском Windows, может быть добавлена в проводник Windows, когда пользователь открывает файл. OSDX-.</span><span class="sxs-lookup"><span data-stu-id="9920f-121">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with Windows Federated Search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="9920f-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9920f-122">Additional Resources</span></span>

<span data-ttu-id="9920f-123">Дополнительные сведения о реализации Федерации поиска в удаленных хранилищах данных с помощью технологий OpenSearch в Windows 7 и более поздних версиях см. в разделе "дополнительные ресурсы" в [Федеративной функции поиска в Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9920f-123">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9920f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="9920f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9920f-125">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="9920f-125">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="9920f-126">начало работы с федеративными поиском в Windows</span><span class="sxs-lookup"><span data-stu-id="9920f-126">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="9920f-127">Включение хранилища данных в федеративный поиск Windows</span><span class="sxs-lookup"><span data-stu-id="9920f-127">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="9920f-128">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="9920f-128">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="9920f-129">Следующие рекомендации по использованию федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="9920f-129">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="9920f-130">Развертывание соединителей поиска в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="9920f-130">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
