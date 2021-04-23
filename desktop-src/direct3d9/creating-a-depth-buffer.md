---
description: Буфер глубины — это свойство устройства. Чтобы создать буфер глубины, который управляется Direct3D, задайте соответствующие члены \_ структуры параметров D3DPRESENT, как показано в следующем примере кода.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Создание буфера глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141091"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a><span data-ttu-id="b3442-104">Создание буфера глубины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b3442-104">Creating a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="b3442-105">Буфер глубины — это свойство устройства.</span><span class="sxs-lookup"><span data-stu-id="b3442-105">A depth buffer is a property of the device.</span></span> <span data-ttu-id="b3442-106">Чтобы создать буфер глубины, который управляется Direct3D, задайте соответствующие члены структуры [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md) , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="b3442-106">To create a depth buffer that is managed by Direct3D, set the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure as shown in the following code example.</span></span>


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



<span data-ttu-id="b3442-107">Установив для элемента ЕнаблеаутодепсстенЦил **значение true**, вы указываете Direct3D управлять буферами глубины для приложения.</span><span class="sxs-lookup"><span data-stu-id="b3442-107">By setting the EnableAutoDepthStencil member to **TRUE**, you instruct Direct3D to manage depth buffers for the application.</span></span> <span data-ttu-id="b3442-108">Обратите внимание, что для АутодепсстенЦилформат должен быть задан допустимый формат буфера глубины.</span><span class="sxs-lookup"><span data-stu-id="b3442-108">Note that AutoDepthStencilFormat must be set to a valid depth buffer format.</span></span> <span data-ttu-id="b3442-109">Флаг D3DFMT \_ D16 задает 16-разрядный буфер глубины, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="b3442-109">The D3DFMT\_D16 flag specifies a 16-bit depth buffer, if one is available.</span></span>

<span data-ttu-id="b3442-110">Следующий вызов метода [**IDirect3D9:: креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) создает устройство, которое затем создает буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="b3442-110">The following call to the [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) method creates a device that then creates a depth buffer.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



<span data-ttu-id="b3442-111">Буфер глубины автоматически устанавливается в качестве целевого объекта рендеринга для устройства.</span><span class="sxs-lookup"><span data-stu-id="b3442-111">The depth buffer is automatically set as the render target of the device.</span></span> <span data-ttu-id="b3442-112">При сбросе устройства буфер глубины автоматически уничтожается и создается заново в новом размере.</span><span class="sxs-lookup"><span data-stu-id="b3442-112">When the device is reset, the depth buffer is automatically destroyed and re-created in the new size.</span></span>

<span data-ttu-id="b3442-113">Чтобы создать новую поверхность буфера глубины, используйте метод [**IDirect3DDevice9:: креатедепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .</span><span class="sxs-lookup"><span data-stu-id="b3442-113">To create a new depth buffer surface, use the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) method.</span></span>

<span data-ttu-id="b3442-114">Чтобы задать новую поверхность буфера глубины для устройства, используйте метод [**IDirect3DDevice9:: сетдепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) .</span><span class="sxs-lookup"><span data-stu-id="b3442-114">To set a new depth-buffer surface for the device, use the [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) method.</span></span>

<span data-ttu-id="b3442-115">Чтобы использовать в приложении буфер глубины, необходимо включить буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="b3442-115">To use the depth buffer in your application, you need to enable the depth buffer.</span></span> <span data-ttu-id="b3442-116">Дополнительные сведения см. в разделе [Включение буферизации глубины (Direct3D 9)](enabling-depth-buffering.md).</span><span class="sxs-lookup"><span data-stu-id="b3442-116">For details, see [Enabling Depth Buffering (Direct3D 9)](enabling-depth-buffering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3442-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b3442-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3442-118">Буферы глубины</span><span class="sxs-lookup"><span data-stu-id="b3442-118">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
