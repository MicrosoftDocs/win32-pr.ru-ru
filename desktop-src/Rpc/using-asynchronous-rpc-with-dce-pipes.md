---
title: Использование асинхронного RPC с каналами DCE
description: Microsoft RPC поддерживает использование каналов DCE. Несмотря на то, что они имеют одинаковое имя, каналы DCE не связаны с именованными каналами. Именованные каналы являются транспортным протоколом. Каналы DCE — это не зависящий от протокола метод обмена данными между клиентом и сервером.
ms.assetid: 9de4f6dc-0aa9-446e-b68c-e0d1e247fea7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e9c98f4d4191a064d78cff2c918077f27d676f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067928"
---
# <a name="using-asynchronous-rpc-with-dce-pipes"></a><span data-ttu-id="2f391-106">Использование асинхронного RPC с каналами DCE</span><span class="sxs-lookup"><span data-stu-id="2f391-106">Using Asynchronous RPC with DCE Pipes</span></span>

<span data-ttu-id="2f391-107">Microsoft RPC поддерживает использование каналов DCE.</span><span class="sxs-lookup"><span data-stu-id="2f391-107">Microsoft RPC supports the use of DCE pipes.</span></span> <span data-ttu-id="2f391-108">Несмотря на то, что они имеют одинаковое имя, каналы DCE не связаны с [именованными каналами](asynchronous-rpc-over-the-named-pipe-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="2f391-108">Although they share a similar name, DCE pipes are unrelated to [named pipes](asynchronous-rpc-over-the-named-pipe-protocol.md).</span></span> <span data-ttu-id="2f391-109">Именованные каналы являются транспортным протоколом.</span><span class="sxs-lookup"><span data-stu-id="2f391-109">Named pipes are a transport protocol.</span></span> <span data-ttu-id="2f391-110">Каналы DCE — это не зависящий от протокола метод обмена данными между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="2f391-110">DCE pipes are a protocol-independent method of client/server communication.</span></span>

<span data-ttu-id="2f391-111">В этом разделе представлено обсуждение RPC с использованием асинхронных каналов DCE.</span><span class="sxs-lookup"><span data-stu-id="2f391-111">This section presents a discussion of RPC using asynchronous DCE pipes.</span></span> <span data-ttu-id="2f391-112">Он разделен на следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="2f391-112">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="2f391-113">Асинхронные каналы</span><span class="sxs-lookup"><span data-stu-id="2f391-113">Asynchronous Pipes</span></span>](asynchronous-pipes.md)
-   [<span data-ttu-id="2f391-114">Объявление асинхронных каналов</span><span class="sxs-lookup"><span data-stu-id="2f391-114">Declaring Asynchronous Pipes</span></span>](declaring-asynchronous-pipes.md)
-   [<span data-ttu-id="2f391-115">Асинхронная обработка канала на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="2f391-115">Client-side Asynchronous Pipe Handling</span></span>](client-side-asynchronous-pipe-handling.md)
-   [<span data-ttu-id="2f391-116">Обработка асинхронных каналов на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="2f391-116">Server-side Asynchronous Pipe Handling</span></span>](server-side-asynchronous-pipe-handling.md)

<span data-ttu-id="2f391-117">Пример приложения RPC с асинхронным каналом см. в образце Филереп в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="2f391-117">For a sample asynchronous pipe RPC application, see the FileRep sample in the Platform Software Development Kit (SDK).</span></span>

 

 




