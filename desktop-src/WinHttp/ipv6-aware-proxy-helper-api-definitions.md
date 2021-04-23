---
description: Чтобы воспользоваться преимуществами функций, поддерживающих протокол IPv6, ИТ-администраторы должны определить в своем скрипте WPAD, функцию с именем Финдпроксифорурлекс (URL-адрес, узел), которая заменит устаревшую функцию Финдпроксифорурл (URL-адрес, узел).
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: Определения API модуля поддержки IPv6-Aware прокси-сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684217"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a><span data-ttu-id="bc0d2-103">Определения API модуля поддержки IPv6-Aware прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="bc0d2-103">IPv6-Aware Proxy Helper API Definitions</span></span>

<span data-ttu-id="bc0d2-104">Чтобы воспользоваться преимуществами функций, поддерживающих протокол IPv6, ИТ-администраторы должны определить в своем скрипте WPAD, функцию с именем Финдпроксифорурлекс (URL-адрес, узел), которая заменит устаревшую функцию Финдпроксифорурл (URL-адрес, узел).</span><span class="sxs-lookup"><span data-stu-id="bc0d2-104">In order to take advantage of the IPv6 enabled functions, IT administrators must define within their WPAD script, a function called FindProxyForURLEx (url, host) which will replace the legacy FindProxyForUrl (url, host) function.</span></span> <span data-ttu-id="bc0d2-105">Только из новой функции Финдпроксифорурлекс администраторы смогут выполнять новые функции.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-105">Only from the new FindProxyForURLEx function will administrators be able to execute the new functions.</span></span>

<span data-ttu-id="bc0d2-106">Мы также попытались упростить работу для разработчиков, выполнив сопоставление наших функций для возврата различных типов IP-адресов в том же порядке предпочтения, что и другие сетевые компоненты, в частности IPv6-адреса, за которыми следует IPv4-адреса (т. е. текущее поведение функции функцию getaddrinfo (...) Winsock).</span><span class="sxs-lookup"><span data-stu-id="bc0d2-106">We also attempted to simplify work for developers, by aligning our functions to return different types of IP addresses in the same order of preference as other networking components, specifically IPv6 addresses followed by IPv4 addresses (i.e. current behavior for Winsock’s getaddrinfo(..) function).</span></span>

<span data-ttu-id="bc0d2-107">Следующие функции являются расширениями [спецификации формата файла для прокси-сервера Navigator (PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) , которые позволяют сценариям WPAD обрабатывать сети с поддержкой IPv6.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-107">The following functions are extensions to the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) to enable WPAD scripts to handle IPv6 capable networks.</span></span>

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a><span data-ttu-id="bc0d2-108">Стандартные функции и среда для функции JavaScript Финдпроксифорурлекс</span><span class="sxs-lookup"><span data-stu-id="bc0d2-108">Predefined Functions and Environment for the JavaScript Function FindProxyforURLEx</span></span>

<span data-ttu-id="bc0d2-109">Условия на основе имени узла</span><span class="sxs-lookup"><span data-stu-id="bc0d2-109">Hostname based conditions</span></span>

<dl> <dt>

[<span data-ttu-id="bc0d2-110">**исресолвабликс**</span><span class="sxs-lookup"><span data-stu-id="bc0d2-110">**isResolvableEx**</span></span>](isresolvableex.md)
</dt> <dd>

<span data-ttu-id="bc0d2-111">Определяет, может ли данная строка узла разрешаться в IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-111">Determines if a given host string can resolve to an IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="bc0d2-112">**исиннетекс**</span><span class="sxs-lookup"><span data-stu-id="bc0d2-112">**isInNetEx**</span></span>](isinnetex.md)
</dt> <dd>

<span data-ttu-id="bc0d2-113">Определяет, находится ли IP-адрес в определенной подсети.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-113">Determines if an IP address is in a specific subnet.</span></span>

</dd> </dl>

<span data-ttu-id="bc0d2-114">Связанные служебные функции</span><span class="sxs-lookup"><span data-stu-id="bc0d2-114">Related utility functions</span></span>

<dl> <dt>

[<span data-ttu-id="bc0d2-115">**днсресолвикс**</span><span class="sxs-lookup"><span data-stu-id="bc0d2-115">**dnsResolveEx**</span></span>](dnsresolveex.md)
</dt> <dd>

<span data-ttu-id="bc0d2-116">Разрешение строки узла в IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-116">Resolve a host string to its IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="bc0d2-117">**мипаддрессекс**</span><span class="sxs-lookup"><span data-stu-id="bc0d2-117">**myIPAddressEx**</span></span>](myipaddressex.md)
</dt> <dd>

<span data-ttu-id="bc0d2-118">Находит все IP-адреса для localhost.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-118">Finds all the IP addresses for localhost.</span></span>

</dd> <dt>

[<span data-ttu-id="bc0d2-119">**сортипаддресслист**</span><span class="sxs-lookup"><span data-stu-id="bc0d2-119">**sortIpAddressList**</span></span>](sortipaddresslist.md)
</dt> <dd>

<span data-ttu-id="bc0d2-120">Сортирует список IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-120">Sorts a list of IP addresses.</span></span>

</dd> <dt>

[<span data-ttu-id="bc0d2-121">**жетклиентверсион**</span><span class="sxs-lookup"><span data-stu-id="bc0d2-121">**getClientVersion**</span></span>](getclientversion.md)
</dt> <dd>

<span data-ttu-id="bc0d2-122">Возвращает версию обработчика обработки WPAD.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-122">Gets the version of the WPAD processing engine.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="bc0d2-123">Для этой функции требуется Windows Internet Explorer 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-123">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



