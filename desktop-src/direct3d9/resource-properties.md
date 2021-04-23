---
description: Все ресурсы совместно используют следующие свойства.
ms.assetid: 6ef6ce68-44fa-4964-8b61-2a37382eda1c
title: Свойства ресурсов (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7b53a23e489b5f53495c5d2626da1e2633c9cf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806526"
---
# <a name="resource-properties-direct3d-9"></a><span data-ttu-id="6a19b-103">Свойства ресурсов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6a19b-103">Resource Properties (Direct3D 9)</span></span>

<span data-ttu-id="6a19b-104">Все ресурсы совместно используют следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6a19b-104">All resources share the following properties.</span></span>

-   <span data-ttu-id="6a19b-105">Использование.</span><span class="sxs-lookup"><span data-stu-id="6a19b-105">Usage.</span></span> <span data-ttu-id="6a19b-106">Способ использования ресурса, например, текстуры или целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="6a19b-106">The way a resource is used, for example, as a texture or a render target.</span></span>
-   <span data-ttu-id="6a19b-107">Выполните форматирование.</span><span class="sxs-lookup"><span data-stu-id="6a19b-107">Format.</span></span> <span data-ttu-id="6a19b-108">Формат данных, например формат пикселей двухмерной поверхности.</span><span class="sxs-lookup"><span data-stu-id="6a19b-108">The format of the data, for example, the pixel format of a 2D surface.</span></span>
-   <span data-ttu-id="6a19b-109">Подключений.</span><span class="sxs-lookup"><span data-stu-id="6a19b-109">Pool.</span></span> <span data-ttu-id="6a19b-110">Тип памяти, в которой выделяется ресурс.</span><span class="sxs-lookup"><span data-stu-id="6a19b-110">The type of memory where the resource is allocated.</span></span>
-   <span data-ttu-id="6a19b-111">Введите ,</span><span class="sxs-lookup"><span data-stu-id="6a19b-111">Type.</span></span> <span data-ttu-id="6a19b-112">Тип ресурса, например буфер вершин или целевой объект прорисовки.</span><span class="sxs-lookup"><span data-stu-id="6a19b-112">The type of resource, for example, a vertex buffer or render target.</span></span>

<span data-ttu-id="6a19b-113">Применяются все используемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="6a19b-113">Resource uses are enforced.</span></span> <span data-ttu-id="6a19b-114">Приложение, которое будет использовать ресурс в определенной операции, должно указать эту операцию во время создания ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a19b-114">An application that will use a resource in a certain operation must specify that operation at resource-creation time.</span></span> <span data-ttu-id="6a19b-115">Список констант использования, определенных для ресурсов, см. в разделе [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="6a19b-115">For a list of the usage constants defined for resources, see [**D3DUSAGE**](d3dusage.md).</span></span>

<span data-ttu-id="6a19b-116">\_Константы D3DUSAGE ртпатчес, D3DUSAGE \_ НПАТЧЕС и D3DUSAGE \_ указывают драйверу, что данные в этих буферах, скорее всего, будут использоваться для треугольных или исправлений, N-патчей или спрайтов, соответственно.</span><span class="sxs-lookup"><span data-stu-id="6a19b-116">The D3DUSAGE\_RTPATCHES, D3DUSAGE\_NPATCHES, and D3DUSAGE\_POINTS constants indicate to the driver that the data in these buffers is likely to be used for triangular or grid patches, N-patches, or point sprites, respectively.</span></span> <span data-ttu-id="6a19b-117">Эти флаги предоставляются в том случае, если оборудование не может выполнять эти операции без обработки узла.</span><span class="sxs-lookup"><span data-stu-id="6a19b-117">These flags are provided in case the hardware cannot perform these operations without host processing.</span></span> <span data-ttu-id="6a19b-118">Поэтому драйверу потребуется выделить эти поверхности в системной памяти, чтобы ЦП мог получить к ним доступ.</span><span class="sxs-lookup"><span data-stu-id="6a19b-118">Therefore, the driver will want to allocate these surfaces in system memory so that the CPU can access them.</span></span> <span data-ttu-id="6a19b-119">Если драйвер может выполнять эти операции полностью в аппаратном обеспечении, он может выделить эти поверхности в видеопамяти или AGP, чтобы избежать копирования узлов и повысить производительность по крайней мере двойная.</span><span class="sxs-lookup"><span data-stu-id="6a19b-119">If the driver can perform these operations entirely in hardware, it can allocate these surfaces in video or AGP memory to avoid a host copy and improve performance at least twofold.</span></span> <span data-ttu-id="6a19b-120">Обратите внимание, что сведения, предоставленные этими флагами, не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="6a19b-120">Note that the information provided by these flags is not absolutely required.</span></span> <span data-ttu-id="6a19b-121">Драйвер может обнаружить, что такие операции выполняются с данными, и переместит буфер обратно в системную память для последующих кадров.</span><span class="sxs-lookup"><span data-stu-id="6a19b-121">A driver can detect that such operations are being performed on the data, and it will move the buffer back to system memory for subsequent frames.</span></span>

<span data-ttu-id="6a19b-122">Дополнительные сведения о флагах использования и о том, как они связаны с конкретными ресурсами, см. на справочных страницах по отдельным методам создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a19b-122">For details about the usage flags and how they relate to specific resources, see the reference pages on the individual resource creation methods.</span></span>

<span data-ttu-id="6a19b-123">Сведения о формате поверхности ресурсов см. в разделе перечислимый тип [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="6a19b-123">For information about the surface format of resources, see the [D3DFORMAT](d3dformat.md) enumerated type.</span></span>

<span data-ttu-id="6a19b-124">Класс памяти, в которой хранятся буферы ресурса, называется пулом.</span><span class="sxs-lookup"><span data-stu-id="6a19b-124">The class of memory that holds a resource's buffers is called a pool.</span></span> <span data-ttu-id="6a19b-125">Значения пула определяются перечисляемым типом [**D3DPOOL**](./d3dpool.md) .</span><span class="sxs-lookup"><span data-stu-id="6a19b-125">Pool values are defined by the [**D3DPOOL**](./d3dpool.md) enumerated type.</span></span> <span data-ttu-id="6a19b-126">Пул не может быть смешанным для различных объектов, содержащихся в одном ресурсе, т. е. MIP уровней в mipmap-и при выборе пула для ресурса пул нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="6a19b-126">A pool cannot be mixed for different objects contained in a single resource - that is, mip levels in a mipmap - and, when a pool is chosen for a resource, the pool cannot be changed.</span></span>

<span data-ttu-id="6a19b-127">Типы ресурсов задаются неявно во время выполнения, когда приложение вызывает метод создания ресурса, например [**IDirect3DDevice9:: креатекубетекстуре**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="6a19b-127">The resources types are set implicitly at run time when the application calls a resource creation method such as [**IDirect3DDevice9::CreateCubeTexture**](/windows/desktop/api).</span></span> <span data-ttu-id="6a19b-128">Типы ресурсов определяются перечисляемым типом [**D3DRESOURCETYPE**](./d3dresourcetype.md) .</span><span class="sxs-lookup"><span data-stu-id="6a19b-128">Resource types are defined by the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type.</span></span> <span data-ttu-id="6a19b-129">Приложения могут запрашивать эти типы во время выполнения; Однако предполагается, что для большинства сценариев проверка типов во время выполнения не требуется.</span><span class="sxs-lookup"><span data-stu-id="6a19b-129">Applications can query these types at run time; however, it is expected that most scenarios will not require run-time type checking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a19b-130">См. также</span><span class="sxs-lookup"><span data-stu-id="6a19b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a19b-131">Ресурсы Direct3D</span><span class="sxs-lookup"><span data-stu-id="6a19b-131">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 
