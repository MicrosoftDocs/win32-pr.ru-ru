---
title: Терминология каналов
description: Как и другие типы параметров для удаленных вызовов процедур, каналы могут быть \ "\" \ "\" \ "\" \ "\ \" \ "
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533404"
---
# <a name="essential-pipe-terminology"></a><span data-ttu-id="8bc9f-103">Терминология каналов</span><span class="sxs-lookup"><span data-stu-id="8bc9f-103">Essential Pipe Terminology</span></span>

<span data-ttu-id="8bc9f-104">Как и другие типы параметров для удаленных вызовов процедур, каналы могут находиться \[ [**в**](/windows/desktop/Midl/in) \] параметрах in или \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="8bc9f-104">Like other types of parameters to remote procedure calls, pipes can be \[ [**in**](/windows/desktop/Midl/in)\] or \[ [**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="8bc9f-105">Поскольку сервер управляет передачей данных через канал, говорят, что каналы с \[  \] атрибутом in *запрашивают* данные на сервер.</span><span class="sxs-lookup"><span data-stu-id="8bc9f-105">Since the server controls the transfer of data through a pipe, pipes with the \[**in**\] attribute are said to *pull* data to the server.</span></span> <span data-ttu-id="8bc9f-106">Аналогичным образом выходные *каналы* отправляют данные с сервера клиенту.</span><span class="sxs-lookup"><span data-stu-id="8bc9f-106">Similarly, output pipes *push* data from the server to the client.</span></span> <span data-ttu-id="8bc9f-107">Процедуры, которые выполняют передачу данных, называются *процедурой извлечения* и *процедурой Push* соответственно.</span><span class="sxs-lookup"><span data-stu-id="8bc9f-107">The procedures that do the data transfer are called the *pull procedure* and the *push procedure*, respectively.</span></span>

<span data-ttu-id="8bc9f-108">Компилятор MIDL создает процедуры push и Pull для сервера.</span><span class="sxs-lookup"><span data-stu-id="8bc9f-108">The MIDL compiler generates the push and pull procedures for the server.</span></span> <span data-ttu-id="8bc9f-109">Кроме того, он управляет выделением буферов данных в памяти.</span><span class="sxs-lookup"><span data-stu-id="8bc9f-109">In addition, it manages the allocation of data buffers in memory.</span></span> <span data-ttu-id="8bc9f-110">Однако клиент должен предоставить собственные процедуры push и Pull.</span><span class="sxs-lookup"><span data-stu-id="8bc9f-110">However, the client must provide its own push and pull procedures.</span></span> <span data-ttu-id="8bc9f-111">Он также должен предоставить процедуру выделения буферов памяти, используемых каналом.</span><span class="sxs-lookup"><span data-stu-id="8bc9f-111">It must also provide a procedure for allocating the memory buffers used by the pipe.</span></span> <span data-ttu-id="8bc9f-112">Они автоматически вызываются клиентской заглушкой в соответствующее время.</span><span class="sxs-lookup"><span data-stu-id="8bc9f-112">These are automatically called at the appropriate time by the client stub.</span></span> <span data-ttu-id="8bc9f-113">Процедура распределения часто называется процедурой выделения или функцией выделения.</span><span class="sxs-lookup"><span data-stu-id="8bc9f-113">The allocation procedure is often called the alloc procedure or the alloc function.</span></span>

 

 