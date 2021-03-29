---
title: Настройка расширенных таймеров API HTTP-сервера
description: Настройка расширенных таймеров API HTTP-сервера
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae91abb1c89419e99fa13273cd55b0783df3906a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253313"
---
# <a name="configuring-the-http-server-api-wide-timers"></a>Настройка расширенных таймеров API HTTP-сервера

Таймеры **хеадерваит** и **ИДЛЕКОННЕКТИОН** на уровне API HTTP-сервера настраиваются путем вызова функции [**хттпсетсервицеконфигуратион**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) версии 1,0. Параметр *конфигид* имеет значение **хттпсервицеконфигтимеаут** , а параметр *пконфигинформатион* указывает структуру [**\_ \_ \_ \_ набора времени ожидания конфигурации службы HTTP**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) , которая содержит установленный таймер и значение для таймера.

Для настройки времени ожидания на уровне API HTTP-сервера требуются права администратора, однако при выполнении запросов они не запрашиваются. Эти конфигурации задаются для всех приложений на компьютере и сохраняются при перезапуске службы HTTP или перезагрузке компьютера. Чтобы выполнить запрос к существующему времени ожидания API HTTP-сервера, приложение вызывает [**хттпкуерисервицеконфигуратион**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).

 

 




