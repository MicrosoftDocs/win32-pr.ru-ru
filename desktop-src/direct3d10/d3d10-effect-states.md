---
description: Состояния эффектов — это пары "имя-значение" в виде выражения.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Группы состояний эффектов (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351742"
---
# <a name="effect-state-groups-direct3d-10"></a>Группы состояний эффектов (Direct3D 10)

Состояния эффектов — это пары "имя-значение" в виде выражения.

## <a name="blend-state"></a>Состояние смешения

| | |
|-|-|
| **алфатоковеражеенабле**, **бленденабле**, **сркбленд**, **дестбленд**, **блендоп**, **сркблендалфа**, **дестблендалфа**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK** | Члены [ **D3D10 \_ Blend \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) |

## <a name="depth-and-stencil-state"></a>Состояние глубины и трафарета

| | |
|-|-|
| **депсенабле**, **депсвритемаск**, **депсфунк**, **стенЦиленабле**, **стенЦилреадмаск**, **стенЦилвритемаск** | Элементы в [ **\_ \_ наборе элементов \_ глубины D3D10 DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |
| ФРОНТФАЦЕСТЕНЦИЛФАИЛ * *, **фронтфацестенЦилзфаил**, **фронтфацестенЦилпасс**, **фронтфацестенЦилфунк**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC** | Член [ **D3D10 \_ глубины \_ стенЦилоп \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc) |

## <a name="rasterizer-state"></a>Состояние средства программной прорисовки

| | |
|-|-|
| филлмоде | [**\_Режим заполнения \_ D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| куллмоде | [**Режим D3D10ного \_ отбора \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| **фронткаунтерклокквисе**, **депсбиас**, **депсбиаскламп**, **слопескаледдепсбиас**, **зклипенабле**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE** | Члены класса [ **D3D10 средство \_ растеризации \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc) |

## <a name="sampler-state"></a>Состояние дискретизатора

| | |
|-|-|
| **Filter**, **аддрессу**, **аддрессв**, **аддрессв**, **миплодбиас**, **максанисотропи**, **компарисонфунк**, **BorderColor**, **минлод**, **макслод** | Члены [ **D3D10ного \_ образца \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) |

Примеры см. в разделе [тип образца (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) .

## <a name="effect-object-state"></a>Состояние объекта Effect

| Этот объект Effect | Соответствует параметру |
|-|-|
| растеризерстате | Объект состояния состояния средства программной [прорисовки](#rasterizer-state) . |
| депсстенЦилстате | Объект состояния " [глубина" и "набор элементов](#depth-and-stencil-state) ". |
| блендстате | Объект состояния [смешения состояния](#blend-state) . |
| вертексшадер | Скомпилированный объект шейдера вершин. |
| PIXELSHADER | Скомпилированный объект шейдера пикселей. |
| жеометришадер | Скомпилированный объект шейдера Geometry. |
| DS \_ СТЕНЦИЛРЕФ AB \_ блендфактор AB \_ самплемаск | Члены [**D3D10 \_ Pass \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc). |

## <a name="defining-and-using-state-objects"></a>Определение и использование объектов состояния

Объекты состояния объявляются в файлах FX в следующем формате. *Статеобжекттипе* — одно из состояний, перечисленных выше, а *MemberName* — имя любого члена, который будет иметь значение, отличное от значения по умолчанию.

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

Например, чтобы настроить объект состояния Blend с Алфатоковеражеенабле, а Бленденабле \[ 0 \] — значением **false**, используется следующий код.

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

Объект состояния применяется к методу Pass с помощью одной из функций Сетстатеграуп, описанных в разделе [синтаксис методики работы (Direct3D 10)](d3d10-effect-technique-syntax.md). Например, для применения объекта Блендстате, описанного выше, будет использоваться следующий код.

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

Учебник, в котором описывается использование состояний, см. в разделе [Управление состоянием](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="related-topics"></a>См. также

* [Синтаксис методики эффектов](d3d10-effect-technique-syntax.md)
* [Формат эффектов (Direct3D 10)](d3d10-effect-format.md)
