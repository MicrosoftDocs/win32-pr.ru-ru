---
description: Direct3D предоставляет следующие функции для определения поддержки оборудования.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Определение поддержки оборудования (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710607"
---
# <a name="determining-hardware-support-direct3d-9"></a><span data-ttu-id="44357-103">Определение поддержки оборудования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="44357-103">Determining Hardware Support (Direct3D 9)</span></span>

<span data-ttu-id="44357-104">Direct3D предоставляет следующие функции для определения поддержки оборудования.</span><span class="sxs-lookup"><span data-stu-id="44357-104">Direct3D provides the following functions to determine hardware support.</span></span>

-   [<span data-ttu-id="44357-105">**IDirect3D9:: Чеккдевицеформат**</span><span class="sxs-lookup"><span data-stu-id="44357-105">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    <span data-ttu-id="44357-106">Используется для проверки того, можно ли использовать формат поверхности в качестве текстуры, можно ли использовать формат поверхности в качестве текстуры и целевого объекта прорисовки, а также можно ли использовать формат поверхности в качестве буфера шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="44357-106">Used to verify whether a surface format can be used as a texture, whether a surface format can be used as a texture and a render target, or whether a surface format can be used as a depth-stencil buffer.</span></span> <span data-ttu-id="44357-107">Кроме того, этот метод используется для проверки поддержки формата буфера глубины и поддержки формата буфера трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="44357-107">In addition, this method is used to verify depth buffer format support and depth-stencil buffer format support.</span></span>

-   [<span data-ttu-id="44357-108">**IDirect3D9:: Чеккдевицетипе**</span><span class="sxs-lookup"><span data-stu-id="44357-108">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    <span data-ttu-id="44357-109">Используется для проверки способности устройства выполнять аппаратное ускорение, способность устройства создавать цепочку буферов для представления или способность устройства к просмотру в текущем формате отображения.</span><span class="sxs-lookup"><span data-stu-id="44357-109">Used to verify a device's ability to perform hardware acceleration, a device's ability to build a swap chain for presentation, or a device's ability to render to the current display format.</span></span>

-   [<span data-ttu-id="44357-110">**IDirect3D9:: ЧеккдепсстенЦилматч**</span><span class="sxs-lookup"><span data-stu-id="44357-110">**IDirect3D9::CheckDepthStencilMatch**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    <span data-ttu-id="44357-111">Используется для проверки совместимости формата буфера трафарета глубины с форматом целевого объекта подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="44357-111">Used to verify whether a depth-stencil buffer format is compatible with a render-target format.</span></span> <span data-ttu-id="44357-112">Обратите внимание, что перед вызовом этого метода приложение должно вызывать [**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) в форматах "Глубина-трафарет" и "Визуализация-целевой объект".</span><span class="sxs-lookup"><span data-stu-id="44357-112">Note that before calling this method, the application should call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) on both the depth-stencil and render-target formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44357-113">См. также</span><span class="sxs-lookup"><span data-stu-id="44357-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44357-114">Устройства Direct3D</span><span class="sxs-lookup"><span data-stu-id="44357-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
