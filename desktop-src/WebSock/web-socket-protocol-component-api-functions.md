---
title: Функции API компонента протокола WebSocket
description: Эти функции определяются API компонента протокола WebSocket.
ms.assetid: B833D18D-286C-4D32-A9C7-D5D5806EC306
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d88a4ef8eb9caa0e409d0ded60b6dffd2717dc74d1b2cdddeb08ee6d9de08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330342"
---
# <a name="websocket-protocol-component-api-functions"></a>Функции API компонента протокола WebSocket

Эти функции определяются API компонента протокола WebSocket.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                             | Описание                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**вебсоккетаборсандле**](/windows/desktop/api/Websocket/nf-websocket-websocketaborthandle)<br/>                   | прерывает работу обработчика сеанса WebSocket, созданного с помощью [**вебсоккеткреатеклиенсандле**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) или [**вебсоккеткреатесерверхандле**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle).<br/>   |
| [**вебсоккетбегинклиенсандшаке**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginclienthandshake)<br/> | начинает подтверждение на стороне клиента.<br/>                                                                                                                                                                |
| [**вебсоккетбегинсерверхандшаке**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginserverhandshake)<br/> | начинает согласование на стороне сервера.<br/>                                                                                                                                                                |
| [**вебсоккеткомплетеактион**](/windows/desktop/api/Websocket/nf-websocket-websocketcompleteaction)<br/>             | завершает действие, запущенное [**вебсоккетжетактион**](/windows/desktop/api/websocket/nf-websocket-websocketgetaction).<br/>                                                                                                             |
| [**вебсоккеткреатеклиенсандле**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateclienthandle)<br/>     | создает обработчик сеанса WebSocket на стороне клиента.<br/>                                                                                                                                                  |
| [**вебсоккеткреатесерверхандле**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateserverhandle)<br/>     | создает обработчик сеанса WebSocket на стороне сервера.<br/>                                                                                                                                                  |
| [**вебсоккетделетехандле**](/windows/desktop/api/Websocket/nf-websocket-websocketdeletehandle)<br/>                 | Удаляет обработчик сеанса WebSocket, созданный с помощью [**вебсоккеткреатеклиенсандле**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) или [**вебсоккеткреатесерверхандле**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle).<br/>  |
| [**вебсоккетендклиенсандшаке**](/windows/desktop/api/Websocket/nf-websocket-websocketendclienthandshake)<br/>     | завершает подтверждение на стороне клиента.<br/>                                                                                                                                                             |
| [**вебсоккетендсерверхандшаке**](/windows/desktop/api/Websocket/nf-websocket-websocketendserverhandshake)<br/>     | завершает согласование на стороне сервера.<br/>                                                                                                                                                             |
| [**вебсоккетжетактион**](/windows/desktop/api/Websocket/nf-websocket-websocketgetaction)<br/>                       | Возвращает действие из вызова [**вебсоккетсенд**](/windows/desktop/api/websocket/nf-websocket-websocketsend), [**вебсоккетрецеиве**](/windows/desktop/api/websocket/nf-websocket-websocketreceive) или [**вебсоккеткомплетеактион**](/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction).<br/> |
| [**вебсоккетжетглобалпроперти**](/windows/desktop/api/Websocket/nf-websocket-websocketgetglobalproperty)<br/>       | Возвращает одно свойство WebSocket.<br/>                                                                                                                                                                |
| [**вебсоккетрецеиве**](/windows/desktop/api/Websocket/nf-websocket-websocketreceive)<br/>                           | добавляет операцию получения в очередь операций компонента протокола.<br/>                                                                                                                              |
| [**вебсоккетсенд**](/windows/desktop/api/Websocket/nf-websocket-websocketsend)<br/>                                 | добавляет операцию отправки в очередь операций компонента протокола.<br/>                                                                                                                                 |



 

 

