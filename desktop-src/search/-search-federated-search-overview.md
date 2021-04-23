---
description: Поддержка интеграции поиска в Windows 7 с удаленными хранилищами данных с помощью технологий OpenSearch позволяет пользователям получать доступ к удаленным данным и взаимодействовать с ними в проводнике Windows.
ms.assetid: 2014b7ac-4885-4f17-b6d4-5fd95872ed59
title: Федеративный поиск в Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d7718bb5215072ceeb8786f5728017ed329e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497079"
---
# <a name="federated-search-in-windows"></a><span data-ttu-id="3aff4-103">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="3aff4-103">Federated Search in Windows</span></span>

<span data-ttu-id="3aff4-104">Поддержка интеграции поиска в Windows 7 с удаленными хранилищами данных с помощью технологий OpenSearch позволяет пользователям получать доступ к удаленным данным и взаимодействовать с ними в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="3aff4-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span>

<span data-ttu-id="3aff4-105">В следующем списке разделов описывается создание веб-хранилища данных, в котором можно выполнять поиск с помощью федеративного поиска Windows, а также возможность многофункциональной интеграции удаленных источников данных с проводником Windows без необходимости писать или развертывать код на стороне клиента Windows.</span><span class="sxs-lookup"><span data-stu-id="3aff4-105">The following list of topics describe how you can build a web-based data store that can be searched using Windows federated search, and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

-   [<span data-ttu-id="3aff4-106">начало работы с федеративными поиском в Windows</span><span class="sxs-lookup"><span data-stu-id="3aff4-106">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
-   [<span data-ttu-id="3aff4-107">Подключение веб-службы в Федеративной службе поиска Windows</span><span class="sxs-lookup"><span data-stu-id="3aff4-107">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
-   [<span data-ttu-id="3aff4-108">Включение хранилища данных в федеративный поиск Windows</span><span class="sxs-lookup"><span data-stu-id="3aff4-108">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
-   [<span data-ttu-id="3aff4-109">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="3aff4-109">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
-   [<span data-ttu-id="3aff4-110">Следующие рекомендации по использованию федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="3aff4-110">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
-   [<span data-ttu-id="3aff4-111">Развертывание соединителей поиска в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="3aff4-111">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
-   [<span data-ttu-id="3aff4-112">Схема описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="3aff4-112">Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)

## <a name="additional-resources"></a><span data-ttu-id="3aff4-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3aff4-113">Additional Resources</span></span>

-   <span data-ttu-id="3aff4-114">Пример кода [OpenSearch](-search-sample-opensearch.md) демонстрирует создание федеративной службы поиска с помощью протокола [OpenSearch](https://github.com/dewitt/opensearch) и файла дескриптора OpenSearch (. OSDX-) (соединителя поиска).</span><span class="sxs-lookup"><span data-stu-id="3aff4-114">The [OpenSearch](-search-sample-opensearch.md) code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>
-   <span data-ttu-id="3aff4-115">Видеодемонстрацию создания веб-службы [OpenSearch](https://github.com/dewitt/opensearch) для базы данных SQL см. в статье [Windows 7: предоставление пользователям возможности поиска, визуализации и организации данных с помощью библиотек и обозревателя](https://channel9.msdn.com/pdc2008/PC16/).</span><span class="sxs-lookup"><span data-stu-id="3aff4-115">For a video demonstration of creating an [OpenSearch](https://github.com/dewitt/opensearch) web service for a SQL database, see [Windows 7: Empower Users to Find, Visualize and Organize their Data with Libraries and the Explorer](https://channel9.msdn.com/pdc2008/PC16/).</span></span>
-   <span data-ttu-id="3aff4-116">Если вы создаете поставщик [OpenSearch](https://github.com/dewitt/opensearch) на стороне клиента, см. следующие статьи:</span><span class="sxs-lookup"><span data-stu-id="3aff4-116">If you are writing a client-side [OpenSearch](https://github.com/dewitt/opensearch) provider, see:</span></span>
    -   <span data-ttu-id="3aff4-117">Дополнительные сведения о подключении к поставщику на стороне клиента с помощью протоколов или интерфейсов API для собственного хранилища данных см. в статье [руководство по OpenSearch](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) .</span><span class="sxs-lookup"><span data-stu-id="3aff4-117">The [OpenSearch Developer How To Guide](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) for more information on connecting to a client-side provider by using a proprietary data store's protocols or APIs.</span></span>
    -   <span data-ttu-id="3aff4-118">Обзор документации по схеме [описания соединителя поиска](search-sconn-desc-schema-entry.md) (. сеарчконнектор-MS).</span><span class="sxs-lookup"><span data-stu-id="3aff4-118">The [Overview of the Search Connector Description Schema](search-sconn-desc-schema-entry.md) (.searchconnector-ms) schema documentation.</span></span>
-   <span data-ttu-id="3aff4-119">Ниже приведен веб-сайт [центра загрузки Майкрософт](https://www.microsoft.com/DOWNLOADS/en/default.aspx) со сведениями о загружаемом ресурсе: образец сервера search Server 2008 пример: федеративный соединитель поиска.</span><span class="sxs-lookup"><span data-stu-id="3aff4-119">See the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) website for the following downloadable resource: Search Server 2008 Sample: Federated Search Connector Sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3aff4-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3aff4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aff4-121">Обзор Windows Search</span><span class="sxs-lookup"><span data-stu-id="3aff4-121">Windows Search Overview</span></span>](-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="3aff4-122">Руководством разработчика Windows Search</span><span class="sxs-lookup"><span data-stu-id="3aff4-122">Windows Search Developer's Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="3aff4-123">Справочник по поиску Windows</span><span class="sxs-lookup"><span data-stu-id="3aff4-123">Windows Search Reference</span></span>](-search-reference-entry-page.md)
</dt> <dt>

[<span data-ttu-id="3aff4-124">Примеры кода для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="3aff4-124">Windows Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

[<span data-ttu-id="3aff4-125">Связанные технологии поиска</span><span class="sxs-lookup"><span data-stu-id="3aff4-125">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)
</dt> <dt>

[<span data-ttu-id="3aff4-126">Глоссарий поиска Windows</span><span class="sxs-lookup"><span data-stu-id="3aff4-126">Windows Search Glossary</span></span>](search-glossary.md)
</dt> </dl>

 

 



