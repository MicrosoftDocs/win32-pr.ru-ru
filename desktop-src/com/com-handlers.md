---
title: Обработчики COM
description: Назначение обработчиков COM заключается в том, чтобы предоставить некоторые \ 0034; Smart \ \ 0034; код в адресном пространстве клиента, который может оптимизировать вызовы между клиентом и сервером. Обработчики могут переопределять некоторые интерфейсы, одновременно делегируя других пользователей серверу (через прокси-сервер).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710029"
---
# <a name="com-handlers"></a><span data-ttu-id="bc4d8-104">Обработчики COM</span><span class="sxs-lookup"><span data-stu-id="bc4d8-104">COM Handlers</span></span>

<span data-ttu-id="bc4d8-105">Назначение обработчиков COM заключается в том, чтобы предоставить в адресном пространстве клиента код Smart, который может оптимизировать вызовы между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="bc4d8-105">The purpose of COM handlers is to provide some "smart" code in the client address space that can optimize calls between a client and server.</span></span> <span data-ttu-id="bc4d8-106">Обработчики могут переопределять некоторые интерфейсы, одновременно делегируя других пользователей серверу (через прокси-сервер).</span><span class="sxs-lookup"><span data-stu-id="bc4d8-106">Handlers can override some interfaces while delegating others directly to the server (through the proxy).</span></span>

<span data-ttu-id="bc4d8-107">Существует два типа обработчиков COM:</span><span class="sxs-lookup"><span data-stu-id="bc4d8-107">There are two types of COM handlers:</span></span>

-   <span data-ttu-id="bc4d8-108">[Обработчик OLE](the-ole-handler.md) — это высокоплотная библиотека DLL, которая предоставляет важные службы для связывания и внедрения.</span><span class="sxs-lookup"><span data-stu-id="bc4d8-108">[The OLE handler](the-ole-handler.md) is a heavyweight DLL that provides important services for linking and embedding.</span></span> <span data-ttu-id="bc4d8-109">Обычно он создается перед запуском сервера и инициализируется, чтобы сервер был активирован, когда внедренный объект переходит в состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="bc4d8-109">It is usually created before the server is launched and is initialized so that the server is activated when the embedded object enters the running state.</span></span>
-   <span data-ttu-id="bc4d8-110">[Упрощенный клиентский обработчик](the-lightweight-client-side-handler.md) может быть создан для любой цели, может быть очень небольшим и не может быть создан перед сервером.</span><span class="sxs-lookup"><span data-stu-id="bc4d8-110">[The lightweight client-side handler](the-lightweight-client-side-handler.md) can be created for any purpose, can be very small, and cannot be created before the server.</span></span>

 

 




