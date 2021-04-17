---
title: Клиенты моникера
description: Клиенты моникера должны начать с получения моникера, и для клиента моникера существует несколько способов получения моникера.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681378"
---
# <a name="moniker-clients"></a><span data-ttu-id="6da9f-103">Клиенты моникера</span><span class="sxs-lookup"><span data-stu-id="6da9f-103">Moniker Clients</span></span>

<span data-ttu-id="6da9f-104">Клиенты моникера должны начать с получения моникера, и для клиента моникера существует несколько способов получения моникера.</span><span class="sxs-lookup"><span data-stu-id="6da9f-104">Moniker clients must start by getting a moniker, and there are several ways for a moniker client to get a moniker.</span></span> <span data-ttu-id="6da9f-105">Например, в составных документах OLE, когда пользователь создает связанный элемент (с помощью диалогового окна « **Вставка объекта** », буфера обмена или перетаскивания), моникер внедряется как часть связанного элемента.</span><span class="sxs-lookup"><span data-stu-id="6da9f-105">For example, in OLE compound documents, when the end user creates a linked item (either using **Insert Object** dialog, the clipboard, or drag-and drop), a moniker is embedded as part of the linked item.</span></span> <span data-ttu-id="6da9f-106">В этом случае программист имеет минимальное Контактное имя с моникерами.</span><span class="sxs-lookup"><span data-stu-id="6da9f-106">In that case, the programmer has minimal contact with monikers.</span></span> <span data-ttu-id="6da9f-107">Программно, если у вас есть указатель интерфейса на объект, реализующий интерфейс [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , его можно использовать для получения моникера, а для других интерфейсов, которые определены для возврата моникеров, существуют методы.</span><span class="sxs-lookup"><span data-stu-id="6da9f-107">Programmatically, if you have an interface pointer to an object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface, you can use that to get a moniker, and there are methods on other interfaces that are defined to return monikers.</span></span>

<span data-ttu-id="6da9f-108">Существуют различные разновидности моникеров, которые используются для обнаружения различных типов объектов, но для клиента моникера все имена моникеров выглядят одинаково.</span><span class="sxs-lookup"><span data-stu-id="6da9f-108">There are different kinds of monikers, which are used to identify different kinds of objects, but to a moniker client, all monikers look the same.</span></span> <span data-ttu-id="6da9f-109">Клиент моникера просто вызывает [**IMoniker:: биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) в моникере и получает указатель интерфейса на объект, идентифицируемый моникером.</span><span class="sxs-lookup"><span data-stu-id="6da9f-109">A moniker client simply calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on a moniker and gets an interface pointer to the object that the moniker identifies.</span></span> <span data-ttu-id="6da9f-110">Независимо от того, определяет ли моникер объект как целую электронную таблицу или как маленькую как одну ячейку в таблице, вызов **биндтубжект** вернет указатель на этот объект.</span><span class="sxs-lookup"><span data-stu-id="6da9f-110">Whether the moniker identifies an object as large as an entire spreadsheet or as small as a single cell within a spreadsheet, calling **BindToObject** will return a pointer to that object.</span></span> <span data-ttu-id="6da9f-111">Если объект уже выполняется, **биндтубжект** найдет его в памяти.</span><span class="sxs-lookup"><span data-stu-id="6da9f-111">If the object is already running, **BindToObject** will find it in memory.</span></span> <span data-ttu-id="6da9f-112">Если объект хранится на диске, **биндтубжект** найдет сервер для этого объекта, запустит сервер и переместит объект в состояние выполняется.</span><span class="sxs-lookup"><span data-stu-id="6da9f-112">If the object is stored passively on disk, **BindToObject** will locate a server for that object, run the server, and have the server bring the object into the running state.</span></span> <span data-ttu-id="6da9f-113">Все сведения о процессе привязки скрыты от клиента моникера.</span><span class="sxs-lookup"><span data-stu-id="6da9f-113">All the details of the binding process are hidden from the moniker client.</span></span> <span data-ttu-id="6da9f-114">Таким же для клиента моникера Использование моникера очень просто.</span><span class="sxs-lookup"><span data-stu-id="6da9f-114">Thus, for a moniker client, using the moniker is very simple.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6da9f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="6da9f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6da9f-116">Поставщики моникеров</span><span class="sxs-lookup"><span data-stu-id="6da9f-116">Moniker Providers</span></span>](moniker-providers.md)
</dt> <dt>

[<span data-ttu-id="6da9f-117">Реализации моникера OLE</span><span class="sxs-lookup"><span data-stu-id="6da9f-117">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




