---
title: Список прослушивания IP-адресов
description: Интерфейсы API HTTP-сервера не привязаны к IP-адресу и парам портов TCP до тех пор, пока пользователь не зарегистрирует UrlPrefix.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986800"
---
# <a name="ip-listen-list"></a><span data-ttu-id="b7193-103">Список прослушивания IP-адресов</span><span class="sxs-lookup"><span data-stu-id="b7193-103">IP Listen List</span></span>

<span data-ttu-id="b7193-104">Интерфейсы API HTTP-сервера не привязаны к IP-адресу и парам портов TCP до тех пор, пока пользователь не зарегистрирует UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="b7193-104">The HTTP Server APIs do not bind to any IP address and TCP port pairs until a user registers a UrlPrefix.</span></span> <span data-ttu-id="b7193-105">По умолчанию после того, как регистрация введена в очередь запросов, API сервера HTTP привязывается к порту, указанному в UrlPrefix (например, порт 80) для всех IP-адресов (a ADDR \_ ANY или INADDR6 \_ Any), доступных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b7193-105">By default, once a registration is entered in the request queue, the HTTP Server API binds to the port specified in the UrlPrefix (for example port 80) for all IP addresses (INADDR\_ANY or INADDR6\_ANY) available on the machine.</span></span> <span data-ttu-id="b7193-106">Проблемы возникают, когда сторонние приложения (не использующие API HTTP-сервера) привязываются к IP-адресу и парам порта 80 на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b7193-106">Problems arise when third party applications (not using the HTTP Server APIs) bind to IP address and port 80 pairs on the machine.</span></span> <span data-ttu-id="b7193-107">API сервера HTTP позволяет настроить список IP-адресов, которые он привязывает, и решить эту проблему сосуществования.</span><span class="sxs-lookup"><span data-stu-id="b7193-107">The HTTP Server API provides a way to configure the list of IP addresses that it binds and solves this coexistence issue.</span></span> <span data-ttu-id="b7193-108">Системный администратор вызывает функцию [**хттпсетсервицеконфигуратион**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) с параметром *конфигид* , для которого задано значение хттпсервицеконфигиплистенлист, чтобы указать список прослушивания IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b7193-108">The system administrator calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the *ConfigId* parameter set to the HttpServiceConfigIPListenList value to specify the IP listen list.</span></span> <span data-ttu-id="b7193-109">В список можно добавить адреса IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="b7193-109">Both IPv4 and IPv6 addresses can be added to the list.</span></span> <span data-ttu-id="b7193-110">Указанные IP-адреса применяются ко всем приложениям на компьютере с помощью API HTTP-сервера и сохраняются в перезагрузках компьютера.</span><span class="sxs-lookup"><span data-stu-id="b7193-110">The IP addresses entered apply to all applications on the machine using the HTTP Server API and persist across reboots of the machine.</span></span> <span data-ttu-id="b7193-111">Однако любые изменения в конфигурации списка прослушивания IP-адресов не выполняются динамически. в большинстве случаев может потребоваться перезагрузка системы.</span><span class="sxs-lookup"><span data-stu-id="b7193-111">However, any changes to the IP listen list configuration do not take place dynamically; in most cases, a system reboot may be necessary.</span></span>

 

 




