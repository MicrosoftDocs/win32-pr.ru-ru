---
title: Моникеров
description: Моникер в COM — это не только способ обнаружения объекта \ 8212; моникер также реализуется как объект.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067407"
---
# <a name="monikers"></a><span data-ttu-id="1db58-103">Моникеров</span><span class="sxs-lookup"><span data-stu-id="1db58-103">Monikers</span></span>

<span data-ttu-id="1db58-104">Моникер в COM — это не только способ обнаружения объекта — моникер также реализуется как объект.</span><span class="sxs-lookup"><span data-stu-id="1db58-104">A moniker in COM is not only a way to identify an object—a moniker is also implemented as an object.</span></span> <span data-ttu-id="1db58-105">Этот объект предоставляет службам, которые позволяют компоненту получить указатель на объект, определяемый моникером.</span><span class="sxs-lookup"><span data-stu-id="1db58-105">This object provides services allowing a component to obtain a pointer to the object identified by the moniker.</span></span> <span data-ttu-id="1db58-106">Этот процесс называется *привязкой*.</span><span class="sxs-lookup"><span data-stu-id="1db58-106">This process is referred to as *binding*.</span></span>

<span data-ttu-id="1db58-107">Моникеры — это объекты, реализующие интерфейс [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) и обычно реализованные в DLL как объекты компонентов.</span><span class="sxs-lookup"><span data-stu-id="1db58-107">Monikers are objects that implement the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface and are generally implemented in DLLs as component objects.</span></span> <span data-ttu-id="1db58-108">Существует два способа просмотра использования моникеров: в качестве клиента моникера — компонента, который использует моникер для получения указателя на другой объект. и в качестве поставщика моникера компонент, предоставляющий моникеры, идентифицирующие свои объекты для клиентов моникера.</span><span class="sxs-lookup"><span data-stu-id="1db58-108">There are two ways of viewing the use of monikers: as a moniker client, a component that uses a moniker to get a pointer to another object; and as a moniker provider, a component that supplies monikers identifying its objects to moniker clients.</span></span>

<span data-ttu-id="1db58-109">OLE использует моникеры для подключения и активации объектов, будь то они находятся на одном компьютере или по сети.</span><span class="sxs-lookup"><span data-stu-id="1db58-109">OLE uses monikers to connect to and activate objects, whether they are in the same machine or across a network.</span></span> <span data-ttu-id="1db58-110">Очень важно использовать для сетевых подключений.</span><span class="sxs-lookup"><span data-stu-id="1db58-110">A very important use is for network connections.</span></span> <span data-ttu-id="1db58-111">Они также используются для обнаружения, подключения и выполнения объектов связи с составным документом OLE.</span><span class="sxs-lookup"><span data-stu-id="1db58-111">They are also used to identify, connect to, and run OLE compound document link objects.</span></span> <span data-ttu-id="1db58-112">В этом случае источник ссылки выступает в качестве поставщика моникера, а контейнер, который владеет объектом Link, выступает в качестве клиента моникера.</span><span class="sxs-lookup"><span data-stu-id="1db58-112">In this case, the link source acts as the moniker provider and the container holding the link object acts as the moniker client.</span></span>

<span data-ttu-id="1db58-113">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="1db58-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="1db58-114">Клиенты моникера</span><span class="sxs-lookup"><span data-stu-id="1db58-114">Moniker Clients</span></span>](moniker-clients.md)
-   [<span data-ttu-id="1db58-115">Поставщики моникеров</span><span class="sxs-lookup"><span data-stu-id="1db58-115">Moniker Providers</span></span>](moniker-providers.md)
-   [<span data-ttu-id="1db58-116">Реализации моникера OLE</span><span class="sxs-lookup"><span data-stu-id="1db58-116">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)

## <a name="related-topics"></a><span data-ttu-id="1db58-117">См. также</span><span class="sxs-lookup"><span data-stu-id="1db58-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1db58-118">Модель COM</span><span class="sxs-lookup"><span data-stu-id="1db58-118">The Component Object Model</span></span>](the-component-object-model.md)
</dt> </dl>

 

 




