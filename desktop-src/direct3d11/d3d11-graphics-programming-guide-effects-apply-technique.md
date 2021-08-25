---
title: Применение методики (Direct3D 11)
description: Узнайте, как задать состояние воздействия на устройстве для Direct3D 11 после объявления и инициализации констант, текстур и состояния шейдера.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b53eb5f60c80baf69199885f8036a9e92ac1572fe8339bd6d4a96454adb0121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792044"
---
# <a name="apply-a-technique-direct3d-11"></a>Применение методики (Direct3D 11)

Когда константы, текстуры и состояние шейдера объявлены и инициализированы, осталось только установить состояние воздействия на устройстве.

## <a name="set-non-shader-state-in-the-device"></a>Задание состояния, отличного от шейдера, на устройстве

Некоторые состояния конвейера не задаются каким-либо действием. Например, очистка целевого объекта рендеринга готовит целевой объект отрисовки для данных. Ниже приведен пример очистки выходных буферов перед установкой состояния воздействия на устройство.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Установка состояния воздействия на устройстве

Установка состояния действия выполняется путем применения состояния действия в цикле подготовки к просмотру. Это делается из внешней среды в. То есть выберите метод, а затем задайте состояние для каждого из проходов (в зависимости от желаемого результата).


```
    D3D11_TECHNIQUE_DESC techDesc;
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

[Отрисовка результата (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




