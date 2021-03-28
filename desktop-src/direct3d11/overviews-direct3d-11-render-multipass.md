---
title: Подготовка к просмотру Multiple-Pass
description: Многопроходная визуализация — это процесс, в ходе которого приложение несколько раз проходит по графу сцены, чтобы получить выходные данные для отображения на экране.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fcf7f3f04bd641fdf82c9cf317e8a2ec99e85c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330803"
---
# <a name="multiple-pass-rendering"></a><span data-ttu-id="b5fb9-103">Подготовка к просмотру Multiple-Pass</span><span class="sxs-lookup"><span data-stu-id="b5fb9-103">Multiple-Pass Rendering</span></span>

<span data-ttu-id="b5fb9-104">Многопроходная визуализация — это процесс, в ходе которого приложение несколько раз проходит по графу сцены, чтобы получить выходные данные для отображения на экране.</span><span class="sxs-lookup"><span data-stu-id="b5fb9-104">Multiple-pass rendering is a process in which an application traverses its scene graph multiple times in order to produce an output to render to the display.</span></span> <span data-ttu-id="b5fb9-105">Многопроходная визуализация повышает производительность, поскольку она разбивает сложные сцены на задачи, которые могут выполняться параллельно.</span><span class="sxs-lookup"><span data-stu-id="b5fb9-105">Multiple-pass rendering improves performance because it breaks up complex scenes into tasks that can run concurrently.</span></span>

<span data-ttu-id="b5fb9-106">Чтобы выполнить многопроходную отрисовку, создайте отложенный контекст и список команд для каждого дополнительного прохода.</span><span class="sxs-lookup"><span data-stu-id="b5fb9-106">To perform multiple-pass rendering, you create a deferred context and command list for each additional pass.</span></span> <span data-ttu-id="b5fb9-107">Пока приложение проходит по графику сцены, он записывает команды (например [**, отрисовки) в**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)отложенный контекст.</span><span class="sxs-lookup"><span data-stu-id="b5fb9-107">While the application traverses the scene graph, it records commands (for example, rendering commands such as [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) into a deferred context.</span></span> <span data-ttu-id="b5fb9-108">После завершения обхода приложения он вызывает метод [**финишкоммандлист**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) для отложенного контекста.</span><span class="sxs-lookup"><span data-stu-id="b5fb9-108">After the application finishes the traversal, it calls the [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) method on the deferred context.</span></span> <span data-ttu-id="b5fb9-109">Наконец, приложение вызывает метод [**вызова элемента executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) в непосредственных контекстах для выполнения команд в каждом списке команд.</span><span class="sxs-lookup"><span data-stu-id="b5fb9-109">Finally, the application calls the [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) method on the immediate context to execute the commands in each command list.</span></span>

<span data-ttu-id="b5fb9-110">В следующем псевдокоде показано, как выполнить многопроходную отрисовку:</span><span class="sxs-lookup"><span data-stu-id="b5fb9-110">The following pseudocode shows how to perform multiple-pass rendering:</span></span>

``` syntax
{
 ImmCtx->SetRenderTarget( pRTViewOfResourceX );
 DefCtx1->SetTexture( pSRView1OfResourceX );
 DefCtx2->SetTexture( pSRView2OfResourceX );

 for () // Traverse the scene graph.
  {
    ImmCtx->Draw(); // Pass 0: immediate context renders primitives into resource X.

    // The following texturing by the deferred contexts occurs after the 
    // immediate context makes calls to ExecuteCommandList. 
    // Resource X is then comletely updated by the immediate context. 
    DefCtx1->Draw(); // Pass 1: deferred context 1 performs texturing from resource X.
    DefCtx2->Draw(); // Pass 2: deferred context 2 performs texturing from resource X.
      }

  // Create command lists and record commands into them.
  DefCtx1->FinishCommandList( &pCL1 ); 
  DefCtx2->FinishCommandList( &pCL2 );

  ImmCtx->ExecuteCommandList( pCL1 ); // Execute pass 1.
  ImmCtx->ExecuteCommandList( pCL2 ); // Exeucte pass 2.
}
```

> [!Note]  
> <span data-ttu-id="b5fb9-111">Непосредственный контекст изменяет ресурс, который привязан к немедленному контексту как представление целевого объекта отрисовки (РТВ); напротив, каждый отложенный контекст просто использует ресурс, который привязан к отложенному контексту в виде представления ресурсов шейдера (SRV).</span><span class="sxs-lookup"><span data-stu-id="b5fb9-111">The immediate context modifies a resource, which is bound to the immediate context as a render target view (RTV); in contrast, each deferred context simply uses the resource, which is bound to the deferred context as a shader resource view (SRV).</span></span> <span data-ttu-id="b5fb9-112">Дополнительные сведения о немедленном и отложенном контекстах см. в разделе [Интерпретация и отложенная визуализация](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="b5fb9-112">For more information about immediate and deferred contexts, see [Immediate and Deferred Rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b5fb9-113">См. также</span><span class="sxs-lookup"><span data-stu-id="b5fb9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5fb9-114">Отрисовка</span><span class="sxs-lookup"><span data-stu-id="b5fb9-114">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




