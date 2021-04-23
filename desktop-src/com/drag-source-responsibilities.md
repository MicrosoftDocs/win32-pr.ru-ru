---
title: Перетаскивание исходных обязанностей
description: Перетаскивание исходных обязанностей
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105691670"
---
# <a name="drag-source-responsibilities"></a><span data-ttu-id="9b058-103">Перетаскивание исходных обязанностей</span><span class="sxs-lookup"><span data-stu-id="9b058-103">Drag Source Responsibilities</span></span>

<span data-ttu-id="9b058-104">Источник перетаскивания отвечает за следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="9b058-104">The drag source is responsible for the following tasks:</span></span>

-   <span data-ttu-id="9b058-105">Предоставление объекта для переноса данных для целевого объекта перетаскивания, предоставляющего интерфейсы [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) и [**идропсаурце**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .</span><span class="sxs-lookup"><span data-stu-id="9b058-105">Providing a data-transfer object for the drop target that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span>
-   <span data-ttu-id="9b058-106">Создание отзыва указателя и источника.</span><span class="sxs-lookup"><span data-stu-id="9b058-106">Generating pointer and source feedback.</span></span>
-   <span data-ttu-id="9b058-107">Определение, когда операция перетаскивания была отменена или произошла операция удаления.</span><span class="sxs-lookup"><span data-stu-id="9b058-107">Determining when the drag operation has been canceled or a drop operation has occurred.</span></span>
-   <span data-ttu-id="9b058-108">Выполнение любых действий с исходными данными, вызванными операцией Drop, например удалением данных или созданием ссылки на нее.</span><span class="sxs-lookup"><span data-stu-id="9b058-108">Performing any action on the original data caused by the drop operation, such as deleting the data or creating a link to it.</span></span>

<span data-ttu-id="9b058-109">Основная задача — создание объекта для перемещения данных, предоставляющего интерфейсы [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) и [**идропсаурце**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .</span><span class="sxs-lookup"><span data-stu-id="9b058-109">The main task is creating a data-transfer object that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span> <span data-ttu-id="9b058-110">Источник перетаскивания может содержать или не включать копию выбранных данных.</span><span class="sxs-lookup"><span data-stu-id="9b058-110">The drag source might or might not include a copy of the selected data.</span></span> <span data-ttu-id="9b058-111">Включение не является обязательным, но это помогает защититься от непреднамеренного изменения и позволяет коду операций с буфером обмена быть идентичен коду перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="9b058-111">Including it is not mandatory, but doing so helps protect against inadvertent changes and allows the Clipboard operations code to be identical to the drag and drop code.</span></span>

<span data-ttu-id="9b058-112">Пока выполняется операция перетаскивания, источник перетаскивания отвечает за установку указателя мыши и, при необходимости, для предоставления пользователю дополнительных отзывов об источнике.</span><span class="sxs-lookup"><span data-stu-id="9b058-112">While a drag operation is in progress, the drag source is responsible for setting the mouse pointer and, if appropriate, for providing additional source feedback to the user.</span></span> <span data-ttu-id="9b058-113">Источник перетаскивания не может предоставить отзыв, который отслеживает расположение мыши, отличное от фактической установки указателя (см. функцию [**сеткурсор**](/windows/win32/api/winuser/nf-winuser-setcursor) ).</span><span class="sxs-lookup"><span data-stu-id="9b058-113">The drag source cannot provide any feedback that tracks the mouse position other than by actually setting the real pointer (see the [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) function).</span></span> <span data-ttu-id="9b058-114">Это правило должно быть применено во избежание конфликтов с отзывом, предоставленным целью перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="9b058-114">This rule must be enforced to avoid conflicts with the feedback provided by the drop target.</span></span> <span data-ttu-id="9b058-115">(Источник перетаскивания также может быть целевым объектом перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="9b058-115">(A drag source can also be a drop target.</span></span> <span data-ttu-id="9b058-116">При удалении самого себя источник или цель, конечно же, могут предоставить обратную связь, чтобы отвести указатель мыши.</span><span class="sxs-lookup"><span data-stu-id="9b058-116">When dropping on itself, the source/target can, of course, provide target feedback to track the mouse position.</span></span> <span data-ttu-id="9b058-117">Однако в данном случае это объект перетаскивания, отслеживающий мышь, а не источник.) Исходя из отзывов, предлагаемых целью перетаскивания, источник устанавливает соответствующий указатель.</span><span class="sxs-lookup"><span data-stu-id="9b058-117">In this case, however, it is the drop target tracking the mouse, not the source.) Based on the feedback offered by the drop target, the source sets an appropriate pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b058-118">См. также</span><span class="sxs-lookup"><span data-stu-id="9b058-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b058-119">Перетаскивание</span><span class="sxs-lookup"><span data-stu-id="9b058-119">Drag and Drop</span></span>](drag-and-drop.md)
</dt> </dl>

 

 