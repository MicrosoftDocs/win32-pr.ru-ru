---
description: Когда константы, текстуры и состояние шейдера объявлены и инициализированы, осталось только установить состояние воздействия на устройстве.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Применение методики (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4c920cbc7323ba42f3b099688a962674e3f5c2305746df7a56d1e158330919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128416"
---
# <a name="apply-a-technique-direct3d-10"></a>Применение методики (Direct3D 10)

Когда константы, текстуры и состояние шейдера объявлены и инициализированы, осталось только установить состояние воздействия на устройстве.

## <a name="set-non-shader-state-in-the-device"></a>Задание состояния, отличного от шейдера, на устройстве

Некоторые состояния конвейера не задаются каким-либо действием. Например, очистка целевого объекта рендеринга готовит целевой объект отрисовки для данных. Ниже приведен пример очистки выходных буферов перед установкой состояния воздействия на устройство.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Установка состояния воздействия на устройстве

Установка состояния действия выполняется путем применения состояния действия в цикле подготовки к просмотру. Это делается из внешней среды в. То есть выберите метод, а затем задайте состояние для каждого из проходов (в зависимости от желаемого результата).


```
    D3D10_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



Результат не отображает ничего, он просто устанавливает состояние воздействия на устройство. Код отрисовки вызывается после того, как состояние действия изменит состояние устройства. В этом примере вызов Дравиндексед выполняет отрисовку.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Отрисовка влияния (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



