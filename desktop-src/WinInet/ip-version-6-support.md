---
title: Поддержка протокола IP версии 6
description: Начиная с версии IE7 и выше, WinINet поддерживает литералы IPv6 в имени узла и компонент центра URI.
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- Поддержка протокола IP версии 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed0857d9a0968bcd3e6c18e54623fb0c7d86cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413467"
---
# <a name="ip-version-6-support"></a><span data-ttu-id="902ad-104">Поддержка протокола IP версии 6</span><span class="sxs-lookup"><span data-stu-id="902ad-104">IP Version 6 Support</span></span>

<span data-ttu-id="902ad-105">Начиная с версии IE7 и выше, WinINet поддерживает литералы IPv6 в имени узла и компонент центра URI.</span><span class="sxs-lookup"><span data-stu-id="902ad-105">Starting with IE7 and above, WinINet supports IPv6 literals in the hostname, and the authority component of the URI.</span></span> <span data-ttu-id="902ad-106">WinINet также поддерживает использование литералов IPv6 в соответствующих частях протокола HTTP, например в заголовке Location.</span><span class="sxs-lookup"><span data-stu-id="902ad-106">WinINet also supports the use of IPv6 literals in relevant portions of the HTTP protocol, such as in the Location header.</span></span>

## <a name="hostname-ipv6-literals-and-uri-components"></a><span data-ttu-id="902ad-107">Литералы IPv6 имени узла и компоненты URI</span><span class="sxs-lookup"><span data-stu-id="902ad-107">Hostname IPv6 Literals and URI Components</span></span>

<span data-ttu-id="902ad-108">WinINet реализует литералы IPv6 в соответствии со спецификациями в RFC 3513.</span><span class="sxs-lookup"><span data-stu-id="902ad-108">WinINet implements IPv6 literals according to the specifications in RFC 3513.</span></span> <span data-ttu-id="902ad-109">Как указано в этом документе RFC, литералы IPv6 в URI должны быть заключены в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="902ad-109">As specified in this RFC, IPv6 literals in a URI must be enclosed in brackets.</span></span> <span data-ttu-id="902ad-110">Например, https:// \[ :: 1 \] /является допустимым URI IPv6; форма без квадратных скобок (недопустима https://::1/) .</span><span class="sxs-lookup"><span data-stu-id="902ad-110">For example, https://\[::1\]/ is a valid IPv6 URI; the form without brackets (https://::1/) is not valid.</span></span> <span data-ttu-id="902ad-111">Однако имена узлов IPv6, которые не являются частью URI, не обязательно должны быть заключены в квадратные скобки. Любая форма допустима для WinINet.</span><span class="sxs-lookup"><span data-stu-id="902ad-111">Hostname IPv6 literals that are not part of the URI, however, do not need to be enclosed in the brackets; either form is acceptable to WinINet.</span></span> <span data-ttu-id="902ad-112">Например, ":: 1" и " \[ :: 1 \] " являются приемлемыми формами литералов имен узлов IPv6.</span><span class="sxs-lookup"><span data-stu-id="902ad-112">For example, both "::1" and "\[::1\]" are acceptable forms of IPv6 hostname literals.</span></span> <span data-ttu-id="902ad-113">Другие API, например API WinSock, также будут принимать обе формы.</span><span class="sxs-lookup"><span data-stu-id="902ad-113">Other APIs, such as the WinSock API, will also accept both forms.</span></span> <span data-ttu-id="902ad-114">Поэтому приложения должны быть подготовлены для поддержки обеих форм литералов имен узлов IPv6.</span><span class="sxs-lookup"><span data-stu-id="902ad-114">Thus applications should be prepared to handle both forms of IPv6 hostname literals.</span></span>

## <a name="scope-id"></a><span data-ttu-id="902ad-115">Идентификатор области</span><span class="sxs-lookup"><span data-stu-id="902ad-115">Scope ID</span></span>

