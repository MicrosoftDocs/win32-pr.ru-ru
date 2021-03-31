---
description: Использование сопоставления выпуклости (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Использование сопоставления выпуклости (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4bc96f78ffb19dda04ff6b2bc3d0e46800b04b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495759"
---
# <a name="using-bump-mapping-direct3d-9"></a>Использование сопоставления выпуклости (Direct3D 9)

## <a name="detecting-support-for-bump-mapping"></a>Обнаружение поддержки для отображения рельефов

Устройство может выполнять сопоставление выпуклости, если оно поддерживает \_ \_ операцию смешения текстур D3DTOP БУМПЕНВМАП или D3DTOP бумпенвмаплуминанце. Используйте [**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) с D3DUSAGE \_ Query \_ легацибумпмап, чтобы узнать, поддерживается ли формат для сопоставления выпуклости.

Кроме того, приложения должны проверить возможности устройства, чтобы убедиться, что устройство поддерживает соответствующее количество стадий смешения, обычно по крайней мере три, и предоставляет по крайней мере один формат пикселей сопоставления выпуклости.

В следующем примере кода выполняется проверка возможностей устройства, чтобы обнаружить поддержку для сопоставления выпуклости на текущем устройстве, используя заданные критерии.


```
BOOL SupportsBumpMapping()
{
    D3DCAPS9 d3dCaps;

    d3dDevice->GetDeviceCaps( &d3dCaps );

    // Does this device support the two bump mapping blend operations?
    if ( 0 == d3dCaps.TextureOpCaps & ( D3DTEXOPCAPS_BUMPENVMAP |
                                            D3DTEXOPCAPS_BUMPENVMAPLUMINANCE ))
        return FALSE;

    // Does this device support up to three blending stages?
    if( d3dCaps.MaxTextureBlendStages < 3 )
        return FALSE;

    return TRUE;
}
```



## <a name="creating-a-bump-map-texture"></a>Создание текстуры с картой выпуклости

Вы создаете текстуру карт выпуклости, аналогичную любой другой текстуре. Приложение проверяет поддержку сопоставления выпуклости и извлекает допустимый формат пикселей, как описано в разделе Обнаружение поддержки для отображения выпуклости.

После создания поверхности можно загрузить каждый пиксель с соответствующими разностными значениями и светимостью, если формат поверхности включает светимость. Значения для каждого компонента пикселей описаны в разделе [форматы точек выпуклости (Direct3D 9)](bump-map-pixel-formats.md).

## <a name="configuring-bump-mapping-parameters"></a>Настройка параметров сопоставления выпуклости

Когда приложение создает карту выпуклости и устанавливает содержимое каждого пикселя, можно подготовиться к подготовке к просмотру, настроив параметры сопоставления выпуклости. Параметры сопоставления выпуклости включают настройку требуемых текстур и их операции смешения, а также элементы управления преобразованием и яркостью для самой карты выпуклости.

1.  Установите базовую карту текстуры, если она используется, а также карту выпуклости и карту окружения в этапы смешения текстур.
2.  Установите операции смешения цвета и альфа-канала для каждой стадии текстуры.
3.  Задайте матрицу преобразования карт выпуклости.
4.  При необходимости задайте значения параметров "масштаб светимости" и "смещение".

В следующем примере кода задаются три текстуры (базовая текстура, схема выпуклости и гиперкарта) для соответствующих этапов смешения текстур.


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



После установки текстур на стадии смешения в следующем примере кода подготавливаются операции смешения и аргументы для каждого этапа.


```
// Set the color operations and arguments to prepare for
//   bump mapping.

// Stage 0: The base texture
d3dDevice->SetTextureStageState( 0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAOP, D3DTOP_SELECTARG1 );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE ); 
d3dDevice->SetTextureStageState( 0, D3DTSS_TEXCOORDINDEX, 1 );

// Stage 1: The bump map - Use luminance for this example.
d3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_BUMPENVMAPLUMINANCE);
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Stage 2: A specular environment map
d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX, 0 );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



Если заданы операции смешения и аргументы, то в следующем примере кода матрица сопоставления «выпуклость 2x2» устанавливается в матрицу идентификаторов, задавая \_ элементы D3DTSS BUMPENVMAPMAT00 и D3DTSS \_ BUMPENVMAPMAT11 [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) в 1,0. Настройка матрицы для идентификации приводит к тому, что система использует разностные значения в карте выпуклости без изменений, но это не является обязательным.


```
// Set the bump mapping matrix.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT00, F2DW(1.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT01, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT10, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT11, F2DW(1.0f) );
```



Если для операции отображения рельефа задана светимость (D3DTOP \_ бумпенвмаплуминанце), необходимо задать элементы управления яркостью. Элементы управления яркостью настраивают, как система рассчитывает светимость, прежде чем модулатинг цвет из текстуры на следующем этапе. Дополнительные сведения см. в разделе [формулы сопоставления выпуклости (Direct3D 9)](bump-mapping-formulas.md).


```
// Set luminance controls. This is only needed when using
// a bump map that contains luminance, and when the 
// D3DTOP_BUMPENVMAPLUMINANCE texture blending operation is
// being used.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLSCALE, F2DW(0.5f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLOFFSET, F2DW(0.0f) );
```



После того как приложение настроит параметры сопоставления выпуклости, оно может быть отображено как нормальное, а отображаемые многоугольники получают эффекты отображения выпуклости.

Обратите внимание, что в предыдущем примере показаны параметры, настроенные для сопоставления с зеркальной средой. При выполнении рассеянного освещения приложения устанавливают операцию смешения текстуры для последнего этапа, чтобы D3DTOPая \_ модуляция. Дополнительные сведения см. в разделе [диффузная легкая карта (Direct3D 9)](diffuse-light-maps.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сопоставление рельефов](bump-mapping.md)
</dt> </dl>

 

 
