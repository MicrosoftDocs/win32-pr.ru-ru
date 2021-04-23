---
title: Модели Memory-Management
description: Модели Memory-Management
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986859"
---
# <a name="memory-management-models"></a><span data-ttu-id="3176f-103">Модели Memory-Management</span><span class="sxs-lookup"><span data-stu-id="3176f-103">Memory-Management Models</span></span>

<span data-ttu-id="3176f-104">Как разработчик, у вас есть несколько вариантов выделения и освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="3176f-104">As a developer, you have several choices for how memory is allocated and freed.</span></span> <span data-ttu-id="3176f-105">Рассмотрим сложную структуру данных, состоящую из узлов, связанных с указателями, таких как связанный список или дерево.</span><span class="sxs-lookup"><span data-stu-id="3176f-105">Consider a complex data structure that consists of nodes connected with pointers, such as a linked list or a tree.</span></span> <span data-ttu-id="3176f-106">Можно применять атрибуты, которые выбирают одну из следующих моделей:</span><span class="sxs-lookup"><span data-stu-id="3176f-106">You can apply attributes that select one of the following models:</span></span>

-   <span data-ttu-id="3176f-107">[Выделение и освобождение узлов по](node-by-node-allocation-and-deallocation.md)узлам.</span><span class="sxs-lookup"><span data-stu-id="3176f-107">[Node-by-node allocation and deallocation](node-by-node-allocation-and-deallocation.md).</span></span>
-   <span data-ttu-id="3176f-108">[Один линейный буфер, выделенный заглушкой для всего дерева](stub-allocated-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="3176f-108">[A single linear buffer allocated by the stub for the entire tree](stub-allocated-buffers.md).</span></span>
-   [<span data-ttu-id="3176f-109">Управление памятью заглушки сервера</span><span class="sxs-lookup"><span data-stu-id="3176f-109">Server stub memory management</span></span>](server-stub-memory-management.md)
-   <span data-ttu-id="3176f-110">[Один линейный буфер, выделенный клиентским приложением для всего дерева](application-allocated-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="3176f-110">[A single linear buffer allocated by the client application for the entire tree](application-allocated-buffer.md).</span></span>
-   <span data-ttu-id="3176f-111">[Постоянное хранилище на сервере](persistent-storage-on-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="3176f-111">[Persistent storage on the server](persistent-storage-on-the-server.md).</span></span>

 

 




