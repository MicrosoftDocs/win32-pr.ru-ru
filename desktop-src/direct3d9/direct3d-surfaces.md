---
description: Поверхность представляет собой линейную область отображения памяти и обычно находится в отображаемой памяти видеокарты, хотя поверхности могут существовать в системной памяти. Поверхности управляются интерфейсом IDirect3DSurface9.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Поверхности Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805200"
---
# <a name="direct3d-surfaces-direct3d-9"></a><span data-ttu-id="0aeb9-104">Поверхности Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-104">Direct3D Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="0aeb9-105">Поверхность представляет собой линейную область отображения памяти и обычно находится в отображаемой памяти видеокарты, хотя поверхности могут существовать в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-105">A surface represents a linear area of display memory and usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span> <span data-ttu-id="0aeb9-106">Поверхности управляются интерфейсом [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="0aeb9-106">Surfaces are managed by the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span>

-   <span data-ttu-id="0aeb9-107">Интерфейсный буфер.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-107">Front Buffer.</span></span> <span data-ttu-id="0aeb9-108">Прямоугольник памяти, который преобразуется графическим адаптером и отображается на мониторе.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-108">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span> <span data-ttu-id="0aeb9-109">В Direct3D приложение никогда не записывает данные непосредственно в передний буфер.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-109">In Direct3D an application never writes directly to the front buffer.</span></span>
-   <span data-ttu-id="0aeb9-110">Задний буфер.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-110">Back Buffer.</span></span> <span data-ttu-id="0aeb9-111">Прямоугольник памяти, в который приложение может непосредственно выполнять запись.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-111">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="0aeb9-112">Задний буфер никогда не отображается на мониторе напрямую.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-112">The back buffer is never directly displayed on the monitor.</span></span>
-   <span data-ttu-id="0aeb9-113">Зеркальное отображение поверхностей.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-113">Flipping surfaces.</span></span> <span data-ttu-id="0aeb9-114">Процесс перемещения заднего буфера в передний буфер.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-114">The process of moving the back buffer to the front buffer.</span></span>
-   <span data-ttu-id="0aeb9-115">Цепочка буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-115">Swap chain.</span></span> <span data-ttu-id="0aeb9-116">Коллекция из одного или нескольких задних буферов, которые могут быть последовательно представлены в интерфейсном буфере.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-116">A collection of one or more back buffers that can be serially presented to the front buffer.</span></span>

## <a name="getting-a-surface"></a><span data-ttu-id="0aeb9-117">Получение поверхности</span><span class="sxs-lookup"><span data-stu-id="0aeb9-117">Getting a Surface</span></span>

<span data-ttu-id="0aeb9-118">Создайте поверхность, вызвав любой из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="0aeb9-118">Create a surface by calling any of these methods:</span></span>

