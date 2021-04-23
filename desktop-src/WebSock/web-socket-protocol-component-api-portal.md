---
title: API компонента протокола WebSocket
description: .
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24edd74fe87185db498e6309a7fda5fa091c7d60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134195"
---
# <a name="websocket-protocol-component-api"></a><span data-ttu-id="f3fae-103">API компонента протокола WebSocket</span><span class="sxs-lookup"><span data-stu-id="f3fae-103">WebSocket Protocol Component API</span></span>

## <a name="purpose"></a><span data-ttu-id="f3fae-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="f3fae-104">Purpose</span></span>

<span data-ttu-id="f3fae-105">API компонента протокола WebSocket позволяет выполнять асинхронные двунаправленные каналы связи по протоколу HTTP, которые работают через существующие сетевые посредники.</span><span class="sxs-lookup"><span data-stu-id="f3fae-105">The WebSocket Protocol Component API enables asynchronous, bi-directional communication channels over HTTP that work across existing network intermediaries.</span></span> <span data-ttu-id="f3fae-106">С помощью API компонента протокола WebSocket клиент использует HTTP для обмена данными с сервером, а затем обе стороны переключаются на базовый протокол, на котором был разворот HTTP (например, TCP или SSL).</span><span class="sxs-lookup"><span data-stu-id="f3fae-106">With the WebSocket Protocol Component API, a client uses HTTP to communicate with a server, and then both sides switch to using the underlying protocol that HTTP was layered on (such as TCP or SSL).</span></span> <span data-ttu-id="f3fae-107">Цель — сначала использовать HTTP для обхода сетевых посредников, а затем использовать установленный сквозной канал TCP/SSL для двунаправленного взаимодействия приложений.</span><span class="sxs-lookup"><span data-stu-id="f3fae-107">The goal is to first use HTTP to traverse over network intermediaries, and then use the established end-to-end underlying TCP/SSL channel for bi-directional application communication.</span></span> <span data-ttu-id="f3fae-108">Протокол WebSocket \[ [вспрото](https://tools.ietf.org/html/rfc6455) \] определен в IETF, а соответствующий API JavaScript \[ [W3CAPI](https://dev.w3.org/html5/websockets/) \] определен в консорциуме W3C.</span><span class="sxs-lookup"><span data-stu-id="f3fae-108">The WebSocket protocol \[[WSPROTO](https://tools.ietf.org/html/rfc6455)\] is defined at the IETF, while an associated Javascript API \[[W3CAPI](https://dev.w3.org/html5/websockets/)\] is defined at the W3C.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f3fae-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="f3fae-109">In this section</span></span>



| <span data-ttu-id="f3fae-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="f3fae-110">Topic</span></span>                                                                                                          | <span data-ttu-id="f3fae-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f3fae-111">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="f3fae-112">**Типы данных API компонента протокола WebSocket**</span><span class="sxs-lookup"><span data-stu-id="f3fae-112">**WebSocket Protocol Component API Data Types**</span></span>](web-socket-protocol-component-api-data-types.md)<br/> | <span data-ttu-id="f3fae-113">Эти типы данных определяются API компонента протокола WebSocket.</span><span class="sxs-lookup"><span data-stu-id="f3fae-113">The WebSocket Protocol Component API defines these data types.</span></span><br/>   |
| [<span data-ttu-id="f3fae-114">Перечисления API компонента протокола WebSocket</span><span class="sxs-lookup"><span data-stu-id="f3fae-114">WebSocket Protocol Component API Enumerations</span></span>](web-socket-protocol-component-api-enumerations.md)<br/> | <span data-ttu-id="f3fae-115">Эти перечисления определяются API компонента протокола WebSocket.</span><span class="sxs-lookup"><span data-stu-id="f3fae-115">The WebSocket Protocol Component API defines these enumerations.</span></span><br/> |
| [<span data-ttu-id="f3fae-116">Функции API компонента протокола WebSocket</span><span class="sxs-lookup"><span data-stu-id="f3fae-116">WebSocket Protocol Component API Functions</span></span>](web-socket-protocol-component-api-functions.md)<br/>       | <span data-ttu-id="f3fae-117">Эти функции определяются API компонента протокола WebSocket.</span><span class="sxs-lookup"><span data-stu-id="f3fae-117">The WebSocket Protocol Component API defines these functions.</span></span><br/>    |
| [<span data-ttu-id="f3fae-118">Структуры API компонентов протокола WebSocket</span><span class="sxs-lookup"><span data-stu-id="f3fae-118">WebSocket Protocol Component API Structures</span></span>](web-socket-protocol-component-api-structures.md)<br/>     | <span data-ttu-id="f3fae-119">Эти структуры определяются API компонента протокола WebSocket.</span><span class="sxs-lookup"><span data-stu-id="f3fae-119">The WebSocket Protocol Component API defines these structures.</span></span><br/>   |



 

## <a name="developer-audience"></a><span data-ttu-id="f3fae-120">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="f3fae-120">Developer audience</span></span>

<span data-ttu-id="f3fae-121">API компонента протокола WebSocket предназначен для использования с помощью программистов C/C++.</span><span class="sxs-lookup"><span data-stu-id="f3fae-121">The WebSocket Protocol Component API is designed for use by use by C/C++ programmers.</span></span> <span data-ttu-id="f3fae-122">Вам потребуются навыки работы с сетью HTTP и Windows.</span><span class="sxs-lookup"><span data-stu-id="f3fae-122">Familiarity with HTTP and Windows networking is required.</span></span>

> [!Note]  
> <span data-ttu-id="f3fae-123">Предпочтительным способом использования протокола WebSocket в Windows является использование [API служб Windows HTTP (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) или [пространства имен Windows. Networks. Sockets](/uwp/api/Windows.Networking.Sockets).</span><span class="sxs-lookup"><span data-stu-id="f3fae-123">The preferred way to use the WebSocket protocol on Windows is through the [Windows HTTP Services (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) or the [Windows.Networking.Sockets namespace](/uwp/api/Windows.Networking.Sockets).</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="f3fae-124">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="f3fae-124">Run-time requirements</span></span>

<span data-ttu-id="f3fae-125">Для API компонента протокола WebSocket требуется Windows 8 и более поздние версии операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="f3fae-125">The WebSocket Protocol Component API requires Windows 8 and later versions of the Windows operating system.</span></span> <span data-ttu-id="f3fae-126">Интерфейсы API можно динамически связывать с помощью websocket.dll.</span><span class="sxs-lookup"><span data-stu-id="f3fae-126">The APIs can be dynamically linked through websocket.dll.</span></span>

> [!Note]  
> <span data-ttu-id="f3fae-127">websocket.dll обеспечивает поддержку HTTP-заголовков, связанных с подтверждением соответствия клиента и сервера, проверяет полученные данные подтверждения и анализирует поток данных WebSocket.</span><span class="sxs-lookup"><span data-stu-id="f3fae-127">websocket.dll provides support for client and server handshake related HTTP headers, verifies received handshake data, and parses the WebSocket data stream.</span></span> <span data-ttu-id="f3fae-128">Он не обрабатывает какие-либо операции HTTP (перенаправление, проверку подлинности, поддержку прокси-сервера) и не выполняет никаких операций ввода-вывода (отправка или получение байтов потока WebSocket).</span><span class="sxs-lookup"><span data-stu-id="f3fae-128">It does not handle any HTTP-specific operations (redirection, authentication, proxy support) nor perform any I/O operations (sending or receiving WebSocket stream bytes).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f3fae-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f3fae-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3fae-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="f3fae-130">HTTP</span></span>](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[<span data-ttu-id="f3fae-131">Службы HTTP Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="f3fae-131">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

