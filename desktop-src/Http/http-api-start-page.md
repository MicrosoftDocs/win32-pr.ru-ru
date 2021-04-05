---
title: API сервера HTTP
description: API сервера HTTP позволяет приложениям взаимодействовать по протоколу HTTP без использования Microsoft Internet Information Server (IIS).
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- API сервера HTTP
- API сервера HTTP, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133858"
---
# <a name="http-server-api"></a><span data-ttu-id="d3fe0-105">API сервера HTTP</span><span class="sxs-lookup"><span data-stu-id="d3fe0-105">HTTP Server API</span></span>

## <a name="purpose"></a><span data-ttu-id="d3fe0-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="d3fe0-106">Purpose</span></span>

<span data-ttu-id="d3fe0-107">API сервера HTTP позволяет приложениям взаимодействовать по протоколу HTTP без использования Microsoft Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="d3fe0-107">The HTTP Server API enables applications to communicate over HTTP without using Microsoft Internet Information Server (IIS).</span></span> <span data-ttu-id="d3fe0-108">Приложения могут регистрироваться для получения HTTP-запросов для определенных URL-адресов, получения HTTP-запросов и отправки HTTP-ответов.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-108">Applications can register to receive HTTP requests for particular URLs, receive HTTP requests, and send HTTP responses.</span></span> <span data-ttu-id="d3fe0-109">API сервера HTTP включает поддержку SSL, чтобы приложения могли обмениваться данными по защищенным HTTP-соединениям без служб IIS.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-109">The HTTP Server API includes SSL support so that applications can exchange data over secure HTTP connections without IIS.</span></span> <span data-ttu-id="d3fe0-110">Он также предназначен для работы с портами завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-110">It is also designed to work with I/O completion ports.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d3fe0-111">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="d3fe0-111">Developer audience</span></span>

<span data-ttu-id="d3fe0-112">Этот API предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-112">This API is designed for use by C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d3fe0-113">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="d3fe0-113">Run-time requirements</span></span>

<span data-ttu-id="d3fe0-114">API сервера HTTP поддерживается в операционных системах Windows Server 2003 и Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="d3fe0-114">The HTTP Server API is supported on Windows Server 2003 operating systems and on Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="d3fe0-115">Имейте в виду, что Microsoft IIS 5, работающий в Windows XP с пакетом обновления 2 (SP2), не может использовать порт 80 совместно с другими приложениями HTTP, работающими одновременно.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-115">Be aware that Microsoft IIS 5 running on Windows XP with SP2 is not able to share port 80 with other HTTP applications running simultaneously.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d3fe0-116">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d3fe0-116">In this section</span></span>



| <span data-ttu-id="d3fe0-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="d3fe0-117">Topic</span></span>                                                                           | <span data-ttu-id="d3fe0-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d3fe0-118">Description</span></span>                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3fe0-119">Об API сервера HTTP</span><span class="sxs-lookup"><span data-stu-id="d3fe0-119">About HTTP Server API</span></span>](about-http-server-api.md)<br/>                   | <span data-ttu-id="d3fe0-120">Общие сведения о протоколе HTTP.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-120">General information about HTTP.</span></span><br/>                                                              |
| [<span data-ttu-id="d3fe0-121">Использование API сервера HTTP</span><span class="sxs-lookup"><span data-stu-id="d3fe0-121">Using HTTP Server API</span></span>](using-http-server-api.md)<br/>                   | <span data-ttu-id="d3fe0-122">Процедурное пошаговое описание использования протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-122">Procedural guide for using HTTP.</span></span><br/>                                                             |
| [<span data-ttu-id="d3fe0-123">Справочник по API HTTP-сервера</span><span class="sxs-lookup"><span data-stu-id="d3fe0-123">HTTP Server API Reference</span></span>](http-server-api-reference.md)<br/>           | <span data-ttu-id="d3fe0-124">Документация по конкретным функциям, структурам и типам перечислений, доступным в HTTP.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-124">Documentation of specific functions, structures, and enumeration types available in HTTP.</span></span><br/>    |
| [<span data-ttu-id="d3fe0-125">Пример приложения HTTP-сервера</span><span class="sxs-lookup"><span data-stu-id="d3fe0-125">HTTP Server Sample Application</span></span>](http-server-sample-application.md)<br/> | <span data-ttu-id="d3fe0-126">Пример приложения, демонстрирующий использование API сервера HTTP для выполнения задач на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="d3fe0-126">A sample application that shows how to use the HTTP Server API to perform server-side tasks.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="d3fe0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d3fe0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3fe0-128">Службы HTTP Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="d3fe0-128">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

