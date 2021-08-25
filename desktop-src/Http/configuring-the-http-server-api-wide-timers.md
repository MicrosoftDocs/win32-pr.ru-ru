---
title: Настройка расширенных таймеров API HTTP-сервера
description: Настройка расширенных таймеров API HTTP-сервера
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0eb5fc40bedd51884830893673b3bae2341a21110fa2c3b33878dba7a4aef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047354"
---
# <a name="configuring-the-http-server-api-wide-timers"></a>Настройка расширенных таймеров API HTTP-сервера

Таймеры **хеадерваит** и **ИДЛЕКОННЕКТИОН** на уровне API HTTP-сервера настраиваются путем вызова функции [**хттпсетсервицеконфигуратион**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) версии 1,0. Параметр *конфигид* имеет значение **хттпсервицеконфигтимеаут** , а параметр *пконфигинформатион* указывает структуру [**\_ \_ \_ \_ набора времени ожидания конфигурации службы HTTP**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) , которая содержит установленный таймер и значение для таймера.

Для настройки времени ожидания на уровне API HTTP-сервера требуются права администратора, однако при выполнении запросов они не запрашиваются. Эти конфигурации задаются для всех приложений на компьютере и сохраняются при перезапуске службы HTTP или перезагрузке компьютера. Чтобы выполнить запрос к существующему времени ожидания API HTTP-сервера, приложение вызывает [**хттпкуерисервицеконфигуратион**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).

 

 




