---
title: Недостатки
description: Недостатки
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532390"
---
# <a name="disadvantages"></a><span data-ttu-id="205b8-103">Недостатки</span><span class="sxs-lookup"><span data-stu-id="205b8-103">Disadvantages</span></span>

<span data-ttu-id="205b8-104">Внутрипроцессный сервер предоставляет преимущество скорости и размера обработчика объектов с возможностью редактирования локального сервера.</span><span class="sxs-lookup"><span data-stu-id="205b8-104">In-process servers provide the speed and size advantage of an object handler with the editing capability of a local server.</span></span> <span data-ttu-id="205b8-105">Итак, почему вы когда-либо решили реализовать приложение OLE как локальный сервер, а не внутрипроцессный сервер?</span><span class="sxs-lookup"><span data-stu-id="205b8-105">So why would you ever choose to implement your OLE application as a local server rather than an in-process server?</span></span> <span data-ttu-id="205b8-106">Существует несколько причин.</span><span class="sxs-lookup"><span data-stu-id="205b8-106">There are several reasons:</span></span>

-   <span data-ttu-id="205b8-107">Безопасность.</span><span class="sxs-lookup"><span data-stu-id="205b8-107">Security.</span></span> <span data-ttu-id="205b8-108">Только локальный сервер имеет адресное пространство, изолированное от клиента.</span><span class="sxs-lookup"><span data-stu-id="205b8-108">Only a local server has its address space isolated from that of the client.</span></span> <span data-ttu-id="205b8-109">Внутрипроцессный сервер использует адресное пространство и контекст процесса клиента и, таким образом, может быть менее надежным в случае сбоев или вредоносного программирования.</span><span class="sxs-lookup"><span data-stu-id="205b8-109">An in-process server shares the address space and process context of the client and can therefore be less robust in the face of faults or malicious programming.</span></span>
-   <span data-ttu-id="205b8-110">Гранулярности.</span><span class="sxs-lookup"><span data-stu-id="205b8-110">Granularity.</span></span> <span data-ttu-id="205b8-111">На локальном сервере может размещаться несколько экземпляров своего объекта на множестве клиентов, совместное использование состояния сервера несколькими объектами в нескольких клиентах, которые могут быть сложными или невозможными, если они реализованы в качестве внутрипроцессного сервера, который является просто библиотекой DLL, загруженной в каждый клиент.</span><span class="sxs-lookup"><span data-stu-id="205b8-111">A local server can host multiple instances of its object across many different clients, sharing server state between objects in multiple clients in ways that would be difficult or impossible if implemented as an in-process server, which is simply a DLL loaded into each client.</span></span>
-   <span data-ttu-id="205b8-112">См.</span><span class="sxs-lookup"><span data-stu-id="205b8-112">Compatibility.</span></span> <span data-ttu-id="205b8-113">Если вы решили реализовать внутрипроцессный сервер, вы освобождаете совместимость с OLE 1, который не поддерживает такие серверы.</span><span class="sxs-lookup"><span data-stu-id="205b8-113">If you choose to implement an in-process server, you relinquish compatibility with OLE 1, which does not support such servers.</span></span> <span data-ttu-id="205b8-114">Это не будет рассматриваться для многих разработчиков, но если это так, то это критически важная задача.</span><span class="sxs-lookup"><span data-stu-id="205b8-114">This will not be a consideration for many developers, but if it is, then it is of critical concern.</span></span>
-   <span data-ttu-id="205b8-115">Невозможность поддержки ссылок.</span><span class="sxs-lookup"><span data-stu-id="205b8-115">Inability to support links.</span></span> <span data-ttu-id="205b8-116">Внутрипроцессный сервер не может выступать в качестве источника ссылки.</span><span class="sxs-lookup"><span data-stu-id="205b8-116">An in-process server cannot serve as a link source.</span></span> <span data-ttu-id="205b8-117">Так как библиотека DLL не может выполняться сама по себе, она не может создать объект файла, с которым будет связана ссылка.</span><span class="sxs-lookup"><span data-stu-id="205b8-117">Since a DLL cannot run by itself, it cannot create a file object to be linked to.</span></span>

<span data-ttu-id="205b8-118">Несмотря на эти недостатки, внутрипроцессный сервер может быть отличным выбором для его скорости и размера — если он соответствует всем другим требованиям.</span><span class="sxs-lookup"><span data-stu-id="205b8-118">Despite these disadvantages, an in-process server can be an excellent choice for its speed and size — if it fits all your other requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="205b8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="205b8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="205b8-120">Преимущества</span><span class="sxs-lookup"><span data-stu-id="205b8-120">Advantages</span></span>](advantages.md)
</dt> <dt>

[<span data-ttu-id="205b8-121">Внутрипроцессный сервер</span><span class="sxs-lookup"><span data-stu-id="205b8-121">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




