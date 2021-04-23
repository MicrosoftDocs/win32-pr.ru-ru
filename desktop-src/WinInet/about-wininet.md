---
title: О команде WinINet
description: Прикладной программный интерфейс (API) Windows Internet (WinINet) позволяет приложению взаимодействовать с протоколами FTP и HTTP для доступа к Интернет-ресурсам.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- О команде WinINet WinINet
- WinINet WinINet, сведения
- WinINet WinINet, начальная страница
- Windows Internet WinINet
- Интернет, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103987232"
---
# <a name="about-wininet"></a><span data-ttu-id="97e57-108">О команде WinINet</span><span class="sxs-lookup"><span data-stu-id="97e57-108">About WinINet</span></span>

> [!NOTE]
> <span data-ttu-id="97e57-109">Для контейнеров приложений, начиная с Windows 10, версия 1709, HTTP/2 (см. [RFC7540](https://tools.ietf.org/html/rfc7540)) включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="97e57-109">For app containers since Windows 10, version 1709, HTTP/2 (see [RFC7540](https://tools.ietf.org/html/rfc7540)) is on by default.</span></span>

<span data-ttu-id="97e57-110">Прикладной программный интерфейс (API) Windows Internet (WinINet) позволяет приложению взаимодействовать с протоколами FTP и HTTP для доступа к Интернет-ресурсам.</span><span class="sxs-lookup"><span data-stu-id="97e57-110">The Windows Internet (WinINet) application programming interface (API) enables your application to interact with FTP and HTTP protocols to access Internet resources.</span></span> <span data-ttu-id="97e57-111">По мере развития стандартов эти функции обрабатывают изменения в базовых протоколах, позволяя им поддерживать единообразное поведение.</span><span class="sxs-lookup"><span data-stu-id="97e57-111">As standards evolve, these functions handle the changes in underlying protocols, enabling them to maintain consistent behavior.</span></span>

<span data-ttu-id="97e57-112">**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также включены приложения для взаимодействия с Gopher.</span><span class="sxs-lookup"><span data-stu-id="97e57-112">**Windows XP and Windows Server 2003 R2 and earlier:** Also enabled applications to interact with Gopher.</span></span>

<span data-ttu-id="97e57-113">Дополнительные сведения можно найти в разделе</span><span class="sxs-lookup"><span data-stu-id="97e57-113">For more information, see:</span></span>

-   [<span data-ttu-id="97e57-114">WinINet и WinHTTP</span><span class="sxs-lookup"><span data-stu-id="97e57-114">WinINet vs. WinHTTP</span></span>](wininet-vs-winhttp.md)
-   [<span data-ttu-id="97e57-115">Дескрипторы ХИНТЕРНЕТ</span><span class="sxs-lookup"><span data-stu-id="97e57-115">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
-   [<span data-ttu-id="97e57-116">Поддержка протокола IP версии 6</span><span class="sxs-lookup"><span data-stu-id="97e57-116">IP Version 6 Support</span></span>](ip-version-6-support.md)
-   [<span data-ttu-id="97e57-117">\_Кодировка содержимого</span><span class="sxs-lookup"><span data-stu-id="97e57-117">Content\_Encoding</span></span>](content-encoding.md)
-   [<span data-ttu-id="97e57-118">Кэширование</span><span class="sxs-lookup"><span data-stu-id="97e57-118">Caching</span></span>](caching.md)
-   [<span data-ttu-id="97e57-119">Общие функции</span><span class="sxs-lookup"><span data-stu-id="97e57-119">Common Functions</span></span>](common-functions.md)
-   [<span data-ttu-id="97e57-120">Сеансы FTP</span><span class="sxs-lookup"><span data-stu-id="97e57-120">FTP Sessions</span></span>](ftp-sessions.md)
-   [<span data-ttu-id="97e57-121">HTTP-сеансы</span><span class="sxs-lookup"><span data-stu-id="97e57-121">HTTP Sessions</span></span>](http-sessions.md)
-   [<span data-ttu-id="97e57-122">Файлы cookie HTTP</span><span class="sxs-lookup"><span data-stu-id="97e57-122">HTTP Cookies</span></span>](http-cookies.md)
-   [<span data-ttu-id="97e57-123">Асинхронная операция</span><span class="sxs-lookup"><span data-stu-id="97e57-123">Asynchronous Operation</span></span>](asynchronous-operation.md)
-   [<span data-ttu-id="97e57-124">Обработка проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="97e57-124">Handling Authentication</span></span>](handling-authentication.md)
-   [<span data-ttu-id="97e57-125">Обработка указателей универсальных ресурсов</span><span class="sxs-lookup"><span data-stu-id="97e57-125">Handling Uniform Resource Locators</span></span>](handling-uniform-resource-locators.md)
-   [<span data-ttu-id="97e57-126">Рекомендации по безопасности \_</span><span class="sxs-lookup"><span data-stu-id="97e57-126">Security\_Guideline</span></span>](security-guidelines.md)

## <a name="internet-protocols"></a><span data-ttu-id="97e57-127">Протоколы Интернета</span><span class="sxs-lookup"><span data-stu-id="97e57-127">Internet Protocols</span></span>

<span data-ttu-id="97e57-128">Два основных протокола Интернета — FTP и HTTP.</span><span class="sxs-lookup"><span data-stu-id="97e57-128">The two primary Internet protocols are FTP and HTTP.</span></span> <span data-ttu-id="97e57-129">Дополнительные сведения об этих протоколах см. в документах RFC (запрос комментариев) для FTP и HTTP:</span><span class="sxs-lookup"><span data-stu-id="97e57-129">For more information about these protocols, see the Request For Comments (RFC) documents for FTP and HTTP:</span></span>

-   <span data-ttu-id="97e57-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *протокол FTP (FTP)*.</span><span class="sxs-lookup"><span data-stu-id="97e57-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.</span></span>
-   <span data-ttu-id="97e57-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *протокол гипертекста-HTTP/1.0*.</span><span class="sxs-lookup"><span data-stu-id="97e57-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol - HTTP/1.0*.</span></span>
-   <span data-ttu-id="97e57-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *протокол HTTP/1.1*.</span><span class="sxs-lookup"><span data-stu-id="97e57-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol - HTTP/1.1*.</span></span>

> [!NOTE]  
> <span data-ttu-id="97e57-133">(Эти ресурсы могут быть недоступны в некоторых языках и странах.)</span><span class="sxs-lookup"><span data-stu-id="97e57-133">(These resources may not be available in some languages and countries.)</span></span>

<span data-ttu-id="97e57-134">**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также поддерживается протокол Gopher.</span><span class="sxs-lookup"><span data-stu-id="97e57-134">**Windows XP and Windows Server 2003 R2 and earlier:** The Gopher protocol was also supported.</span></span> <span data-ttu-id="97e57-135">См. [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *Протокол Интернета Gopher*.</span><span class="sxs-lookup"><span data-stu-id="97e57-135">See [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *The Internet Gopher Protocol*.</span></span>
