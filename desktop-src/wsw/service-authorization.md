---
title: 'Авторизация службы '
description: Приложение может реализовать пользовательскую авторизацию для входящих сообщений на узле службы.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Веб-службы авторизации служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b84b9947d088d5f594ac11f0ee83cc03925f8a3bbc9aeceae0bc7d5cb120477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109844"
---
# <a name="service-authorization"></a>Авторизация службы 

Приложение может реализовать пользовательскую авторизацию для входящих сообщений на узле службы.


Узел службы получает [**\_ \_ \_ обратный вызов безопасности службы**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) обратного вызова WS в рамках [**\_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) , который передается функции [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) . Этот обратный вызов вызывается при получении [ \_ сообщения WS](ws-message.md) .

Приложение может полагаться на этот обратный вызов, чтобы реализовать пользовательскую авторизацию для входящих сообщений на узле службы. Если авторизация не удалась, функция обратного вызова безопасности возвращает кадр сбоя, а узел службы прерывает канал.

Пример реализации см. в примере имени пользователя через SSL example, [хттпкалкулаторвисусернамеоверсслсервицеексампле](httpcalculatorwithusernameoversslserviceexample.md).

 

 




