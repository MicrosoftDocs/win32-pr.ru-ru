---
description: узнайте, как Windows поиск позволяет управлять Windows индексом поиска с помощью диспетчера поиска, диспетчера каталогов и диспетчера области обхода содержимого.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Интерфейсы для управления индексом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505752cc496d55057eece87bd673b31a323c6597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476800"
---
# <a name="interfaces-for-managing-the-index"></a>Интерфейсы для управления индексом

Windows поиск позволяет управлять индексом поиска Windows с помощью трех основных компонентов: диспетчер поиска, диспетчер каталогов и диспетчер области обхода содержимого. Некоторые из этих интерфейсов управления могут использоваться с правами обычного пользователя, но для тех, кто изменяет состояние индекса, требуются права администратора.

## <a name="about-the-interfaces-for-managing-the-index"></a>Сведения об интерфейсах для управления индексом


| Компонент | Интерфейсы | Описание | 
|-----------|------------|-------------|
| Диспетчер поиска | <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">исеарчманажер</a> | предоставляет методы для получения и настройки сведений о Windowsном поиске:<ul><li>Получение экземпляра диспетчера каталогов для определенного каталога.</li><li>Получение или Установка сведений о прокси-сервере.</li><li>получение сведений о версии поисковой системы Windows.</li></ul>Дополнительные сведения см. <a href="-search-3x-wds-mngidx-searchmanager.md">в разделе Использование диспетчера поиска</a>.<br /> | 
| Диспетчер каталога | <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">исеарчкаталогманажер</a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br /> | Предоставляет методы для управления отдельным каталогом поиска, например, что вызывает повторную индексацию или настройку времени ожидания. Этот интерфейс управляет каталогом в четырех областях:<ul><li>Содержимое каталога — гарантируется, что новые данные индексируются и что другие приложения и компоненты работают надлежащим образом путем принудительной повторной индексации всего или части каталога или путем сброса всего каталога.</li><li>Свойства каталога — задание свойств, определяющих, как каталог управляет временем ожидания при подключении к обработчикам протоколов и как диакритические знаки обрабатываются при поиске.</li><li>Состояние каталога — получение сведений о каталоге, включая состояние, размер и текущее состояние действия.</li><li>Доступ к другим интерфейсам — получение других интерфейсов, связанных с поиском, требуемых диспетчером области сканирования, уведомлениями об изменении данных и интерфейсом <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>исеарчкуерихелпер</strong></a> .</li></ul>Дополнительные сведения см. <a href="-search-3x-wds-mngidx-catalog-manager.md">в разделе Использование диспетчера каталогов</a>.<br /> | 
| Диспетчер области обхода содержимого | <a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>иенумсеарчрутс</strong></a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">иенумсеарчскоперулес</a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>исеарчкравлскопеманажер</strong></a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>исеарчрут</strong></a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>исеарчскоперуле</strong></a><br /><a href="/windows/desktop/search/-search-isearchitem">исеарчитем</a><br /> | Предоставляет методы для информирования поисковой системы о контейнерах для обхода или просмотра, а также элементов в этих контейнерах для включения или исключения в индексе. Можно также запросить Диспетчер области сканирования, чтобы узнать, находится ли конкретный URL-адрес в области сканирования. Дополнительные сведения см. <a href="-search-3x-wds-extidx-csm.md">в разделе Использование диспетчера области сканирования</a>.<br /> | 


## <a name="related-topics"></a>Связанные темы

[Управление индексом](-search-3x-wds-mngidx-overview.md)

[Использование диспетчера поиска](-search-3x-wds-mngidx-searchmanager.md)

[Использование диспетчера каталогов](-search-3x-wds-mngidx-catalog-manager.md)

[Использование диспетчера области сканирования](-search-3x-wds-extidx-csm.md)
