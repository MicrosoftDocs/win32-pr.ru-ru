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
# <a name="federated-search-in-windows"></a>Федеративный поиск в Windows

Поддержка интеграции поиска в Windows 7 с удаленными хранилищами данных с помощью технологий OpenSearch позволяет пользователям получать доступ к удаленным данным и взаимодействовать с ними в проводнике Windows.

В следующем списке разделов описывается создание веб-хранилища данных, в котором можно выполнять поиск с помощью федеративного поиска Windows, а также возможность многофункциональной интеграции удаленных источников данных с проводником Windows без необходимости писать или развертывать код на стороне клиента Windows.

-   [начало работы с федеративными поиском в Windows](getting-started-with-federated-search-in-windows.md)
-   [Подключение веб-службы в Федеративной службе поиска Windows](-search-federated-search-web-service.md)
-   [Включение хранилища данных в федеративный поиск Windows](-search-federated-search-data-store.md)
-   [Создание файла описания OpenSearch в федеративного поиска Windows](-search-federated-search-osdx-file.md)
-   [Следующие рекомендации по использованию федеративного поиска Windows](-search-fedsearch-best.md)
-   [Развертывание соединителей поиска в федеративного поиска Windows](-search-federated-search-deploying.md)
-   [Схема описания соединителя поиска](search-sconn-desc-schema-entry.md)

## <a name="additional-resources"></a>Дополнительные ресурсы

-   Пример кода [OpenSearch](-search-sample-opensearch.md) демонстрирует создание федеративной службы поиска с помощью протокола [OpenSearch](https://github.com/dewitt/opensearch) и файла дескриптора OpenSearch (. OSDX-) (соединителя поиска).
-   Видеодемонстрацию создания веб-службы [OpenSearch](https://github.com/dewitt/opensearch) для базы данных SQL см. в статье [Windows 7: предоставление пользователям возможности поиска, визуализации и организации данных с помощью библиотек и обозревателя](https://channel9.msdn.com/pdc2008/PC16/).
-   Если вы создаете поставщик [OpenSearch](https://github.com/dewitt/opensearch) на стороне клиента, см. следующие статьи:
    -   Дополнительные сведения о подключении к поставщику на стороне клиента с помощью протоколов или интерфейсов API для собственного хранилища данных см. в статье [руководство по OpenSearch](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) .
    -   Обзор документации по схеме [описания соединителя поиска](search-sconn-desc-schema-entry.md) (. сеарчконнектор-MS).
-   Ниже приведен веб-сайт [центра загрузки Майкрософт](https://www.microsoft.com/DOWNLOADS/en/default.aspx) со сведениями о загружаемом ресурсе: образец сервера search Server 2008 пример: федеративный соединитель поиска.

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

[Связанные технологии поиска](-search-3x-wds-sampleentry.md)
</dt> <dt>

[Глоссарий поиска Windows](search-glossary.md)
</dt> </dl>

 

 



