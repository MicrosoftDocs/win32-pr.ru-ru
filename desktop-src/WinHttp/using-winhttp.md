---
description: В этом разделе описывается, как использовать API C/C++ для служб Microsoft Windows HTTP (WinHTTP) и COM-интерфейс, предоставляемый объектом WinHttpRequest.
ms.assetid: 16178bb8-5e95-46a5-825a-880edc402445
title: Использование WinHTTP
ms.topic: article
ms.date: 07/22/2020
ms.openlocfilehash: cda0a7772b88dfd9c03675c522f4b7504ea00b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497502"
---
# <a name="using-winhttp"></a><span data-ttu-id="3cfc3-103">Использование WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-103">Using WinHTTP</span></span>

<span data-ttu-id="3cfc3-104">В этом разделе описывается, как использовать API C/C++ для служб Microsoft Windows HTTP (WinHTTP) и COM-интерфейс, предоставляемый объектом **WinHttpRequest** .</span><span class="sxs-lookup"><span data-stu-id="3cfc3-104">This section describes how to use both the C/C++ API for Microsoft Windows HTTP Services (WinHTTP) and the COM interface exposed by the **WinHttpRequest** Object.</span></span> <span data-ttu-id="3cfc3-105">Сравнение этих интерфейсов см. в разделе [Выбор интерфейса WinHTTP](choosing-a-winhttp-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="3cfc3-105">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span> <span data-ttu-id="3cfc3-106">В нем также описывается использование средств администрирования, входящих в состав WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="3cfc3-106">It also describes how to use the administrative tools included with WinHTTP.</span></span>

## <a name="how-to-topics"></a><span data-ttu-id="3cfc3-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="3cfc3-107">How-To Topics</span></span>

[<span data-ttu-id="3cfc3-108">Использование API WinHTTP C/C++</span><span class="sxs-lookup"><span data-stu-id="3cfc3-108">Using the WinHTTP C/C++ API</span></span>](using-the-winhttp-c-c---api.md)

-   [<span data-ttu-id="3cfc3-109">Общие сведения о сеансах WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-109">WinHTTP Sessions Overview</span></span>](winhttp-sessions-overview.md)
-   [<span data-ttu-id="3cfc3-110">Дескрипторы ХИНТЕРНЕТ в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-110">HINTERNET Handles in WinHTTP</span></span>](hinternet-handles-in-winhttp.md)
-   [<span data-ttu-id="3cfc3-111">Универсальные указатели ресурсов (URL-адреса) в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-111">Uniform Resource Locators (URLs) in WinHTTP</span></span>](uniform-resource-locators--urls--in-winhttp.md)
-   [<span data-ttu-id="3cfc3-112">Проверка подлинности в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-112">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
-   [<span data-ttu-id="3cfc3-113">Проверка подлинности Passport в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-113">Passport Authentication in WinHTTP</span></span>](passport-authentication-in-winhttp.md)
-   [<span data-ttu-id="3cfc3-114">SSL в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-114">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
-   [<span data-ttu-id="3cfc3-115">Использование WinHTTP в качестве параллельной сборки</span><span class="sxs-lookup"><span data-stu-id="3cfc3-115">Using WinHTTP as a Side-by-side Assembly</span></span>](using-winhttp-as-a-side-by-side-assembly.md)
-   [<span data-ttu-id="3cfc3-116">Обработка файлов cookie в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-116">Cookie Handling in WinHTTP</span></span>](cookie-handling-in-winhttp.md)
-   [<span data-ttu-id="3cfc3-117">Обработка ошибок в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-117">Error Handling in WinHTTP</span></span>](error-handling-in-winhttp.md)
-   [<span data-ttu-id="3cfc3-118">Поддержка автопрокси WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-118">WinHTTP AutoProxy Support</span></span>](winhttp-autoproxy-support.md)

[<span data-ttu-id="3cfc3-119">Использование COM-объекта WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="3cfc3-119">Using the WinHttpRequest COM Object</span></span>](using-the-winhttprequest-com-object.md)

-   [<span data-ttu-id="3cfc3-120">Извлечение данных с помощью скрипта</span><span class="sxs-lookup"><span data-stu-id="3cfc3-120">Retrieving Data Using Script</span></span>](retrieving-data-using-script.md)
-   [<span data-ttu-id="3cfc3-121">Проверка подлинности с помощью скрипта</span><span class="sxs-lookup"><span data-stu-id="3cfc3-121">Authentication Using Script</span></span>](authentication-using-script.md)

[<span data-ttu-id="3cfc3-122">Использование средств WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cfc3-122">Using WinHTTP Tools</span></span>](using-winhttp-tools.md)

-   [<span data-ttu-id="3cfc3-123">WinHttpCfg.exe, средство настройки сертификатов</span><span class="sxs-lookup"><span data-stu-id="3cfc3-123">WinHttpCfg.exe, a Certificate Configuration Tool</span></span>](winhttpcertcfg-exe--a-certificate-configuration-tool.md)
-   [<span data-ttu-id="3cfc3-124">ProxyCfg.exe, средство настройки прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="3cfc3-124">ProxyCfg.exe, a Proxy Configuration Tool</span></span>](proxycfg-exe--a-proxy-configuration-tool.md)
-   [<span data-ttu-id="3cfc3-125">Винхттптрацекфг, средство настройки трассировки</span><span class="sxs-lookup"><span data-stu-id="3cfc3-125">WinHttpTraceCfg, a Trace Configuration Tool</span></span>](winhttptracecfg-exe--a-trace-configuration-tool.md)

 

 



