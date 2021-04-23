---
title: Создание связанных и внедренных объектов из существующих данных
description: Создание связанных и внедренных объектов из существующих данных
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779802"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a><span data-ttu-id="e6429-103">Создание связанных и внедренных объектов из существующих данных</span><span class="sxs-lookup"><span data-stu-id="e6429-103">Creating Linked and Embedded Objects from Existing Data</span></span>

<span data-ttu-id="e6429-104">Пользователь обычно собирает составной документ с помощью буфера обмена или перетаскивания, чтобы скопировать объект данных из серверного приложения в приложение-контейнер пользователя.</span><span class="sxs-lookup"><span data-stu-id="e6429-104">A user typically assembles a compound document by using either the clipboard or drag and drop to copy a data object from its server application to the user's container application.</span></span> <span data-ttu-id="e6429-105">При использовании приложений, поддерживающих OLE, пользователь может инициировать перемещение с сервера или из контейнера.</span><span class="sxs-lookup"><span data-stu-id="e6429-105">With applications that support OLE, the user can initiate the transfer from either the server or the container.</span></span> <span data-ttu-id="e6429-106">Например, сервер может скопировать данные в буфер обмена в серверном приложении, затем переключиться в приложение-контейнер и выбрать пункт Вставить специальный/внедренный объект или эквивалентную команду меню, чтобы создать новый внедренный объект из выбранных данных.</span><span class="sxs-lookup"><span data-stu-id="e6429-106">For example, the server can copy data to the clipboard in the server application, then switch to the container application and choose Paste Special/Embedded Object or an equivalent menu command to create a new embedded object from the selected data.</span></span> <span data-ttu-id="e6429-107">Или же пользователь может перетащить данные из одного приложения в другое.</span><span class="sxs-lookup"><span data-stu-id="e6429-107">Or, the user can drag the data from one application to the other.</span></span> <span data-ttu-id="e6429-108">Процесс аналогичен созданию связанного объекта.</span><span class="sxs-lookup"><span data-stu-id="e6429-108">The process is similar for creating a linked object.</span></span>

> [!Note]  
> <span data-ttu-id="e6429-109">Приложение, которое работает как OLE-сервер и контейнер, может использовать выбор собственных данных для создания внедренного или связанного объекта в новом месте в том же документе.</span><span class="sxs-lookup"><span data-stu-id="e6429-109">An application that functions as both OLE server and container can use a selection of its own data to create an embedded or linked object at a new location within the same document.</span></span>

 

<span data-ttu-id="e6429-110">Обмен данными между сервером OLE и приложениями-контейнерами основан на равномерном переносе данных, как описано в [Передача данных](data-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="e6429-110">Data transfer between OLE server and container applications is built on uniform data transfer, as described in [Data Transfer](data-transfer.md).</span></span> <span data-ttu-id="e6429-111">Серверы OLE и обработчики объектов реализуют интерфейс [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , чтобы сделать их данные доступными для передачи с помощью буфера обмена или перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="e6429-111">OLE servers and object handlers implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) in order to make their data available for transfers using either the clipboard or drag and drop.</span></span> <span data-ttu-id="e6429-112">Объекты OLE поддерживают все стандартные форматы буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="e6429-112">OLE objects support all the usual clipboard formats.</span></span> <span data-ttu-id="e6429-113">Кроме того, они поддерживают шесть форматов буфера обмена, которые поддерживают создание связанных и внедренных объектов из выбранного объекта данных.</span><span class="sxs-lookup"><span data-stu-id="e6429-113">In addition, they support six clipboard formats that support the creation of linked and embedded objects from a selected data object.</span></span>

<span data-ttu-id="e6429-114">Форматы буфера обмена OLE описывают объекты данных, которые, при удалении или вставлении в контейнеры OLE, становятся внедренными или связанными объектами составных документов.</span><span class="sxs-lookup"><span data-stu-id="e6429-114">OLE clipboard formats describe data objects that, upon being dropped or pasted in OLE containers, are to become embedded or linked compound-document objects.</span></span> <span data-ttu-id="e6429-115">Объект данных представляет эти форматы приложениям контейнера в порядке их точности как описания данных.</span><span class="sxs-lookup"><span data-stu-id="e6429-115">The data object presents these formats to container applications in order of their fidelity as descriptions of the data.</span></span> <span data-ttu-id="e6429-116">Иными словами, объект сначала представляет формат, который лучше всего соответствует ему, затем — следующий наилучший формат и т. д.</span><span class="sxs-lookup"><span data-stu-id="e6429-116">In other words, the object presents first the format that best represents it, followed by the next best format, and so on.</span></span> <span data-ttu-id="e6429-117">Это преднамеренное упорядочение способствует использованию приложением-контейнером лучшего возможного формата.</span><span class="sxs-lookup"><span data-stu-id="e6429-117">This intentional ordering encourages a container application to use the best possible format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6429-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e6429-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6429-119">Составные документы</span><span class="sxs-lookup"><span data-stu-id="e6429-119">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="e6429-120">Передача данных</span><span class="sxs-lookup"><span data-stu-id="e6429-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




