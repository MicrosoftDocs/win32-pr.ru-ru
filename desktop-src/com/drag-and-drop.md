---
title: Перетаскивание
description: Перетаскивание означает передачу данных, в которой используется мышь или другое указывающее устройство для указания источника данных и его назначения.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700581"
---
# <a name="drag-and-drop"></a><span data-ttu-id="dafe4-103">Перетаскивание</span><span class="sxs-lookup"><span data-stu-id="dafe4-103">Drag and Drop</span></span>

<span data-ttu-id="dafe4-104">*Перетаскивание* означает передачу данных, в которой используется мышь или другое указывающее устройство для указания источника данных и его назначения.</span><span class="sxs-lookup"><span data-stu-id="dafe4-104">*Drag and drop* refers to data transfers in which a mouse or other pointing device is used to specify both the data source and its destination.</span></span> <span data-ttu-id="dafe4-105">В обычной операции перетаскивания пользователь выбирает объект для передачи, перемещая указатель мыши на него и удерживая нажатой левую кнопку или другую кнопку, обозначенную для этой цели.</span><span class="sxs-lookup"><span data-stu-id="dafe4-105">In a typical drag and drop operation, a user selects the object to be transferred by moving the mouse pointer to it and holding down either the left button or some other button designated for this purpose.</span></span> <span data-ttu-id="dafe4-106">Продолжая удерживать кнопку, пользователь инициирует перемещение, перетаскивая объект в место назначения, которое может быть любым контейнером OLE.</span><span class="sxs-lookup"><span data-stu-id="dafe4-106">While continuing to hold down the button, the user initiates the transfer by dragging the object to its destination, which can be any OLE container.</span></span> <span data-ttu-id="dafe4-107">Перетаскивание предоставляет те же функции, что и копирование и вставка в буфер обмена OLE, но добавляет визуальный отзыв и устраняет необходимость в меню.</span><span class="sxs-lookup"><span data-stu-id="dafe4-107">Drag and drop provides exactly the same functionality as the OLE clipboard copy and paste but adds visual feedback and eliminates the need for menus.</span></span> <span data-ttu-id="dafe4-108">На самом деле, если приложение поддерживает копирование и вставку в буфер обмена, для поддержки перетаскивания требуется небольшое дополнительное значение.</span><span class="sxs-lookup"><span data-stu-id="dafe4-108">In fact, if an application supports clipboard copy and paste, little extra is needed to support drag and drop.</span></span>

<span data-ttu-id="dafe4-109">Во время операции перетаскивания OLE используются следующие три отдельных фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="dafe4-109">During an OLE drag and drop operation, the following three separate pieces of code are used.</span></span>



| <span data-ttu-id="dafe4-110">Источник кода для перетаскивания</span><span class="sxs-lookup"><span data-stu-id="dafe4-110">Drag-and-drop code source</span></span>                               | <span data-ttu-id="dafe4-111">Реализация и использование</span><span class="sxs-lookup"><span data-stu-id="dafe4-111">Implementation and use</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dafe4-112">Интерфейс [**идропсаурце**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)</span><span class="sxs-lookup"><span data-stu-id="dafe4-112">[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interface</span></span><br/> | <span data-ttu-id="dafe4-113">Реализуется объектом, содержащим перетаскиваемые данные, называемый *источником перетаскивания*.</span><span class="sxs-lookup"><span data-stu-id="dafe4-113">Implemented by the object containing the dragged data, referred to as the *drag source*.</span></span><br/>                                                                                         |
| <span data-ttu-id="dafe4-114">Интерфейс [**интерфейс IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)</span><span class="sxs-lookup"><span data-stu-id="dafe4-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interface</span></span><br/> | <span data-ttu-id="dafe4-115">Реализуется объектом, который предназначен для принятия удаления, называемый *целью перетаскивания*.</span><span class="sxs-lookup"><span data-stu-id="dafe4-115">Implemented by the object that is intended to accept the drop, referred to as the *drop target*.</span></span><br/>                                                                                 |
| <span data-ttu-id="dafe4-116">Функция [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)</span><span class="sxs-lookup"><span data-stu-id="dafe4-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function</span></span><br/>    | <span data-ttu-id="dafe4-117">Реализуется OLE и используется для инициации операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="dafe4-117">Implemented by OLE and used to initiate a drag and drop operation.</span></span> <span data-ttu-id="dafe4-118">После выполнения операции она упрощает обмен данными между источником перетаскивания и целевым объектом перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="dafe4-118">After the operation is in progress, it facilitates communication between the drag source and the drop target.</span></span><br/> |



 

