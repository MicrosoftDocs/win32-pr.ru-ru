---
title: Примеры (RPC)
description: Примеры, демонстрирующие основные понятия удаленного вызова процедур (RPC).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- Удаленный вызов процедур RPC, примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a814d78afbfc7fefa979c890cbbb8c3d4ce0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105672433"
---
# <a name="examples-rpc"></a><span data-ttu-id="bee3d-104">Примеры (RPC)</span><span class="sxs-lookup"><span data-stu-id="bee3d-104">Examples (RPC)</span></span>

<span data-ttu-id="bee3d-105">Пакет средств разработки программного обеспечения платформы (SDK) включает примеры, демонстрирующие различные основные понятия удаленного вызова процедур (RPC), как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="bee3d-105">The Platform Software Development Kit (SDK) includes examples that demonstrate a variety of Remote Procedure Call (RPC) concepts, as follows:</span></span>

-   <span data-ttu-id="bee3d-106">АСИНКРПК иллюстрирует структуру приложения RPC, использующего асинхронные вызовы удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="bee3d-106">ASYNCRPC illustrates the structure of an RPC application that uses asynchronous remote procedure calls.</span></span> <span data-ttu-id="bee3d-107">В нем также демонстрируются различные методы уведомления о завершении вызова.</span><span class="sxs-lookup"><span data-stu-id="bee3d-107">It also demonstrates various methods of notification of the call's completion.</span></span>
-   <span data-ttu-id="bee3d-108">КЛУУИД демонстрирует использование UUID клиентского объекта, чтобы позволить клиенту выбирать из нескольких реализаций удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="bee3d-108">CLUUID demonstrates use of the client-object UUID to enable a client to select from multiple implementations of a remote procedure.</span></span>
-   <span data-ttu-id="bee3d-109">Каталог данных содержит четыре программы: ДУНИОН иллюстрирует Объединенные (неинкапсулированные) объединения; Параметр InOut демонстрирует [ \[ в \] ](../midl/in.md), параметры [ \[ out \] ](../midl/out-idl.md) ; РЕПАС демонстрирует атрибут [представления \_ как](/windows/desktop/Midl/represent-as) . XMIT демонстрирует атрибут [передачи \_ as](/windows/desktop/Midl/transmit-as) .</span><span class="sxs-lookup"><span data-stu-id="bee3d-109">DATA directory contains four programs: DUNION illustrates discriminated (nonencapsulated) unions; INOUT demonstrates [\[in\]](../midl/in.md), [\[out\]](../midl/out-idl.md) parameters; REPAS demonstrates the [represent\_as](/windows/desktop/Midl/represent-as) attribute; XMIT demonstrates the [transmit\_as](/windows/desktop/Midl/transmit-as) attribute.</span></span>
-   <span data-ttu-id="bee3d-110">ДИНЕПТ демонстрирует клиентское приложение, управляющее подключением к серверу через динамические конечные точки.</span><span class="sxs-lookup"><span data-stu-id="bee3d-110">DYNEPT demonstrates a client application managing its connection to the server through dynamic endpoints.</span></span>
-   <span data-ttu-id="bee3d-111">Каталог ФИЛЕРЕП содержит четыре примера, иллюстрирующие, как разработчики могут создавать простую службу репликации файлов, службу репликации файлов с несколькими пользователями, службу, поддерживающую функции безопасности, и службу, использующую асинхронные каналы RPC.</span><span class="sxs-lookup"><span data-stu-id="bee3d-111">FILEREP directory contains four samples illustrating how developers can write a simple file replication service, a multi-user file replication service, a service supporting security features, and a service using RPC asynchronous pipes.</span></span>
-   <span data-ttu-id="bee3d-112">В каталоге Handles содержатся три программы, AUTO, ККСХНДЛ, УСРДЕФ, которые демонстрируют [Автоматические \_ дескрипторы](/windows/desktop/Midl/auto-handle), \[ \_ дескриптор контекста \] и универсальные (определяемые пользователем) дескрипторы соответственно.</span><span class="sxs-lookup"><span data-stu-id="bee3d-112">HANDLES directory contains three programs, AUTO, CXHNDL, USRDEF, which demonstrate [auto\_handle](/windows/desktop/Midl/auto-handle), \[context\_handle\], and generic (user-defined) handles, respectively.</span></span>
-   <span data-ttu-id="bee3d-113">Привет — это реализация клиента или сервера "Hello, World".</span><span class="sxs-lookup"><span data-stu-id="bee3d-113">HELLO is a client/server implementation of "Hello, world."</span></span>
-   <span data-ttu-id="bee3d-114">Каталог выбора содержит две программы: ПИККЛП демонстрирует сериализацию процедур данных. В поле выбора показана сериализация типов данных; Обе программы используют атрибуты [ \[ кодирования \] ](../midl/encode.md) и [ \[ декодирования \] ](../midl/decode.md) .</span><span class="sxs-lookup"><span data-stu-id="bee3d-114">PICKLE directory contains two programs: PICKLP demonstrates data procedure serialization; PICKLT demonstrates data type serialization; both programs use the [\[encode\]](../midl/encode.md) and [\[decode\]](../midl/decode.md) attributes.</span></span>
-   <span data-ttu-id="bee3d-115">КАНАЛЫ демонстрируют использование конструктора типа канала.</span><span class="sxs-lookup"><span data-stu-id="bee3d-115">PIPES demonstrates the use of the pipe-type constructor.</span></span>
-   <span data-ttu-id="bee3d-116">РПКСВК демонстрирует реализацию службы с помощью RPC.</span><span class="sxs-lookup"><span data-stu-id="bee3d-116">RPCSVC demonstrates the implementation of a service with RPC.</span></span>
-   <span data-ttu-id="bee3d-117">СТРАУТ демонстрирует, как выделить память на сервере для двумерного объекта (массива указателей) и передать его обратно клиенту в виде \[ \] параметра только для выхода.</span><span class="sxs-lookup"><span data-stu-id="bee3d-117">STROUT demonstrates how to allocate memory at a server for a two-dimensional object (an array of pointers) and pass it back to the client as an \[out\]-only parameter.</span></span> <span data-ttu-id="bee3d-118">Затем клиент освобождает память.</span><span class="sxs-lookup"><span data-stu-id="bee3d-118">The client then frees the memory.</span></span> <span data-ttu-id="bee3d-119">Эта методика позволяет заглушке вызывать сервер, не зная заранее, сколько данных будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="bee3d-119">This technique allows the stub to call the server without knowing in advance how much data will be returned.</span></span>

    <span data-ttu-id="bee3d-120">Эта программа также позволяет пользователю компилироваться либо для Юникода, либо для ANSI.</span><span class="sxs-lookup"><span data-stu-id="bee3d-120">This program also allows the user to compile either for UNICODE or ANSI.</span></span>

<span data-ttu-id="bee3d-121">Все исходные файлы и файл makefile для этих программ находятся в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="bee3d-121">All of the source files and makefiles for these programs are located in the Platform SDK.</span></span>

<span data-ttu-id="bee3d-122">Основные сведения о разработке приложений RPC и более простых примерах см. в разделах [руководства](tutorial.md) .</span><span class="sxs-lookup"><span data-stu-id="bee3d-122">For basic RPC application development and simpler examples, please see the [Tutorial](tutorial.md) topics.</span></span>

 

 
