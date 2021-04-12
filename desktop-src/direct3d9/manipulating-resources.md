---
description: Приложение управляет ресурсами для отображения сцены.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Управление ресурсами (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416368"
---
# <a name="manipulating-resources-direct3d-9"></a><span data-ttu-id="6fd3b-103">Управление ресурсами (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6fd3b-103">Manipulating Resources (Direct3D 9)</span></span>

<span data-ttu-id="6fd3b-104">Приложение управляет ресурсами для отображения сцены.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-104">Your application manipulates resources in order to render a scene.</span></span> <span data-ttu-id="6fd3b-105">Сначала приложению необходимо создать ресурс текстуры с помощью одного из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="6fd3b-105">First, an application needs to create a texture resource with one of the following methods:</span></span>

-   [<span data-ttu-id="6fd3b-106">**IDirect3DDevice9:: Креатекубетекстуре**</span><span class="sxs-lookup"><span data-stu-id="6fd3b-106">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="6fd3b-107">**IDirect3DDevice9:: Креатетекстуре**</span><span class="sxs-lookup"><span data-stu-id="6fd3b-107">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="6fd3b-108">**IDirect3DDevice9:: Креатеволуметекстуре**</span><span class="sxs-lookup"><span data-stu-id="6fd3b-108">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

<span data-ttu-id="6fd3b-109">Вместо этого можно создать ресурс текстуры с помощью одной из функций текстурирования D3DXCreatexxx.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-109">A texture resource can instead be created with one of the D3DXCreatexxx texturing functions.</span></span>

<span data-ttu-id="6fd3b-110">Объекты текстуры, возвращаемые методами создания текстуры, являются контейнерами для поверхностей или томов. Эти контейнеры являются универсальными и называются буферами.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-110">The texture objects returned by the texture creation methods are containers for surfaces or volumes; these containers are generically known as buffers.</span></span> <span data-ttu-id="6fd3b-111">Буферы, принадлежащие ресурсу, наследуют использование, формат и пул ресурса, но имеют собственный тип.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-111">The buffers owned by the resource inherit the usages, format, and pool of the resource but have their own type.</span></span> <span data-ttu-id="6fd3b-112">Дополнительные сведения см. в разделе [свойства ресурсов (Direct3D 9)](resource-properties.md).</span><span class="sxs-lookup"><span data-stu-id="6fd3b-112">For more information, see [Resource Properties (Direct3D 9)](resource-properties.md).</span></span>

<span data-ttu-id="6fd3b-113">Приложение получает доступ к содержащимся в них поверхностям для загрузки иллюстраций, вызывая следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-113">The application gains access to the contained surfaces, for the purpose of loading artwork, by calling the following methods.</span></span> <span data-ttu-id="6fd3b-114">Дополнительные сведения см. в разделе [Блокировка ресурсов (Direct3D 9)](locking-resources.md).</span><span class="sxs-lookup"><span data-stu-id="6fd3b-114">For details, see [Locking Resources (Direct3D 9)](locking-resources.md).</span></span>

-   [<span data-ttu-id="6fd3b-115">**IDirect3DCubeTexture9:: Локкрект**</span><span class="sxs-lookup"><span data-stu-id="6fd3b-115">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [<span data-ttu-id="6fd3b-116">**IDirect3DTexture9:: Локкрект**</span><span class="sxs-lookup"><span data-stu-id="6fd3b-116">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [<span data-ttu-id="6fd3b-117">**IDirect3DVolumeTexture9:: защищенное хранилище**</span><span class="sxs-lookup"><span data-stu-id="6fd3b-117">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

<span data-ttu-id="6fd3b-118">Методы блокировки принимают аргументы, обозначающие содержащуюся поверхность, например, вложенный уровень mipmap или грань куба текстуры, а также указатели на пиксели.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-118">The lock methods take arguments denoting the contained surface - for example, the mipmap sub-level or cube face of the texture - and return pointers to the pixels.</span></span> <span data-ttu-id="6fd3b-119">Обычное приложение никогда не использует объект Surface напрямую.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-119">The typical application never uses a surface object directly.</span></span>

<span data-ttu-id="6fd3b-120">Создайте ресурсы, ориентированные на геометрические вызовы, вызвав [**IDirect3DDevice9:: креатеиндексбуффер**](/windows/desktop/api) или [**IDirect3DDevice9:: креатевертексбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span><span class="sxs-lookup"><span data-stu-id="6fd3b-120">Create geometry-oriented resources by calling [**IDirect3DDevice9::CreateIndexBuffer**](/windows/desktop/api) or [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span></span>

<span data-ttu-id="6fd3b-121">Заблокируйте и заполните ресурсы буфера, вызвав либо [**IDirect3DIndexBuffer9:: Lock**](/windows/desktop/api) , либо [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), в зависимости от ресурса.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-121">Lock and fill the buffer resources by calling either [**IDirect3DIndexBuffer9::Lock**](/windows/desktop/api) or [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), depending upon the resource.</span></span>

<span data-ttu-id="6fd3b-122">Для управляемых ресурсов текстуры процесс создания ресурса завершается здесь.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-122">For managed texture resources, the resource creation process ends here.</span></span> <span data-ttu-id="6fd3b-123">Для неуправляемых ресурсов текстуры приложение передает ресурсы системной памяти в ресурсы, доступные для устройства (для аппаратного ускорения) путем вызова [**IDirect3DDevice9:: упдатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span><span class="sxs-lookup"><span data-stu-id="6fd3b-123">For non-managed texture resources, an application promotes system memory resources to device-accessible resources (for hardware acceleration) by calling [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

<span data-ttu-id="6fd3b-124">Для отображения изображений, подготовленных к просмотру из ресурсов, приложению также требуются буферы цветов и элементов глубины.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-124">To present images rendered from resources, the application also needs color and depth-stencil buffers.</span></span> <span data-ttu-id="6fd3b-125">Для типичных приложений буфер цвета принадлежит цепочке подкачки устройства, которая представляет собой коллекцию поверхностей заднего буфера и неявно создается на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6fd3b-125">For typical applications, the color buffer is owned by the device's swap chain, which is a collection of back-buffer surfaces, and is implicitly created with the device.</span></span> <span data-ttu-id="6fd3b-126">Поверхности набора элементов глубины могут быть неявно созданы или явно созданы с помощью метода [**IDirect3DDevice9:: креатедепсстенЦилсурфаце**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="6fd3b-126">Depth-stencil surfaces can be implicitly created, or explicitly created by using the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="6fd3b-127">Приложение связывает устройство, его глубину и буфер цвета с вызовом [**IDirect3DDevice9:: сетрендертаржет**](/windows/desktop/api) или [**IDirect3DDevice9:: сетдепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span><span class="sxs-lookup"><span data-stu-id="6fd3b-127">The application associates a device and its depth and color buffer with a call to [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) or [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span></span>

<span data-ttu-id="6fd3b-128">Дополнительные сведения о представлении окончательного образа см. в разделе [представление сцены (Direct3D 9)](presenting-a-scene.md).</span><span class="sxs-lookup"><span data-stu-id="6fd3b-128">For details on presenting the final image, see [Presenting a Scene (Direct3D 9)](presenting-a-scene.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fd3b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="6fd3b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fd3b-130">Ресурсы Direct3D</span><span class="sxs-lookup"><span data-stu-id="6fd3b-130">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 
