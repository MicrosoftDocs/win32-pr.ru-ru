---
title: Подготовка к просмотру Multiple-Pass
description: Многопроходная визуализация — это процесс, в ходе которого приложение несколько раз проходит по графу сцены, чтобы получить выходные данные для отображения на экране.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242573dea2982f3525082187aad536a407e446c4ce59f116f53b8fa0d40fc582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124212"
---
# <a name="multiple-pass-rendering"></a>Подготовка к просмотру Multiple-Pass

Многопроходная визуализация — это процесс, в ходе которого приложение несколько раз проходит по графу сцены, чтобы получить выходные данные для отображения на экране. Многопроходная визуализация повышает производительность, поскольку она разбивает сложные сцены на задачи, которые могут выполняться параллельно.

Чтобы выполнить многопроходную отрисовку, создайте отложенный контекст и список команд для каждого дополнительного прохода. Пока приложение проходит по графику сцены, он записывает команды (например [**, отрисовки) в**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)отложенный контекст. После завершения обхода приложения он вызывает метод [**финишкоммандлист**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) для отложенного контекста. Наконец, приложение вызывает метод [**вызова элемента executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) в непосредственных контекстах для выполнения команд в каждом списке команд.

В следующем псевдокоде показано, как выполнить многопроходную отрисовку:

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
> Непосредственный контекст изменяет ресурс, который привязан к немедленному контексту как представление целевого объекта отрисовки (РТВ); напротив, каждый отложенный контекст просто использует ресурс, который привязан к отложенному контексту в виде представления ресурсов шейдера (SRV). Дополнительные сведения о немедленном и отложенном контекстах см. в разделе [Интерпретация и отложенная визуализация](overviews-direct3d-11-render-multi-thread-render.md).

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Отрисовка](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




