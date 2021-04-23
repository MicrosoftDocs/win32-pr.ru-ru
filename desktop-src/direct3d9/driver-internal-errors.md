---
description: В Direct3D 9 Direct3D позволяет драйверу возвращать коды ошибок, такие как E \_ OUTOFMEMORY, D3DERR \_ АУТОФВИДЕОМЕМОРИ и D3DERR унсуппортедколорарг, \_ чтобы приложение могло отвечать на них.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Внутренние ошибки драйвера (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140159"
---
# <a name="driver-internal-errors-direct3d-9"></a><span data-ttu-id="19752-103">Внутренние ошибки драйвера (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="19752-103">Driver Internal Errors (Direct3D 9)</span></span>

<span data-ttu-id="19752-104">В Direct3D 9 Direct3D позволяет драйверу возвращать коды ошибок, такие как E \_ OUTOFMEMORY, D3DERR \_ АУТОФВИДЕОМЕМОРИ и D3DERR унсуппортедколорарг, \_ чтобы приложение могло отвечать на них.</span><span class="sxs-lookup"><span data-stu-id="19752-104">In Direct3D 9, Direct3D will allow the driver to return error codes such as E\_OUTOFMEMORY, D3DERR\_OUTOFVIDEOMEMORY, and D3DERR\_UNSUPPORTEDCOLORARG so that an application would be able to respond to them.</span></span> <span data-ttu-id="19752-105">Однако иногда вызовы API, которые генерируют эти возвращаемые типы, загружаются в буфер команд и отправляются в GPU (см. раздел [Управление оптимизацией среды выполнения и драйверов](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="19752-105">However, sometimes the API calls that generated these return types get loaded into a command buffer and are batched up to be sent to the GPU (see [Controlling Runtime and Driver Optimizations](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="19752-106">В этом случае ошибки не могут быть ретранслируемы в приложение, когда необходимо выполнить действие, поэтому код ошибки используется средой выполнения, а заметка для объекта устройства, на котором это произошло.</span><span class="sxs-lookup"><span data-stu-id="19752-106">In this case, the errors cannot be relayed to the application when action needs to be taken, so the error code is consumed by the runtime and a note is made on the device object that this happened.</span></span> <span data-ttu-id="19752-107">Позже, когда приложение вызывает [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)повторной отправки, **IDirect3DDevice9::P** повторная отправка вернет D3DERR \_ дриверинтерналеррор.</span><span class="sxs-lookup"><span data-stu-id="19752-107">Later when the application invokes [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::Present** will return D3DERR\_DRIVERINTERNALERROR.</span></span> <span data-ttu-id="19752-108">Именно поэтому наилучший подход к приложению при получении D3DERR \_ дриверинтерналеррор из **IDirect3DDevice9::P** повторной отправки — удаление и повторное создание устройства.</span><span class="sxs-lookup"><span data-stu-id="19752-108">This is why the best approach for an application to take when receiving a D3DERR\_DRIVERINTERNALERROR from **IDirect3DDevice9::Present** is to destroy and recreate the device.</span></span>

<span data-ttu-id="19752-109">Если вы хотите попытаться выполнить отладку еще раз, вот несколько советов по попытке выяснить, какой вызов API создает ошибку:</span><span class="sxs-lookup"><span data-stu-id="19752-109">If you want to try to debug further, here are a couple of suggestions for trying to figure out which API call is generating the error:</span></span>

-   <span data-ttu-id="19752-110">Так как список возможных возвращаемых значений не завершен, можно попытаться определить, какой вызов завершается ошибкой, вызвав следующий вызов API:</span><span class="sxs-lookup"><span data-stu-id="19752-110">Because the list of possible return values is not complete, you can try to find which call is failing by surrounding each API call like this:</span></span>

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    <span data-ttu-id="19752-111">Выходной поток отладки должен затем отображать вызов, который вызывает проблему.</span><span class="sxs-lookup"><span data-stu-id="19752-111">The output debug stream should then show the call that is causing the problem.</span></span>

-   <span data-ttu-id="19752-112">Кроме того, в целях отладки попробуйте вызвать [**IDirect3DDevice9:: валидатедевице**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) непосредственно перед каждым [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , чтобы узнать, есть ли дополнительные проблемы с драйвером устройства (неподдерживаемая операция, неиспользуемое сочетание форматов текстур и т. д.).</span><span class="sxs-lookup"><span data-stu-id="19752-112">Additionally, for debugging purposes, try calling [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immediately before each [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) to see if there is an additional problem with the device driver (unsupported operation, unusable combination of texture formats, etc).</span></span>

    > [!Note]  
    > <span data-ttu-id="19752-113">[**IDirect3DDevice9:: валидатедевице**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) следует использовать осторожно и экономно из-за объема проверки, которую должен выполнить драйвер для возврата ответа.</span><span class="sxs-lookup"><span data-stu-id="19752-113">[**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) should be used carefully and sparingly because of the amount of validation work the driver needs to perform to return an answer.</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="19752-114">См. также</span><span class="sxs-lookup"><span data-stu-id="19752-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19752-115">Советы по программированию</span><span class="sxs-lookup"><span data-stu-id="19752-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
