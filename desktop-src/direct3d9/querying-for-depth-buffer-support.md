---
description: Как и в случае с любой функцией, драйвер, используемый приложением, может не поддерживать все типы буферизации глубины.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Запросы для поддержки буфера глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805291"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a><span data-ttu-id="b8cf1-103">Запросы для поддержки буфера глубины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b8cf1-103">Querying for Depth Buffer Support (Direct3D 9)</span></span>

<span data-ttu-id="b8cf1-104">Как и в случае с любой функцией, драйвер, используемый приложением, может не поддерживать все типы буферизации глубины.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-104">As with any feature, the driver that your application uses might not support all types of depth buffering.</span></span> <span data-ttu-id="b8cf1-105">Всегда проверяйте возможности драйвера.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-105">Always check the driver's capabilities.</span></span> <span data-ttu-id="b8cf1-106">Хотя большинство драйверов поддерживает буферизацию глубины на основе z, не все они поддерживают буферизацию глубины на основе w.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-106">Although most drivers support z-based depth buffering, not all will support w-based depth buffering.</span></span> <span data-ttu-id="b8cf1-107">При попытке включить неподдерживаемую схему драйверы не завершаются ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-107">Drivers do not fail if you attempt to enable an unsupported scheme.</span></span> <span data-ttu-id="b8cf1-108">Вместо этого они переходят на другой метод буферизации глубины, или иногда отключена буферизация глубины, что может привести к отображению сцен с очень высокой глубиной сортировки.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-108">They fall back on another depth buffering method instead, or sometimes disable depth buffering altogether, which can result in scenes rendered with extreme depth-sorting artifacts.</span></span>

<span data-ttu-id="b8cf1-109">Можно проверить общую поддержку для буферов глубины, запросив Direct3D для устройства вывода, которое будет использоваться приложением перед созданием устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-109">You can check for general support for depth buffers by querying Direct3D for the display device that your application will use before you create a Direct3D device.</span></span> <span data-ttu-id="b8cf1-110">Если объект Direct3D сообщает, что он поддерживает буферизацию глубины, все аппаратные устройства, создаваемые из этого объекта Direct3D, будут поддерживать z-буферизацию.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-110">If the Direct3D object reports that it supports depth buffering, any hardware devices you create from this Direct3D object will support z-buffering.</span></span>

<span data-ttu-id="b8cf1-111">Чтобы запросить поддержку буферизации глубины, можно использовать метод [**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-111">To query for depth buffering support, you can use the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) method, as shown in the following code example.</span></span>


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



<span data-ttu-id="b8cf1-112">[**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) позволяет выбрать устройство для создания на основе возможностей этого устройства.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-112">[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="b8cf1-113">В этом случае устройства, не поддерживающие буферы с 16-разрядной глубиной, отклоняются.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-113">In this case, devices that do not support 16-bit depth buffers are rejected.</span></span>

<span data-ttu-id="b8cf1-114">Использование [**IDirect3D9:: чеккдепсстенЦилматч**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) для определения совместимости с набором элементов глубины с целью прорисовки показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-114">Using [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) to determine depth-stencil compatibility with a render target is illustrated in the following code example.</span></span>


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



<span data-ttu-id="b8cf1-115">Если известно, что драйвер поддерживает буферы глубины, можно проверить поддержку w-buffer.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-115">When you know that the driver supports depth buffers, you can verify w-buffer support.</span></span> <span data-ttu-id="b8cf1-116">Хотя буферы глубины поддерживаются всеми программами программной прорисовки, w-buffers поддерживаются только в справочных программах, которые не подходят для работы в реальных приложениях.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-116">Although depth buffers are supported for all software rasterizers, w-buffers are supported only by the reference rasterizer, which is not suited for use by real-world applications.</span></span> <span data-ttu-id="b8cf1-117">Независимо от типа устройства, используемого приложением, перед включением буферизации глубины на основе w следует проверить поддержку для w-буферов.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-117">Regardless of the type of device your application uses, verify support for w-buffers before you attempt to enable w-based depth buffering.</span></span>

1.  <span data-ttu-id="b8cf1-118">После создания устройства вызовите метод [**IDirect3DDevice9:: жетдевицекапс**](/windows/desktop/api) , передав инициализированную структуру [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="b8cf1-118">After creating your device, call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/desktop/api) method, passing an initialized [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>
2.  <span data-ttu-id="b8cf1-119">После вызова элемент Линекапс содержит сведения о поддержке этого драйвера для примитивов отрисовки.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-119">After the call, the LineCaps member contains information about the driver's support for rendering primitives.</span></span>
3.  <span data-ttu-id="b8cf1-120">Если элемент Растеркапс этой структуры содержит \_ флаг D3DPRASTERCAPS вбуффер, то драйвер поддерживает буферизацию глубины на основе w для этого типа-примитива.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-120">If the RasterCaps member of this structure contains the D3DPRASTERCAPS\_WBUFFER flag, then the driver supports w-based depth buffering for that primitive type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8cf1-121">См. также</span><span class="sxs-lookup"><span data-stu-id="b8cf1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8cf1-122">Буферы глубины</span><span class="sxs-lookup"><span data-stu-id="b8cf1-122">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
