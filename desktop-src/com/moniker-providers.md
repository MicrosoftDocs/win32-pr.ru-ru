---
title: Поставщики моникеров
description: Поставщики моникеров
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775887"
---
# <a name="moniker-providers"></a><span data-ttu-id="f82d5-103">Поставщики моникеров</span><span class="sxs-lookup"><span data-stu-id="f82d5-103">Moniker Providers</span></span>

<span data-ttu-id="f82d5-104">Как правило, компонент должен быть поставщиком моникера, если он обеспечивает доступ к одному из его объектов, сохраняя при этом Управление хранилищем объекта.</span><span class="sxs-lookup"><span data-stu-id="f82d5-104">In general, a component should be a moniker provider when it allows access to one of its objects, while still controlling the object's storage.</span></span> <span data-ttu-id="f82d5-105">Если компонент собирает специальные имена, которые обозначают его объекты, он должен иметь возможность выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="f82d5-105">If a component is going to hand out monikers that identify its objects, it must be capable of performing the following tasks:</span></span>

-   <span data-ttu-id="f82d5-106">В запросе создайте моникер, определяющий объект.</span><span class="sxs-lookup"><span data-stu-id="f82d5-106">On request, create a moniker that identifies an object.</span></span>
-   <span data-ttu-id="f82d5-107">Включите привязку моникера, когда клиент вызывает [**IMoniker:: биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) .</span><span class="sxs-lookup"><span data-stu-id="f82d5-107">Enable the moniker to be bound when a client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on it.</span></span>

<span data-ttu-id="f82d5-108">Поставщик моникера должен создать моникер соответствующего *класса моникера* для обнаружения объекта.</span><span class="sxs-lookup"><span data-stu-id="f82d5-108">A moniker provider must create a moniker of an appropriate *moniker class* to identify an object.</span></span> <span data-ttu-id="f82d5-109">Класс моникера ссылается на определенную реализацию интерфейса [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , который определяет тип создаваемого моникера.</span><span class="sxs-lookup"><span data-stu-id="f82d5-109">The moniker class refers to a specific implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface that defines the type of moniker created.</span></span> <span data-ttu-id="f82d5-110">Хотя можно реализовать **IMoniker** для создания нового класса моникера, часто это не требуется, так как OLE предоставляет реализации нескольких различных классов моникеров, каждый из которых имеет собственный идентификатор CLSID.</span><span class="sxs-lookup"><span data-stu-id="f82d5-110">While you can implement **IMoniker** to create a new moniker class, it is frequently unnecessary because OLE provides implementations of several different moniker classes, each with its own CLSID.</span></span> <span data-ttu-id="f82d5-111">Описания классов моникера, предоставляемых OLE, см. в статье [Реализация моникера OLE](ole-moniker-implementations.md) .</span><span class="sxs-lookup"><span data-stu-id="f82d5-111">See [OLE Moniker Implementations](ole-moniker-implementations.md) for descriptions of moniker classes that OLE provides.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f82d5-112">См. также</span><span class="sxs-lookup"><span data-stu-id="f82d5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f82d5-113">Клиенты моникера</span><span class="sxs-lookup"><span data-stu-id="f82d5-113">Moniker Clients</span></span>](moniker-clients.md)
</dt> <dt>

[<span data-ttu-id="f82d5-114">Реализации моникера OLE</span><span class="sxs-lookup"><span data-stu-id="f82d5-114">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




