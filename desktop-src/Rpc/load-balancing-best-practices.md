---
title: Рекомендации по балансировке нагрузки
description: Рекомендации по балансировке нагрузки
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c68b85f60b75cb5a0fc75bd5ad8bd438608a9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987731"
---
# <a name="load-balancing-best-practices"></a><span data-ttu-id="5f00c-103">Рекомендации по балансировке нагрузки</span><span class="sxs-lookup"><span data-stu-id="5f00c-103">Load Balancing Best Practices</span></span>

<span data-ttu-id="5f00c-104">При настройке и настройке балансировки нагрузки RPC следует следовать нескольким рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="5f00c-104">Several best practices should be followed when setting up and configuring RPC Load balancing.</span></span>

<span data-ttu-id="5f00c-105">Во – первых, безопасность должна быть установлена для входящих и исходящих вызовов ФУНТа.</span><span class="sxs-lookup"><span data-stu-id="5f00c-105">First, security should be set on incoming and outgoing LBS calls.</span></span> <span data-ttu-id="5f00c-106">Это означает, что оба необязательных раздела реестра с параметром [безопасности](configuring-load-balancing.md) не должны присутствовать или быть равны нулю.</span><span class="sxs-lookup"><span data-stu-id="5f00c-106">This means both of the optional [NoSecurity](configuring-load-balancing.md) registry keys should either not be present or should be set to zero.</span></span>

<span data-ttu-id="5f00c-107">Во вторых, обратите внимание на решение о балансировке нагрузки переднего плана, используемое в сочетании с решением для балансировки нагрузки RPC.</span><span class="sxs-lookup"><span data-stu-id="5f00c-107">Second, attention must be paid to the front end load balancing solution used in conjunction with the RPC Load Balancing solution.</span></span> <span data-ttu-id="5f00c-108">Например, если подсистема балансировки нагрузки переднего плана использует простую балансировку нагрузки с циклическим перебором, на ферме серверов должно существовать нечетное число серверов.</span><span class="sxs-lookup"><span data-stu-id="5f00c-108">For example, if the front end load balancer uses simple round robin load balancing, an odd number of servers should exist in the server farm.</span></span> <span data-ttu-id="5f00c-109">Это позволяет снизить вероятность того, что все подключения пересылаются и, таким же, обслуживаются одним сервером или серверами.</span><span class="sxs-lookup"><span data-stu-id="5f00c-109">This is to mitigate the possibility of all connections being forwarded and thus serviced by the same server or servers.</span></span>

<span data-ttu-id="5f00c-110">Для обеспечения безопасности обычно желательно, чтобы брандмауэр управляет доступом к прокси-серверам RPC.</span><span class="sxs-lookup"><span data-stu-id="5f00c-110">For security, it is commonly desirable to have a firewall control access to RPC Proxy servers.</span></span> <span data-ttu-id="5f00c-111">Если используется решение брандмауэра на основе порта, конечные точки RPC должны быть статическими, чтобы ограничить число портов, открываемых в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="5f00c-111">If a port based firewall solution is employed, RPC endpoints must be static in order to limit the number of ports that are opened in the firewall.</span></span> <span data-ttu-id="5f00c-112">В Windows Server 2008 и более поздних версиях Windows RPC предоставляет механизм назначения статического порта динамическим конечным точкам.</span><span class="sxs-lookup"><span data-stu-id="5f00c-112">On Windows Server 2008 and later versions of Windows, RPC provides a mechanism to assign a static port to dynamic endpoints.</span></span> <span data-ttu-id="5f00c-113">Это достигается с помощью команд брандмауэра Netsh RPC.</span><span class="sxs-lookup"><span data-stu-id="5f00c-113">This is achieved through the RPC netsh firewall commands.</span></span> <span data-ttu-id="5f00c-114">Пример набора команд для установки для интерфейса ФУНТа статического порта 3010:</span><span class="sxs-lookup"><span data-stu-id="5f00c-114">An example set of commands to set the LBS interface to the static port of 3010 is:</span></span>

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

<span data-ttu-id="5f00c-115">Команду RPC Netsh можно использовать для установки статической конечной точки для любого динамического или статического интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5f00c-115">The RPC netsh command can be used to set a static endpoint for any dynamic or static interface.</span></span> <span data-ttu-id="5f00c-116">Это полезно при ограничении доступа к компьютеру, на котором работает решение брандмауэра на основе портов.</span><span class="sxs-lookup"><span data-stu-id="5f00c-116">This is useful when restricting access to a machine running a port based firewall solution.</span></span> <span data-ttu-id="5f00c-117">Если используется решение брандмауэра Windows, интерфейс RPC можно заблокировать или включить, не назначив его конкретному порту.</span><span class="sxs-lookup"><span data-stu-id="5f00c-117">If the Windows firewall solution is used, the RPC interface can be blocked or enabled without having to assign it to a specific port.</span></span> <span data-ttu-id="5f00c-118">Дополнительные сведения см. в [справочнике по командам брандмауэра Netsh RPC](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="5f00c-118">For more information, see the [RPC netsh firewall command reference](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span></span>

 

 