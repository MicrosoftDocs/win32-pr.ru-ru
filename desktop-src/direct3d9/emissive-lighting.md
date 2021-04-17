---
description: Излучаемое освещение описывается одним условием.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Освещение эмиссионный (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710564"
---
# <a name="emissive-lighting-direct3d-9"></a><span data-ttu-id="46aec-103">Освещение эмиссионный (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="46aec-103">Emissive Lighting (Direct3D 9)</span></span>

<span data-ttu-id="46aec-104">Излучаемое освещение описывается одним условием.</span><span class="sxs-lookup"><span data-stu-id="46aec-104">Emissive lighting is described by a single term.</span></span>

<span data-ttu-id="46aec-105">Излучаемое освещение = Cₑ</span><span class="sxs-lookup"><span data-stu-id="46aec-105">Emissive Lighting = Cₑ</span></span>

<span data-ttu-id="46aec-106">Где:</span><span class="sxs-lookup"><span data-stu-id="46aec-106">Where:</span></span>



| <span data-ttu-id="46aec-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="46aec-107">Parameter</span></span> | <span data-ttu-id="46aec-108">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="46aec-108">Default value</span></span> | <span data-ttu-id="46aec-109">Тип</span><span class="sxs-lookup"><span data-stu-id="46aec-109">Type</span></span>          | <span data-ttu-id="46aec-110">Описание</span><span class="sxs-lookup"><span data-stu-id="46aec-110">Description</span></span>     |
|-----------|---------------|---------------|-----------------|
| <span data-ttu-id="46aec-111">Cₑ</span><span class="sxs-lookup"><span data-stu-id="46aec-111">Cₑ</span></span>        | <span data-ttu-id="46aec-112">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="46aec-112">(0,0,0,0)</span></span>     | <span data-ttu-id="46aec-113">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="46aec-113">D3DCOLORVALUE</span></span> | <span data-ttu-id="46aec-114">Излучаемый цвет.</span><span class="sxs-lookup"><span data-stu-id="46aec-114">Emissive color.</span></span> |



 

<span data-ttu-id="46aec-115">Значение для C ₑ может быть следующим:</span><span class="sxs-lookup"><span data-stu-id="46aec-115">The value for Cₑ is either:</span></span>

-   <span data-ttu-id="46aec-116">Вершинный color1, если ЕМИССИВЕМАТЕРИАЛСАУРЦЕ = D3DMCS \_ color1, а первый цвет вершин указан в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="46aec-116">vertex color1, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="46aec-117">Вершинный color2, если ЕМИССИВЕМАТЕРИАЛСАУРЦЕ = D3DMCS \_ color2, а второй цвет вершин указан в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="46aec-117">vertex color2, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="46aec-118">цвет эмиссионный материала</span><span class="sxs-lookup"><span data-stu-id="46aec-118">material emissive color</span></span>

> [!Note]  
> <span data-ttu-id="46aec-119">Если используется параметр ЕМИССИВЕМАТЕРИАЛСАУРЦЕ и не указан цвет вершины, используется цвет материала эмиссионный.</span><span class="sxs-lookup"><span data-stu-id="46aec-119">If either EMISSIVEMATERIALSOURCE option is used, and the vertex color is not provided, the material emissive color is used.</span></span>

 

## <a name="example"></a><span data-ttu-id="46aec-120">Пример</span><span class="sxs-lookup"><span data-stu-id="46aec-120">Example</span></span>

<span data-ttu-id="46aec-121">В этом примере объект окрашен с помощью внешнего света сцены и внешнего цвета материала.</span><span class="sxs-lookup"><span data-stu-id="46aec-121">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span> <span data-ttu-id="46aec-122">Код показан ниже.</span><span class="sxs-lookup"><span data-stu-id="46aec-122">The code is shown below.</span></span>


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="46aec-123">Согласно уравнению, полученный цвет вершин объекта — это цвет материала.</span><span class="sxs-lookup"><span data-stu-id="46aec-123">According to the equation, the resulting color for the object vertices is the material color.</span></span>

<span data-ttu-id="46aec-124">На следующей иллюстрации показан цвет материала, то есть зеленый.</span><span class="sxs-lookup"><span data-stu-id="46aec-124">The following illustration shows the material color, which is green.</span></span> <span data-ttu-id="46aec-125">Излучаемый свет освещает все вершины объекта одним и тем же цветом.</span><span class="sxs-lookup"><span data-stu-id="46aec-125">Emissive light lights all object vertices with the same color.</span></span> <span data-ttu-id="46aec-126">Это не зависит от нормали вершины или направления света.</span><span class="sxs-lookup"><span data-stu-id="46aec-126">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="46aec-127">В результате сфера выглядит как двухмерный круг, поскольку затенение вокруг поверхности объекта одинаковое.</span><span class="sxs-lookup"><span data-stu-id="46aec-127">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![иллюстрация зеленой сферы](images/lighte.jpg)

<span data-ttu-id="46aec-129">На следующем рисунке показано, как эмиссионный Light смешивается с другими тремя типами индикаторов из предыдущих примеров.</span><span class="sxs-lookup"><span data-stu-id="46aec-129">The following illustration shows how the emissive light blends with the other three types of lights, from the previous examples.</span></span> <span data-ttu-id="46aec-130">С правой стороны сферы смешиваются зеленое излучаемое и красное внешнее освещение.</span><span class="sxs-lookup"><span data-stu-id="46aec-130">On the right side of the sphere, there is a blend of the green emissive and the red ambient light.</span></span> <span data-ttu-id="46aec-131">С левой стороны сферы зеленое излучаемое освещение смешивается с красным внешним и рассеянным освещением, в результате чего получается красный градиент.</span><span class="sxs-lookup"><span data-stu-id="46aec-131">On the left side of the sphere, the green emissive light blends with red ambient and diffuse light producing a red gradient.</span></span> <span data-ttu-id="46aec-132">Вокруг светового блика в центре появилось желтое кольцо, так как значение отраженного света резко падает, оставляя значения внешнего, рассеянного и излучаемого освещения, которые при смешении дают желтый цвет.</span><span class="sxs-lookup"><span data-stu-id="46aec-132">The specular highlight is white in the center and creates a yellow ring as the specular light value falls off sharply leaving the ambient, diffuse and emissive light values which blend together to make yellow.</span></span>

![иллюстрация зеленой сферы с излучаемым освещением](images/lightadse.jpg)

## <a name="related-topics"></a><span data-ttu-id="46aec-134">См. также</span><span class="sxs-lookup"><span data-stu-id="46aec-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46aec-135">Математика освещения</span><span class="sxs-lookup"><span data-stu-id="46aec-135">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



