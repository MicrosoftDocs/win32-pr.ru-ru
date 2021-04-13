---
description: 'Поиск Windows позволяет управлять индексом Windows Search с помощью трех основных компонентов: Диспетчер поиска, диспетчер каталогов и Диспетчер области обхода содержимого.'
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Интерфейсы для управления индексом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7191fbdb4e83c9e3f1460b96123901b5f277b41a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262930"
---
# <a name="interfaces-for-managing-the-index"></a>Интерфейсы для управления индексом

Поиск Windows позволяет управлять индексом Windows Search с помощью трех основных компонентов: Диспетчер поиска, диспетчер каталогов и Диспетчер области обхода содержимого. Некоторые из этих интерфейсов управления могут использоваться с правами обычного пользователя, но для тех, кто изменяет состояние индекса, требуются права администратора.

## <a name="about-the-interfaces-for-managing-the-index"></a>Сведения об интерфейсах для управления индексом

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Компонент</th>
<th>Интерфейсы</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Диспетчер поиска</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">исеарчманажер</a></td>
<td>Предоставляет методы для получения и настройки сведений о поиске Windows:
<ul>
<li>Получение экземпляра диспетчера каталогов для определенного каталога.</li>
<li>Получение или Установка сведений о прокси-сервере.</li>
<li>Получение сведений о версии системы поиска Windows.</li>
</ul>
Дополнительные сведения см. <a href="-search-3x-wds-mngidx-searchmanager.md">в разделе Использование диспетчера поиска</a>.<br/></td>
</tr>
<tr class="even">
<td>Диспетчер каталога</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">исеарчкаталогманажер</a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br/></td>
<td>Предоставляет методы для управления отдельным каталогом поиска, например, что вызывает повторную индексацию или настройку времени ожидания. Этот интерфейс управляет каталогом в четырех областях:
<ul>
<li>Содержимое каталога — гарантируется, что новые данные индексируются и что другие приложения и компоненты работают надлежащим образом путем принудительной повторной индексации всего или части каталога или путем сброса всего каталога.</li>
<li>Свойства каталога — задание свойств, определяющих, как каталог управляет временем ожидания при подключении к обработчикам протоколов и как диакритические знаки обрабатываются при поиске.</li>
<li>Состояние каталога — получение сведений о каталоге, включая состояние, размер и текущее состояние действия.</li>
<li>Доступ к другим интерфейсам — получение других интерфейсов, связанных с поиском, требуемых диспетчером области сканирования, уведомлениями об изменении данных и интерфейсом <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>исеарчкуерихелпер</strong></a> .</li>
</ul>
Дополнительные сведения см. <a href="-search-3x-wds-mngidx-catalog-manager.md">в разделе Использование диспетчера каталогов</a>.<br/></td>
</tr>
<tr class="odd">
<td>Диспетчер области обхода содержимого</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>иенумсеарчрутс</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">иенумсеарчскоперулес</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>исеарчкравлскопеманажер</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>исеарчрут</strong></a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>исеарчскоперуле</strong></a><br/> <a href="/windows/desktop/search/-search-isearchitem">исеарчитем</a><br/></td>
<td>Предоставляет методы для информирования поисковой системы о контейнерах для обхода или просмотра, а также элементов в этих контейнерах для включения или исключения в индексе. Можно также запросить Диспетчер области сканирования, чтобы узнать, находится ли конкретный URL-адрес в области сканирования. Дополнительные сведения см. <a href="-search-3x-wds-extidx-csm.md">в разделе Использование диспетчера области сканирования</a>.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>См. также

[Управление индексом](-search-3x-wds-mngidx-overview.md)

[Использование диспетчера поиска](-search-3x-wds-mngidx-searchmanager.md)

[Использование диспетчера каталогов](-search-3x-wds-mngidx-catalog-manager.md)

[Использование диспетчера области сканирования](-search-3x-wds-extidx-csm.md)