<span data-ttu-id="902ad-116">Литеральный адрес IPv6 в URI может включать идентификатор области.</span><span class="sxs-lookup"><span data-stu-id="902ad-116">The IPv6 literal address in the URI may include a scope ID.</span></span> <span data-ttu-id="902ad-117">Идентификатор области может быть ИДЕНТИФИКАТОРом интерфейса, таким как \[ FE80:: 1% 1 \] .</span><span class="sxs-lookup"><span data-stu-id="902ad-117">A scope ID can be an interface ID such as \[FE80::1%1\].</span></span> <span data-ttu-id="902ad-118">Стандарт URI, описанный в RFC 3986, не определяет синтаксис для идентификатора области, а URI считается неоднородным при наличии идентификатора области.</span><span class="sxs-lookup"><span data-stu-id="902ad-118">The URI standard, documented in RFC 3986, does not define the syntax for the scope ID, and the URI is considered non-uniform when the scope ID is present.</span></span> <span data-ttu-id="902ad-119">Однако WinINet принимает идентификатор области в компоненте центра URI и в литерале имени узла IPv6.</span><span class="sxs-lookup"><span data-stu-id="902ad-119">However, WinINet accepts a scope ID in the authority component of the URI, and in the hostname IPv6 literal.</span></span>

<span data-ttu-id="902ad-120">Символ процента (%) в литеральном адресе IPv6 должно быть процентным escape-символом при его наличии в URI.</span><span class="sxs-lookup"><span data-stu-id="902ad-120">The percent character (%) in the IPv6 literal address must be percent escaped when present in the URI.</span></span> <span data-ttu-id="902ad-121">Например, область с ИДЕНТИФИКАТОРом FE80:: 2% 3 должна отображаться в URI как "https:// \[ FE80:: 2% 253 \] /", где %25 — это шестнадцатеричная кодировка символа процента (%).</span><span class="sxs-lookup"><span data-stu-id="902ad-121">For example, the scope ID FE80::2%3, must appear in the URI as "https://\[FE80::2%253\]/", where %25 is the hex encoded percent character (%).</span></span> <span data-ttu-id="902ad-122">Если приложение получает универсальный код ресурса (URI) из API-интерфейса Winsock [**всааддресстостринг**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) , приложение должно добавить экранированную версию символа процента (%). в имени узла URI.</span><span class="sxs-lookup"><span data-stu-id="902ad-122">If the application retrieves the URI from a Unicode API, such as the Winsock [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) API, the application must add the escaped version of the percent character (%) in the hostname of the URI.</span></span> <span data-ttu-id="902ad-123">Чтобы создать экранированную версию URI, приложения вызывают [**интернеткреатеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) с параметром *dwFlags* , для которого задано значение ICU, и имя узла IPv6, указанное в структуре компонентов URL-адреса, указанной в параметре *лпурлкомпонентс* . **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="902ad-123">To create the escaped version of the URI, applications call [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) with the *dwFlags* parameter set to **ICU\_ESCAPE\_AUTHORITY**, and the IPv6 hostname specified in the URL components structure specified in the *lpUrlComponents* parameter.</span></span>

<span data-ttu-id="902ad-124">Для всех операций сокетов WinINet использует идентификатор области.</span><span class="sxs-lookup"><span data-stu-id="902ad-124">For all sockets operations, WinINet uses the scope ID.</span></span> <span data-ttu-id="902ad-125">Однако, поскольку идентификатор области имеет только значение локального узла, он не отправляется как часть заголовков протокола HTTP в запросе.</span><span class="sxs-lookup"><span data-stu-id="902ad-125">However, because the scope ID has only local host significance, it is not sent as part of the HTTP protocol headers in the request.</span></span> <span data-ttu-id="902ad-126">Например, вызов [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) вызывается со следующим URL-адресом в параметре *лпсзурл* .</span><span class="sxs-lookup"><span data-stu-id="902ad-126">For example, the call to [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) is called with the following URL in the *lpszUrl* parameter.</span></span>

``` syntax
https://[fec0::2%251]:80/path.htm
```

<span data-ttu-id="902ad-127">Часть идентификатора области URL-адреса удаляется с помощью WinINet при отправке запроса HTTP для этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="902ad-127">The scope ID portion of the URL is removed by WinINet when the HTTP request is sent for this URL.</span></span> <span data-ttu-id="902ad-128">Запрос содержит следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="902ad-128">The request contains the following headers:</span></span>

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> <span data-ttu-id="902ad-129">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="902ad-129">WinINet does not support server implementations.</span></span> <span data-ttu-id="902ad-130">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="902ad-130">In addition, it should not be used from a service.</span></span> <span data-ttu-id="902ad-131">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="902ad-131">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 