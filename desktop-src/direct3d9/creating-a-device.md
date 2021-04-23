---
description: Чтобы создать устройство Direct3D, сначала создайте объект Direct3D (см. Direct3DCreate9).
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: Создание устройства (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9c033ed25262f0a3bcdee9db73509ddf5cb53b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710689"
---
# <a name="creating-a-device-direct3d-9"></a><span data-ttu-id="0cdd4-103">Создание устройства (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0cdd4-103">Creating a Device (Direct3D 9)</span></span>

<span data-ttu-id="0cdd4-104">Чтобы создать устройство Direct3D, сначала создайте объект Direct3D (см. [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span><span class="sxs-lookup"><span data-stu-id="0cdd4-104">To create a Direct3D device, first create a Direct3D object (see [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span></span> <span data-ttu-id="0cdd4-105">Все устройства отрисовки, созданные объектом Direct3D, используют одни и те же физические ресурсы.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-105">All rendering devices created by a Direct3D object share the same physical resources.</span></span> <span data-ttu-id="0cdd4-106">Если вы создаете несколько устройств отрисовки из одного объекта Direct3D, это приведет к крайней мере снижения производительности, так как они используют одно и то же оборудование.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-106">If you create multiple rendering devices from a single Direct3D object, extreme performance penalties will be incurred because they share the same hardware.</span></span>

<span data-ttu-id="0cdd4-107">Сначала инициализируйте значения для структуры [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md) , которая используется для создания устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-107">First, initialize values for the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure that is used to create the Direct3D device.</span></span> <span data-ttu-id="0cdd4-108">В следующем примере кода задается оконное приложение, в котором задний буфер копируется в передний буфер во время операции вертикальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-108">The following code example specifies a windowed application where the back buffer is copied to the front buffer during a vertical sync operation only.</span></span>


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



<span data-ttu-id="0cdd4-109">Затем создайте устройство Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-109">Next, create the Direct3D device.</span></span> <span data-ttu-id="0cdd4-110">Следующий вызов [**IDirect3D9:: креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) указывает адаптер по умолчанию, устройство уровня абстрагирования оборудования (HAL) и обработку вершин программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-110">The following [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call specifies the default adapter, a hardware abstraction layer (HAL) device, and software vertex processing.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



<span data-ttu-id="0cdd4-111">Обратите внимание, что вызов для создания, освобождения или сброса устройства должен выполняться только в том же потоке, что и оконная процедура окна фокуса.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-111">Note that a call to create, release, or reset the device should happen only on the same thread as the window procedure of the focus window.</span></span>

<span data-ttu-id="0cdd4-112">После создания устройства задайте его состояние.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-112">After creating the device, set its state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cdd4-113">См. также</span><span class="sxs-lookup"><span data-stu-id="0cdd4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cdd4-114">Устройства Direct3D</span><span class="sxs-lookup"><span data-stu-id="0cdd4-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
