---
title: Создание цепочки буферов
description: В этом разделе показано, как создать цепочку подкачки, которая инкапсулирует два или больше буферов, используемых для отрисовки и отображения.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8355eafff6e233b89be82fd9e58ca53224248e84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413295"
---
# <a name="how-to-create-a-swap-chain"></a><span data-ttu-id="ecffd-103">Как создать цепочку буферов</span><span class="sxs-lookup"><span data-stu-id="ecffd-103">How To: Create a Swap Chain</span></span>

<span data-ttu-id="ecffd-104">В этом разделе показано, как создать цепочку подкачки, которая инкапсулирует два или больше буферов, используемых для отрисовки и отображения.</span><span class="sxs-lookup"><span data-stu-id="ecffd-104">This topic show how to create a swap chain that encapsulates two or more buffers that are used for rendering and display.</span></span> <span data-ttu-id="ecffd-105">Обычно они содержат интерфейсный буфер, представленный для устройства отображения, и задний буфер, который выступает в качестве целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ecffd-105">They usually contain a front buffer that is presented to the display device and a back buffer that serves as the render target.</span></span> <span data-ttu-id="ecffd-106">После того как непосредственный контекст будет готов к просмотру в обратном буфере, цепочка буфера обмена представляет задний буфер путем переключения двух буферов.</span><span class="sxs-lookup"><span data-stu-id="ecffd-106">After the immediate context is done rendering to the back buffer, the swap chain presents the back buffer by swapping the two buffers.</span></span>

<span data-ttu-id="ecffd-107">Цепочка буфера обмена определяет несколько характеристик отрисовки, включая:</span><span class="sxs-lookup"><span data-stu-id="ecffd-107">The swap chain defines several rendering characteristics including:</span></span>

-   <span data-ttu-id="ecffd-108">Размер области рендеринга.</span><span class="sxs-lookup"><span data-stu-id="ecffd-108">The size of the render area.</span></span>
-   <span data-ttu-id="ecffd-109">Частота обновления дисплея.</span><span class="sxs-lookup"><span data-stu-id="ecffd-109">The display refresh rate.</span></span>
-   <span data-ttu-id="ecffd-110">Режим отображения.</span><span class="sxs-lookup"><span data-stu-id="ecffd-110">The display mode.</span></span>
-   <span data-ttu-id="ecffd-111">Формат поверхности.</span><span class="sxs-lookup"><span data-stu-id="ecffd-111">The surface format.</span></span>

<span data-ttu-id="ecffd-112">Определите характеристики цепочки буферов, заполнив структуру для [**\_ \_ цепочки буфера \_ обмена**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) и инициализируя интерфейс [**идксгисвапчаин**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) .</span><span class="sxs-lookup"><span data-stu-id="ecffd-112">Define the characteristics of the swap chain by filling in a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure and initializing an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) interface.</span></span> <span data-ttu-id="ecffd-113">Инициализируйте цепочку подкачки путем вызова [**идксгифактори:: креатесвапчаин**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) или [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="ecffd-113">Initialize a swap chain by calling [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="create-a-device-and-a-swap-chain"></a><span data-ttu-id="ecffd-114">Создание устройства и цепочки буферов</span><span class="sxs-lookup"><span data-stu-id="ecffd-114">Create a device and a swap chain</span></span>

<span data-ttu-id="ecffd-115">Чтобы инициализировать устройство и цепочку буферов, используйте одну из следующих двух функций:</span><span class="sxs-lookup"><span data-stu-id="ecffd-115">To initialize a device and swap chain, use one of the following two functions:</span></span>

-   <span data-ttu-id="ecffd-116">Используйте функцию [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) , если вы хотите инициализировать цепочку буферов одновременно с инициализацией устройства.</span><span class="sxs-lookup"><span data-stu-id="ecffd-116">Use the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function when you want to initialize the swap chain at the same time as device initialization.</span></span> <span data-ttu-id="ecffd-117">Обычно это самый простой вариант.</span><span class="sxs-lookup"><span data-stu-id="ecffd-117">This usually is the easiest option.</span></span>

-   <span data-ttu-id="ecffd-118">Используйте функцию [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) , если цепь подкачки уже создана с помощью [**Идксгифактори:: креатесвапчаин**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span><span class="sxs-lookup"><span data-stu-id="ecffd-118">Use the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function when you have already created a swap chain using [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ecffd-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ecffd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecffd-120">Устройства</span><span class="sxs-lookup"><span data-stu-id="ecffd-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="ecffd-121">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ecffd-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 