---
description: В этом разделе описываются технологии, связанные с поиском Windows.
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: Связанные технологии поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f8a03738958e19712ff8cc4566e4b7f7396ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144158"
---
# <a name="related-search-technologies"></a>Связанные технологии поиска

В этом разделе описываются технологии, связанные с [поиском Windows](-search-3x-wds-overview.md).

Этот раздел организован следующим образом:

-   [Поиск в корпоративной среде](#enterprise-search)
    -   [Поиск в SharePoint Enterprise](#sharepoint-enterprise-search)
-   [Windows Desktop Search 2. x](#windows-desktop-search-2x)
-   [Пакет Platform SDK: служба индексирования](#platform-sdk-indexing-service)
-   [См. также](#related-topics)

## <a name="enterprise-search"></a>Поиск в корпоративной среде

Общие сведения о технических ресурсах для [поиска в корпоративной среде корпорации Майкрософт](https://www.microsoft.com/enterprisesearch/en/us/default.aspx)см. в следующих статьях:

-   [Центр ресурсов по поиску в корпоративной среде](https://developer.microsoft.com/office/docs)
-   [Блог Microsoft Enterprise Search](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a>Поиск в SharePoint Enterprise

SharePoint Foundation 2010 предоставляет [запросы из кода на стороне сервера](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) и [запросы из клиентского кода](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14)). Дополнительные сведения о запросах, поиске нового содержимого и повышении релевантности в SharePoint Server 2010 Enterprise Search см. в статье [основные принципы корпоративного поиска](/previous-versions/office/ee554857(v=office.14)).

Поиск Windows 7 поддерживает федерацию службы поиска для удаленных хранилищ данных с помощью технологий OpenSearch, которые позволяют пользователям получать доступ к удаленным данным и взаимодействовать с ними в проводнике Windows. SharePoint Search Server 2008 и MOSS 2007 с пакетом обновления 2 (SP2) также поддерживают федеративный поиск удаленных серверов с помощью OpenSearch. Сведения о развертывании сервера Search Server 2008 с помощью Office SharePoint Server 2007 см. в статье [федеративный поисковый \[ сервер search Server 2008 \] ](/previous-versions/office/bb931109(v=office.14)). Сведения об Аспектном поиске в MOSS, в котором результаты поиска перечисляются по категориям, см. в разделе [CodePlex](https://www.codeplex.com/FacetedSearch).

Обработчики протоколов поиска Windows используют спецификации проектирования, аналогичные SharePoint Server, и часто взаимозаменяемы. Таким образом, если пользователям требуется искать устаревшие базы данных, хранилища электронной почты или другие структуры данных, которые не поддерживаются службой поиска Windows, необходимо сначала определить, существует ли обработчик протокола для этого хранилища данных, возможно, для использования с другим приложением, например SharePoint Server. В этом случае можно установить обработчик протокола в системе.

## <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2. x

Использование и разработка версий 2. x Microsoft Windows Desktop Search (WDS) настоятельно не рекомендуется. Вместо использования [Windows Desktop Search 2. x](../lwef/-search-2x-wds-overview.md)используйте Windows [Search](-search-3x-wds-overview.md) и [API Windows Search](-search-reference-entry-page.md).

## <a name="platform-sdk-indexing-service"></a>Пакет Platform SDK: служба индексирования

[Platform SDK: служба индексирования](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) устарела в Windows XP. Вместо этого используйте [Windows Search](-search-3x-wds-overview.md) и [API Windows Search](-search-reference-entry-page.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обзор Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Руководством разработчика Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Справочник по поиску Windows](-search-reference-entry-page.md)
</dt> <dt>

[Примеры кода для поиска Windows](-search-samples-ovw.md)
</dt> <dt>

[Федеративный поиск в Windows](-search-federated-search-overview.md)
</dt> <dt>

[Глоссарий поиска Windows](search-glossary.md)
</dt> </dl>

 

 
