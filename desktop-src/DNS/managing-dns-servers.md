---
title: Управление DNS-серверами
description: DNS-сервер — это компьютер, который завершает процесс разрешения имен в DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777963"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="f3ef2-103">Управление DNS-серверами</span><span class="sxs-lookup"><span data-stu-id="f3ef2-103">Managing DNS Servers</span></span>

<span data-ttu-id="f3ef2-104">DNS-сервер — это компьютер, который завершает процесс разрешения имен в DNS.</span><span class="sxs-lookup"><span data-stu-id="f3ef2-104">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="f3ef2-105">DNS-серверы содержат файлы, называемые *файлами зоны*, которые позволяют им разрешать имена в IP-адреса (или наоборот).</span><span class="sxs-lookup"><span data-stu-id="f3ef2-105">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="f3ef2-106">При запросе DNS-сервер реагирует одним из трех способов:</span><span class="sxs-lookup"><span data-stu-id="f3ef2-106">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="f3ef2-107">Сервер возвращает запрошенные данные разрешения имени или разрешения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="f3ef2-107">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="f3ef2-108">Сервер возвращает указатель на другой DNS-сервер, который может обслуживать запрос.</span><span class="sxs-lookup"><span data-stu-id="f3ef2-108">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="f3ef2-109">Сервер указывает, что у него нет запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="f3ef2-109">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="f3ef2-110">DNS-серверы могут, во время подготовки к возврату запрошенных сведений о разрешении, запрашивать другие DNS-серверы.</span><span class="sxs-lookup"><span data-stu-id="f3ef2-110">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="f3ef2-111">Но после этого DNS-серверы не выполняют никаких операций, кроме тех, которые упоминались в предыдущем списке.</span><span class="sxs-lookup"><span data-stu-id="f3ef2-111">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="f3ef2-112">Существует три основных типа DNS-серверов: основные серверы, серверы-получатели и серверы кэширования.</span><span class="sxs-lookup"><span data-stu-id="f3ef2-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="f3ef2-113">Дополнительные сведения об этих DNS-серверах см. в разделе [DNS-серверы](dns-servers.md) .</span><span class="sxs-lookup"><span data-stu-id="f3ef2-113">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="f3ef2-114">Шаги администрирования</span><span class="sxs-lookup"><span data-stu-id="f3ef2-114">Administration Steps</span></span>

<span data-ttu-id="f3ef2-115">Поставщик WMI для DNS позволяет администрировать DNS-серверы с самого сервера или с удаленных узлов.</span><span class="sxs-lookup"><span data-stu-id="f3ef2-115">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="f3ef2-116">Общие шаги, необходимые для администрирования DNS-сервера с помощью поставщика WMI DNS:</span><span class="sxs-lookup"><span data-stu-id="f3ef2-116">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="f3ef2-117">Подключение к поставщику WMI DNS</span><span class="sxs-lookup"><span data-stu-id="f3ef2-117">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="f3ef2-118">Получение экземпляра сервера</span><span class="sxs-lookup"><span data-stu-id="f3ef2-118">Getting a server instance</span></span>
-   <span data-ttu-id="f3ef2-119">Вывод или изменение свойства сервера либо с помощью метода</span><span class="sxs-lookup"><span data-stu-id="f3ef2-119">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="f3ef2-120">Чтобы продемонстрировать, как реализовать эти шаги администрирования, предоставляются примеры.</span><span class="sxs-lookup"><span data-stu-id="f3ef2-120">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="f3ef2-121">Следующие задачи связаны со связанными с ними примерами сценариев.</span><span class="sxs-lookup"><span data-stu-id="f3ef2-121">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="f3ef2-122">Остановка DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="f3ef2-122">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="f3ef2-123">Запуск DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="f3ef2-123">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="f3ef2-124">Перезапуск DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="f3ef2-124">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="f3ef2-125">Добавление IP-адреса</span><span class="sxs-lookup"><span data-stu-id="f3ef2-125">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="f3ef2-126">Удаление IP-адреса</span><span class="sxs-lookup"><span data-stu-id="f3ef2-126">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="f3ef2-127">Вывод свойств DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="f3ef2-127">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="f3ef2-128">Отображение типов свойств DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="f3ef2-128">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="f3ef2-129">Изменение свойств DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="f3ef2-129">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