<span data-ttu-id="dafe4-119">Интерфейсы [**идропсаурце**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) и [**интерфейс IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) могут быть реализованы либо в контейнере, либо в приложении объекта.</span><span class="sxs-lookup"><span data-stu-id="dafe4-119">The [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interfaces can be implemented in either a container or in an object application.</span></span> <span data-ttu-id="dafe4-120">Роль источника перетаскивания или цели перетаскивания не ограничена ни одним типом приложения OLE.</span><span class="sxs-lookup"><span data-stu-id="dafe4-120">The role of drag source or drop target is not limited to any one type of OLE application.</span></span>

<span data-ttu-id="dafe4-121">Функция OLE [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) реализует цикл, который отслеживает перемещение мыши и клавиатуры до тех пор, пока перетаскивание не будет отменено или происходит перетаскивание.</span><span class="sxs-lookup"><span data-stu-id="dafe4-121">The OLE function [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implements a loop that tracks mouse and keyboard movement until such time as the drag is canceled or a drop occurs.</span></span> <span data-ttu-id="dafe4-122">**DoDragDrop** является ключевой функцией в процессе перетаскивания, что упрощает обмен данными между источником перетаскивания и целевым объектом перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="dafe4-122">**DoDragDrop** is the key function in the drag and drop process, facilitating communication between the drag source and drop target.</span></span>

<span data-ttu-id="dafe4-123">Во время операции перетаскивания пользователю могут отображаться три типа отзывов.</span><span class="sxs-lookup"><span data-stu-id="dafe4-123">During a drag and drop operation, three types of feedback can be displayed to the user.</span></span>



| <span data-ttu-id="dafe4-124">Тип отзыва</span><span class="sxs-lookup"><span data-stu-id="dafe4-124">Type of feedback</span></span>            | <span data-ttu-id="dafe4-125">Описание</span><span class="sxs-lookup"><span data-stu-id="dafe4-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dafe4-126">Отзывы об источнике</span><span class="sxs-lookup"><span data-stu-id="dafe4-126">Source feedback</span></span><br/>  | <span data-ttu-id="dafe4-127">Обратная связь источника, предоставляемая источником перетаскивания, указывает, что данные перетаскиваются и не изменяются в процессе перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="dafe4-127">Provided by the drag source, the source feedback indicates the data is being dragged and does not change during the course of the drag.</span></span> <span data-ttu-id="dafe4-128">Как правило, данные выделяются, чтобы выдать сигнал выбранному.</span><span class="sxs-lookup"><span data-stu-id="dafe4-128">Typically, the data is highlighted to signal it has been selected.</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="dafe4-129">Отзыв указателя</span><span class="sxs-lookup"><span data-stu-id="dafe4-129">Pointer feedback</span></span><br/> | <span data-ttu-id="dafe4-130">Обратная связь указателя, предоставляемая источником перетаскивания, указывает, что произойдет, если мышь освобождается в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="dafe4-130">Provided by the drag source, the pointer feedback indicates what happens if the mouse is released at any given moment.</span></span> <span data-ttu-id="dafe4-131">Обратная связь с указателями постоянно меняется по мере того, как пользователь перемещает мышь и/или нажимает клавишу-модификатор.</span><span class="sxs-lookup"><span data-stu-id="dafe4-131">Pointer feedback changes continually as the user moves the mouse and/or presses a modifier key.</span></span> <span data-ttu-id="dafe4-132">Например, если указатель перемещается в окно, которое не принимает перетаскивание, указатель превращается в символ "не разрешено".</span><span class="sxs-lookup"><span data-stu-id="dafe4-132">For example, if the pointer is moved into a window that cannot accept a drop, the pointer changes to the "not allowed" symbol.</span></span><br/> |
| <span data-ttu-id="dafe4-133">Отзывы о цели</span><span class="sxs-lookup"><span data-stu-id="dafe4-133">Target feedback</span></span><br/>  | <span data-ttu-id="dafe4-134">Обратная связь целевого объекта перетаскивания указывает, где будет выполняться перетаскивание.</span><span class="sxs-lookup"><span data-stu-id="dafe4-134">Provided by the drop target, target feedback indicates where the drop is to occur.</span></span><br/>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="dafe4-135">Дополнительные сведения см. в разделе операции [перетаскивания источника](drag-source-responsibilities.md).</span><span class="sxs-lookup"><span data-stu-id="dafe4-135">For more information, see [Drag Source Responsibilities](drag-source-responsibilities.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dafe4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="dafe4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dafe4-137">Передача данных</span><span class="sxs-lookup"><span data-stu-id="dafe4-137">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 





