---
title: Об API сервера HTTP
description: API сервера HTTP предоставляет разработчикам интерфейс низкого уровня на стороне сервера функций HTTP, как определено в RFC 2616.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- API сервера HTTP, обзор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e00fcfe6527b77be32a849f00f62222396f42b5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412592"
---
# <a name="about-http-server-api"></a><span data-ttu-id="88419-104">Об API сервера HTTP</span><span class="sxs-lookup"><span data-stu-id="88419-104">About HTTP Server API</span></span>

<span data-ttu-id="88419-105">API сервера HTTP предоставляет разработчикам интерфейс низкого уровня на стороне сервера функций HTTP, как определено в [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="88419-105">The HTTP Server API provides developers with a low-level interface to the server side of the HTTP functionality as defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="88419-106">API позволяет приложению получать HTTP-запросы, направленные на URL, и отправлять HTTP-ответы.</span><span class="sxs-lookup"><span data-stu-id="88419-106">The API enables an application to receive HTTP requests directed to URLs and send HTTP responses.</span></span> <span data-ttu-id="88419-107">Для отправки динамических ответов рекомендуется использовать интерфейсы ISAPI или ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="88419-107">For sending dynamic responses, the ISAPI or ASP.NET interfaces are recommended.</span></span>

<span data-ttu-id="88419-108">API сервера HTTP позволяет нескольким приложениям сосуществовать в системе, совместно использующим один и тот же TCP-порт (например, порт 80 для HTTP или порт 443 для HTTPS) и обслуживать различные части пространства имен URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="88419-108">The HTTP Server API enables multiple applications to coexist on a system, sharing the same TCP port (for example, port 80 for HTTP or port 443 for HTTPS) and serving different parts of the URL namespace.</span></span>

<span data-ttu-id="88419-109">API сервера HTTP требует знания языка программирования C и знакомство с программированием API Windows.</span><span class="sxs-lookup"><span data-stu-id="88419-109">The HTTP Server API requires knowledge of the C programming language and a familiarity with Windows API programming.</span></span> <span data-ttu-id="88419-110">Приложения, не требующие низкоуровневого доступа к протоколу HTTP, должны использовать службы IIS ISAPI или классы платформа .NET Framework для решений на основе HTTP.</span><span class="sxs-lookup"><span data-stu-id="88419-110">Applications that do not require low-level access to HTTP should use the IIS ISAPI or the .NET Framework classes for HTTP-based solutions.</span></span>

 

 




