---
title: Управление DNS-серверами
description: Сведения об управлении DNS-серверами. DNS-сервер — это компьютер, который завершает процесс разрешения имен в DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d797e05bc326b35e48173082d9b36a2b334fd9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010777"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="9fefd-104">Управление DNS-серверами</span><span class="sxs-lookup"><span data-stu-id="9fefd-104">Managing DNS Servers</span></span>

<span data-ttu-id="9fefd-105">DNS-сервер — это компьютер, который завершает процесс разрешения имен в DNS.</span><span class="sxs-lookup"><span data-stu-id="9fefd-105">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="9fefd-106">DNS-серверы содержат файлы, называемые *файлами зоны*, которые позволяют им разрешать имена в IP-адреса (или наоборот).</span><span class="sxs-lookup"><span data-stu-id="9fefd-106">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="9fefd-107">При запросе DNS-сервер реагирует одним из трех способов:</span><span class="sxs-lookup"><span data-stu-id="9fefd-107">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="9fefd-108">Сервер возвращает запрошенные данные разрешения имени или разрешения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="9fefd-108">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="9fefd-109">Сервер возвращает указатель на другой DNS-сервер, который может обслуживать запрос.</span><span class="sxs-lookup"><span data-stu-id="9fefd-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="9fefd-110">Сервер указывает, что у него нет запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="9fefd-110">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="9fefd-111">DNS-серверы могут, во время подготовки к возврату запрошенных сведений о разрешении, запрашивать другие DNS-серверы.</span><span class="sxs-lookup"><span data-stu-id="9fefd-111">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="9fefd-112">Но после этого DNS-серверы не выполняют никаких операций, кроме тех, которые упоминались в предыдущем списке.</span><span class="sxs-lookup"><span data-stu-id="9fefd-112">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="9fefd-113">Существует три основных типа DNS-серверов: основные серверы, серверы-получатели и серверы кэширования.</span><span class="sxs-lookup"><span data-stu-id="9fefd-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="9fefd-114">Дополнительные сведения об этих DNS-серверах см. в разделе [DNS-серверы](dns-servers.md) .</span><span class="sxs-lookup"><span data-stu-id="9fefd-114">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="9fefd-115">Шаги администрирования</span><span class="sxs-lookup"><span data-stu-id="9fefd-115">Administration Steps</span></span>

<span data-ttu-id="9fefd-116">Поставщик WMI для DNS позволяет администрировать DNS-серверы с самого сервера или с удаленных узлов.</span><span class="sxs-lookup"><span data-stu-id="9fefd-116">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="9fefd-117">Общие шаги, необходимые для администрирования DNS-сервера с помощью поставщика WMI DNS:</span><span class="sxs-lookup"><span data-stu-id="9fefd-117">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="9fefd-118">Подключение к поставщику WMI DNS</span><span class="sxs-lookup"><span data-stu-id="9fefd-118">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="9fefd-119">Получение экземпляра сервера</span><span class="sxs-lookup"><span data-stu-id="9fefd-119">Getting a server instance</span></span>
-   <span data-ttu-id="9fefd-120">Вывод или изменение свойства сервера либо с помощью метода</span><span class="sxs-lookup"><span data-stu-id="9fefd-120">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="9fefd-121">Чтобы продемонстрировать, как реализовать эти шаги администрирования, предоставляются примеры.</span><span class="sxs-lookup"><span data-stu-id="9fefd-121">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="9fefd-122">Следующие задачи связаны со связанными с ними примерами сценариев.</span><span class="sxs-lookup"><span data-stu-id="9fefd-122">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="9fefd-123">Остановка DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="9fefd-123">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9fefd-124">Запуск DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="9fefd-124">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9fefd-125">Перезапуск DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="9fefd-125">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9fefd-126">Добавление IP-адреса</span><span class="sxs-lookup"><span data-stu-id="9fefd-126">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9fefd-127">Удаление IP-адреса</span><span class="sxs-lookup"><span data-stu-id="9fefd-127">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9fefd-128">Вывод свойств DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="9fefd-128">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9fefd-129">Отображение типов свойств DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="9fefd-129">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9fefd-130">Изменение свойств DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="9fefd-130">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




