---
description: Служба однорангового распространения (Майкрософт) поддерживает функции как для ролей потребителя, так и для сценариев роли издателя.
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: Функции API однорангового распределения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a594313300c6bf39a2ea4f08efba89d1ed757ba4b8a50eda074466b94433e1e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612325"
---
# <a name="peer-distribution-api-functions"></a>Функции API однорангового распределения

Служба однорангового распространения (Майкрософт) поддерживает функции как для ролей потребителя, так и для сценариев роли издателя.

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>Следующие функции являются общими в сценариях "клиент" и "сервер".



| Общие функции                                                                                       | Описание                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**пирдистстартуп**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | Создает новый экземпляр **\_ \_ обработчика для экземпляра** , который должен быть передан всем остальным интерфейсам API распространения Peer. |
| [**пирдистшутдовн**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | Высвобождает ресурсы, выделенные вызовом метода [**пирдистстартуп**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup).                         |
| [**пирдистжетстатус**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | Возвращает текущее состояние службы распространения Peer.                                                        |
| [**пирдистжетстатусекс**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | Возвращает текущее состояние и возможности службы распространения Peer.                                   |
| [**пирдистжетоверлаппедресулт**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | Возвращает результаты асинхронных операций.                                                               |
| [**пирдистрегистерфорстатусчанженотификатион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | Запрашивает уведомление вызывающей стороны службы распространения однорангового узла при изменении состояния.                      |
| [**пирдистрегистерфорстатусчанженотификатионекс**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | Запрашивает уведомление вызывающей стороны службы распространения однорангового узла при изменении состояния.                      |
| [**пирдистунрегистерфорстатусчанженотификатион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | Отменяет регистрацию уведомления об изменении состояния для сеанса, связанного с заданным обработчиком.                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>Следующие функции поддерживаются только в сценариях "клиент".



| Функции клиента                                                                             | Описание                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**пирдистклиентопенконтент**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | Открывает и возвращает **\_ \_ маркер содержимого** для ссылки на это содержимое.                                                                                                                                                                                                                                                                     |
| [**пирдистклиентклосеконтент**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | Закрывает **\_ \_ обработчик содержимого для объекта**,                                                                                                                                                                                                                                                                                                        |
| [**пирдистклиентжетинформатионбихандле**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | Извлекает дополнительные сведения из службы распространения Peer для определенного обработчика содержимого.                                                                                                                                                                                                                                               |
| [**пирдистклиентаддконтентинформатион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | Добавляет сведения о содержимом, которое затем связывается с **\_ \_ обработчиком содержимого**, **\_ \_ Обработчик содержимого** , связанный с данными, может быть связан с любым содержимым.                                                                                                                                                                        |
| [**пирдистклиенткомплетеконтентинформатион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | Указывает конец сведений о содержимом.                                                                                                                                                                                                                                                                                                    |
| [**пирдистклиентадддата**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | Используется для передачи содержимого в локальный кэш. Обычно это делается, когда данные не удалось найти в локальной сети, как указано в случае завершения [**пирдистклиентблоккреад**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) или [**пирдистклиентстреамреад**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) с **\_ истечением времени ожидания ошибки** или **\_ ошибки \_ \_**. |
| [**пирдистклиентблоккреад**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | Предоставляет произвольный доступ к потоку содержимого.                                                                                                                                                                                                                                                                                                    |
| [**пирдистклиентстреамреад**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | Предоставляет последовательный доступ к потоку содержимого.                                                                                                                                                                                                                                                                                                |
| [**пирдистклиентфлушконтент**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | Удаляет содержимое, которое ранее было добавлено в локальную систему распространения одноранговой сети.                                                                                                                                                                                                                                                            |
| [**пирдистклиентканцеласинкоператион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | Отменяет асинхронную операцию, связанную с [ПЕРЕкрывающейся](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) структурой, и маркер содержимого, возвращенный [**пирдистклиентопенконтент**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>Следующие функции поддерживаются только в сценариях "сервер".



| Функции сервера                                                                             | Описание                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**пирдистсерверпублишстреам**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | Создает **\_ \_ обработчик потока** , который можно использовать с [**пирдистсерверпублишаддтостреам**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream) для создания сведений о содержимом для потока содержимого. |
| [**пирдистсерверпублишаддтостреам**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | Добавляет данные в поток, на который ссылается handle Stream.                                                                                                                                  |
| [**пирдистсерверпублишкомплетестреам**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | Вызывается для указания на то, что все данные были добавлены в поток.                                                                                                                                     |
| [**пирдистсерверклосестреамхандле**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | Закрывает обработчик потока.                                                                                                                                                                          |
| [**пирдистсерверунпублиш**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Отменяет публикацию ранее опубликованного содержимого в службе однорангового распространения.                                                                                                                         |
| [**пирдистсерверопенконтентинформатион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | Открывает для опубликованного содержимого **\_ \_ рукоятку контентинфо** .                                                                                                                                   |
| [**пирдистсерверопенконтентинформатионекс**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | Открывает для опубликованного содержимого **\_ \_ рукоятку контентинфо** .                                                                                                                                   |
| [**пирдистсерверретриевеконтентинформатион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | Извлекает сведения о содержимом, связанном с опубликованным содержимым.                                                                                                                               |
| [**пирдистсерверклосеконтентинформатион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | Для этого **\_ \_Обработчик контентинфо** , Открытый с помощью [**пирдистсерверопенконтентинформатион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation).                                                                  |
| [**пирдистсерверканцеласинкоператион**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | Отменяет асинхронную операцию, связанную с идентификатором содержимого и структурой [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .                                             |



 

 

 