-   [<span data-ttu-id="0aeb9-119">**креатедепсстенЦилсурфаце**</span><span class="sxs-lookup"><span data-stu-id="0aeb9-119">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="0aeb9-120">**креатеоффскринплаинсурфаце**</span><span class="sxs-lookup"><span data-stu-id="0aeb9-120">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [<span data-ttu-id="0aeb9-121">**креатерендертаржет**</span><span class="sxs-lookup"><span data-stu-id="0aeb9-121">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

<span data-ttu-id="0aeb9-122">Форматы поверхности определяют, как интерпретируется данные для каждого пикселя в памяти поверхности.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-122">Surface formats determine how data for each pixel in surface memory is interpreted.</span></span> <span data-ttu-id="0aeb9-123">Для описания формата поверхности Direct3D использует элемент [D3DFORMAT](d3dformat.md) структуры [**D3DSURFACE \_ DESC**](d3dsurface-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="0aeb9-123">Direct3D uses the [D3DFORMAT](d3dformat.md) member of the [**D3DSURFACE\_DESC**](d3dsurface-desc.md) structure to describe the surface format.</span></span> <span data-ttu-id="0aeb9-124">Можно получить формат существующей поверхности, вызвав [**метод WebMethod**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) .</span><span class="sxs-lookup"><span data-stu-id="0aeb9-124">You can retrieve the format of an existing surface by calling the [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) method.</span></span>

<span data-ttu-id="0aeb9-125">После создания поверхности можно получить указатель на него, вызвав любой из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="0aeb9-125">Once a surface is created, you can get a pointer to it by calling any of these methods:</span></span>

-   [<span data-ttu-id="0aeb9-126">**жеткубемапсурфаце**</span><span class="sxs-lookup"><span data-stu-id="0aeb9-126">**GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [<span data-ttu-id="0aeb9-127">**жетбаккбуффер**</span><span class="sxs-lookup"><span data-stu-id="0aeb9-127">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="0aeb9-128">**жетдепсстенЦилсурфаце**</span><span class="sxs-lookup"><span data-stu-id="0aeb9-128">**GetDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [<span data-ttu-id="0aeb9-129">**жетфронтбуффердата**</span><span class="sxs-lookup"><span data-stu-id="0aeb9-129">**GetFrontBufferData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [<span data-ttu-id="0aeb9-130">**жетрендертаржет**</span><span class="sxs-lookup"><span data-stu-id="0aeb9-130">**GetRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [<span data-ttu-id="0aeb9-131">**жетбаккбуффер**</span><span class="sxs-lookup"><span data-stu-id="0aeb9-131">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="0aeb9-132">**жетсурфацелевел**</span><span class="sxs-lookup"><span data-stu-id="0aeb9-132">**GetSurfaceLevel**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

<span data-ttu-id="0aeb9-133">Интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) позволяет косвенно обращаться к памяти с помощью метода [**упдатесурфаце**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0aeb9-133">The [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface enables you to indirectly access memory through the [**UpdateSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="0aeb9-134">Этот метод позволяет копировать прямоугольную область пикселей из одного интерфейса **IDirect3DSurface9** в другой интерфейс **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="0aeb9-134">This method allows you to copy a rectangular region of pixels from one **IDirect3DSurface9** interface to another **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="0aeb9-135">Интерфейс Surface также имеет методы для прямого доступа к отображаемой памяти.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-135">The surface interface also has methods to directly access display memory.</span></span> <span data-ttu-id="0aeb9-136">Например, можно использовать метод [**локкрект**](/windows/desktop/api) , чтобы заблокировать прямоугольную область экрана памяти.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-136">For example, you can use the [**LockRect**](/windows/desktop/api) method to lock a rectangular region of display memory.</span></span> <span data-ttu-id="0aeb9-137">Важно вызвать [**унлоккрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) после завершения работы с заблокированной прямоугольной областью на поверхности.</span><span class="sxs-lookup"><span data-stu-id="0aeb9-137">It is important to call [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) after you are done working with the locked rectangular region on the surface.</span></span>

## <a name="additional-surface-topics"></a><span data-ttu-id="0aeb9-138">Дополнительные разделы о контактах</span><span class="sxs-lookup"><span data-stu-id="0aeb9-138">Additional Surface Topics</span></span>

<span data-ttu-id="0aeb9-139">Узнайте больше об использовании поверхностей с любым из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="0aeb9-139">Find out more about how to use surfaces with any of these topics:</span></span>

-   [<span data-ttu-id="0aeb9-140">Форматы поверхностей (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-140">Surface Formats (Direct3D 9)</span></span>](surface-formats.md)
-   [<span data-ttu-id="0aeb9-141">Что такое цепочка подкачки? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-141">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
-   [<span data-ttu-id="0aeb9-142">Ширина и шаг (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-142">Width vs. Pitch (Direct3D 9)</span></span>](width-vs--pitch.md)
-   [<span data-ttu-id="0aeb9-143">Зеркальное отображение поверхностей (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-143">Flipping Surfaces (Direct3D 9)</span></span>](flipping-surfaces.md)
-   [<span data-ttu-id="0aeb9-144">Перелистывание страниц и обратная буферизация (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-144">Page Flipping and Back Buffering (Direct3D 9)</span></span>](page-flipping-and-back-buffering.md)
-   [<span data-ttu-id="0aeb9-145">Копирование на поверхности (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-145">Copying to Surfaces (Direct3D 9)</span></span>](copying-to-surfaces.md)
-   [<span data-ttu-id="0aeb9-146">Копирование поверхностей (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-146">Copying Surfaces (Direct3D 9)</span></span>](copying-surfaces.md)
-   [<span data-ttu-id="0aeb9-147">Прямой доступ к памяти Surface (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-147">Accessing Surface Memory Directly (Direct3D 9)</span></span>](accessing-surface-memory-directly.md)
-   [<span data-ttu-id="0aeb9-148">Частные данные поверхности (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-148">Private Surface Data (Direct3D 9)</span></span>](private-surface-data.md)
-   [<span data-ttu-id="0aeb9-149">Элементы управления гамма (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aeb9-149">Gamma Controls (Direct3D 9)</span></span>](gamma-controls.md)

## <a name="related-topics"></a><span data-ttu-id="0aeb9-150">См. также</span><span class="sxs-lookup"><span data-stu-id="0aeb9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aeb9-151">Начало работы</span><span class="sxs-lookup"><span data-stu-id="0aeb9-151">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
