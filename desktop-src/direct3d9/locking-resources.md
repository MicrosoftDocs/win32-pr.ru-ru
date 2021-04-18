---
description: Блокировка ресурса означает предоставление ЦП доступа к своему хранилищу.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Блокировка ресурсов (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701137"
---
# <a name="locking-resources-direct3d-9"></a><span data-ttu-id="2d442-103">Блокировка ресурсов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2d442-103">Locking Resources (Direct3D 9)</span></span>

<span data-ttu-id="2d442-104">Блокировка ресурса означает предоставление ЦП доступа к своему хранилищу.</span><span class="sxs-lookup"><span data-stu-id="2d442-104">Locking a resource means granting CPU access to its storage.</span></span> <span data-ttu-id="2d442-105">Для ресурсов определены следующие параметры блокировки.</span><span class="sxs-lookup"><span data-stu-id="2d442-105">The following locking options are defined for resources:</span></span>

-   <span data-ttu-id="2d442-106">D3DLOCK \_ отбросить</span><span class="sxs-lookup"><span data-stu-id="2d442-106">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="2d442-107">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2d442-107">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="2d442-108">D3DLOCK \_ нуверврите</span><span class="sxs-lookup"><span data-stu-id="2d442-108">D3DLOCK\_NOOVERWRITE</span></span>
-   <span data-ttu-id="2d442-109">D3DLOCK \_ носислокк</span><span class="sxs-lookup"><span data-stu-id="2d442-109">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="2d442-110">D3DLOCK \_ без \_ "грязного" \_ обновления</span><span class="sxs-lookup"><span data-stu-id="2d442-110">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>

<span data-ttu-id="2d442-111">Дополнительные сведения о флагах блокировки и их связи с конкретными ресурсами см. на страницах справочника по отдельным методам блокировки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d442-111">For details on locking flags and how they relate to specific resources, see the reference pages on the individual resource locking methods.</span></span> <span data-ttu-id="2d442-112">Разработчикам приложений следует отметить, что \_ Флаги D3DLOCK Discard, D3DLOCK \_ ReadOnly и D3DLOCK \_ нуверврите являются указаниями.</span><span class="sxs-lookup"><span data-stu-id="2d442-112">Application developers should note that the D3DLOCK\_DISCARD, D3DLOCK\_READONLY, and D3DLOCK\_NOOVERWRITE flags are only hints.</span></span> <span data-ttu-id="2d442-113">Во время выполнения не проверяется, являются ли приложения следующими функциями, указанными в этих флагах.</span><span class="sxs-lookup"><span data-stu-id="2d442-113">The run time does not check that applications are following the functionality specified by these flags.</span></span> <span data-ttu-id="2d442-114">Приложение, которое указывает D3DLOCK \_ ReadOnly, но затем выполняет запись в ресурс, должно предполагать неопределенные результаты.</span><span class="sxs-lookup"><span data-stu-id="2d442-114">An application that specifies D3DLOCK\_READONLY but then writes to the resource should expect undefined results.</span></span> <span data-ttu-id="2d442-115">Как правило, работа с флагами блокировки, включая флаги блокировки использования, не гарантируется для работы в более поздних выпусках и может привести к значительному снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="2d442-115">In general, working against locking flags, including the locking usage flags, is not guaranteed to work in later releases and may incur a significant performance penalty.</span></span>

<span data-ttu-id="2d442-116">За операцией блокировки следует операция разблокировки.</span><span class="sxs-lookup"><span data-stu-id="2d442-116">A lock operation is followed by an unlock operation.</span></span> <span data-ttu-id="2d442-117">Например, после блокировки текстуры приложение впоследствии освобождает прямой доступ к заблокированным текстурам, разблокируя их.</span><span class="sxs-lookup"><span data-stu-id="2d442-117">For example, after locking a texture, the application subsequently relinquishes direct access to locked textures by unlocking them.</span></span> <span data-ttu-id="2d442-118">Помимо предоставления доступа к процессору, любые другие операции, включающие этот ресурс, сериализуются в течение блокировки.</span><span class="sxs-lookup"><span data-stu-id="2d442-118">In addition to granting processor access, any other operations involving that resource are serialized for the duration of a lock.</span></span> <span data-ttu-id="2d442-119">Разрешена только одна блокировка для ресурса, даже для неперекрывающихся регионов, и никакие операции ускорителя на поверхности не могут быть выполнены, пока операция блокировки не будет завершена на этой поверхности.</span><span class="sxs-lookup"><span data-stu-id="2d442-119">Only a single lock for a resource is allowed, even for non-overlapping regions, and no accelerator operations on a surface can be ongoing while a lock operation is outstanding on that surface.</span></span>

<span data-ttu-id="2d442-120">Каждый интерфейс ресурсов имеет методы для блокировки содержащихся буферов.</span><span class="sxs-lookup"><span data-stu-id="2d442-120">Each resource interface has methods for locking the contained buffers.</span></span> <span data-ttu-id="2d442-121">Каждый ресурс текстуры также может блокировать часть этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d442-121">Each texture resource can also lock a sub-portion of that resource.</span></span> <span data-ttu-id="2d442-122">2D-ресурсы (поверхности) позволяют блокировать подпрямоугольники, а ресурсы тома позволяют блокировать подразделы или поля.</span><span class="sxs-lookup"><span data-stu-id="2d442-122">2D resources (surfaces) allow the locking of sub-rectangles, and volume resources allow the locking of sub-volumes or boxes.</span></span> <span data-ttu-id="2d442-123">Каждый метод блокировки возвращает структуру, содержащую указатель на хранилище, в котором хранятся данные о ресурсе, и значения, представляющие расстояния между строками или плоскостями данных в зависимости от типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d442-123">Each lock method returns a structure that contains a pointer to the storage backing the resource and values representing the distances between rows or planes of data, depending on the resource type.</span></span> <span data-ttu-id="2d442-124">Дополнительные сведения см. в списке методов для интерфейсов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d442-124">For details, see the method lists for the resource interfaces.</span></span> <span data-ttu-id="2d442-125">Возвращаемый указатель всегда указывает на левый верхний байт в заблокированных областях.</span><span class="sxs-lookup"><span data-stu-id="2d442-125">The returned pointer always points to the top-left byte in the locked sub-regions.</span></span>

<span data-ttu-id="2d442-126">При работе с буферами индексов и вершин можно выполнять несколько вызовов блокировок. Однако необходимо убедиться, что количество вызовов блокировок соответствует числу вызовов Unlock.</span><span class="sxs-lookup"><span data-stu-id="2d442-126">When working with index and vertex buffers, you can make multiple lock calls; however, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="2d442-127">Дкстн сохраняет пиксели в закодированных блоках 4x4 и может блокироваться только на границах 4x4.</span><span class="sxs-lookup"><span data-stu-id="2d442-127">The DXTn store pixels in encoded 4x4 blocks, and can only be locked on 4x4 boundaries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d442-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2d442-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d442-129">Ресурсы Direct3D</span><span class="sxs-lookup"><span data-stu-id="2d442-129">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



