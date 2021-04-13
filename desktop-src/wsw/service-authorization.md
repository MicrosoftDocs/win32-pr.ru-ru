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
ms.openlocfilehash: c296dc6b4900bd20df7d1e70631e758599a0028d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104134791"
---
# <a name="service-authorization"></a><span data-ttu-id="e6e5e-106">Авторизация службы </span><span class="sxs-lookup"><span data-stu-id="e6e5e-106">Service Authorization</span></span>

<span data-ttu-id="e6e5e-107">Приложение может реализовать пользовательскую авторизацию для входящих сообщений на узле службы.</span><span class="sxs-lookup"><span data-stu-id="e6e5e-107">An application can implement custom authorization for incoming messages on a service host .</span></span>


<span data-ttu-id="e6e5e-108">Узел службы получает [**\_ \_ \_ обратный вызов безопасности службы**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) обратного вызова WS в рамках [**\_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) , который передается функции [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) .</span><span class="sxs-lookup"><span data-stu-id="e6e5e-108">A service host receives a security callback [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) as part of the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) which is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function.</span></span> <span data-ttu-id="e6e5e-109">Этот обратный вызов вызывается при получении [ \_ сообщения WS](ws-message.md) .</span><span class="sxs-lookup"><span data-stu-id="e6e5e-109">This callback is invoked when the [WS\_MESSAGE](ws-message.md) is received.</span></span>

<span data-ttu-id="e6e5e-110">Приложение может полагаться на этот обратный вызов, чтобы реализовать пользовательскую авторизацию для входящих сообщений на узле службы.</span><span class="sxs-lookup"><span data-stu-id="e6e5e-110">The application can rely on this callback to implement custom authorization for incoming messages on the service host.</span></span> <span data-ttu-id="e6e5e-111">Если авторизация не удалась, функция обратного вызова безопасности возвращает кадр сбоя, а узел службы прерывает канал.</span><span class="sxs-lookup"><span data-stu-id="e6e5e-111">If the authorization fails the security callback function returns a failure HR, and the service host aborts the channel.</span></span>

<span data-ttu-id="e6e5e-112">Пример реализации см. в примере имени пользователя через SSL example, [хттпкалкулаторвисусернамеоверсслсервицеексампле](httpcalculatorwithusernameoversslserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="e6e5e-112">See the user name over SSL example, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), for an example implementation.</span></span>

 

 




