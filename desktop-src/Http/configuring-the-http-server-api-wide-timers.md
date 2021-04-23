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
# <a name="configuring-the-http-server-api-wide-timers"></a><span data-ttu-id="22e91-103">Настройка расширенных таймеров API HTTP-сервера</span><span class="sxs-lookup"><span data-stu-id="22e91-103">Configuring the HTTP Server API Wide Timers</span></span>

<span data-ttu-id="22e91-104">Таймеры **хеадерваит** и **ИДЛЕКОННЕКТИОН** на уровне API HTTP-сервера настраиваются путем вызова функции [**хттпсетсервицеконфигуратион**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="22e91-104">The HTTP Server API-wide **HeaderWait** and **IdleConnection** timers are configured by calling the version 1.0 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function.</span></span> <span data-ttu-id="22e91-105">Параметр *конфигид* имеет значение **хттпсервицеконфигтимеаут** , а параметр *пконфигинформатион* указывает структуру [**\_ \_ \_ \_ набора времени ожидания конфигурации службы HTTP**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) , которая содержит установленный таймер и значение для таймера.</span><span class="sxs-lookup"><span data-stu-id="22e91-105">The *ConfigId* parameter is set to **HttpServiceConfigTimeout** and the *pConfigInformation* parameter specifies the [**HTTP\_SERVICE\_CONFIG\_TIMEOUT\_SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) structure that contains the timer that is set and the value for the timer.</span></span>

<span data-ttu-id="22e91-106">Для настройки времени ожидания на уровне API HTTP-сервера требуются права администратора, однако при выполнении запросов они не запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="22e91-106">Configuring the HTTP Server API-wide timeouts requires administrative privileges, however querying them does not.</span></span> <span data-ttu-id="22e91-107">Эти конфигурации задаются для всех приложений на компьютере и сохраняются при перезапуске службы HTTP или перезагрузке компьютера.</span><span class="sxs-lookup"><span data-stu-id="22e91-107">These configurations are set for all applications on the computer and they persist when the HTTP service is restarted or the computer is restarted.</span></span> <span data-ttu-id="22e91-108">Чтобы выполнить запрос к существующему времени ожидания API HTTP-сервера, приложение вызывает [**хттпкуерисервицеконфигуратион**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).</span><span class="sxs-lookup"><span data-stu-id="22e91-108">To query existing HTTP Server API-wide timeouts, the application calls [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).</span></span>

 

 




