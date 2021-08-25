---
title: Ресурсы для мозаичного заполнения тома (графика Direct3D 11)
description: Сведения о том, как можно использовать 3D-текстуры в качестве мозаичных ресурсов. Обратите внимание, что разрешение плитки состоит из трех измерений.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618de4243598cdd9da3e80b0fe8cfad9cef65903736c4ae647f46e38d85fb77c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857654"
---
# <a name="volume-tiled-resources"></a>Объемные плиточные ресурсы

Объемные (трехмерные) текстуры можно использовать в качестве мозаичных ресурсов, отметив, что разрешение плитки состоит из трех измерений.

-   [Обзор](#overview)
-   [API-интерфейсы мозаичного ресурса D3D 11.3](#d3d113-tiled-resource-apis)
-   [Связанные темы](#related-topics)

## <a name="overview"></a>Обзор

Мозаичные ресурсы, связанные с объектом-ресурсами D3D из резервной памяти (ресурсы в прошлом имели отношение 1:1 с резервной памятью). Это позволяет использовать различные интересные сценарии, такие как потоковая передача данных текстуры и повторное использование и уменьшение использования памяти.

ресурсы мозаичного заполнения двухмерной текстуры поддерживаются в D3D 11.2. D3D12 и D3D 11.3 добавляют поддержку трехмерных мозаичных текстур.

К типичным измерениям ресурсов, используемым при мозаичном заполнении, относятся 4 x 4 плитки для двумерных текстур и 4 x 4 x 4 плитки для трехмерных текстур.



| Бит/пиксель (1 образец или пиксель)                            | Размеры мозаики (в пикселях, w x x d)                                    |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1, 4                      | 128x64x16                           |
| BC 2, 3, 5, 6, 7                | 64x64x16                            |



 

Обратите внимание, что следующие форматы не поддерживаются для мозаичных ресурсов: форматы 96bpp, форматы видео, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 \_ UNORM.

На диаграммах ниже темно-серый цвет представляет НУЛЕВые плитки.

-   [Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (наиболее подробное MIP)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (второй самый подробный MIP)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [Трехмерный мозаичный ресурс текстуры (наиболее подробный MIP)](#texture-3d-tiled-resource-most-detailed-mip)
-   [Трехмерный мозаичный ресурс текстуры (второй самый подробный MIP)](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [Трехмерный мозаичный ресурс текстуры (один элемент мозаики)](#texture-3d-tiled-resource-single-tile)
-   [Трехмерный мозаичный ресурс текстуры (унифицированное поле)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (наиболее подробное MIP)

![сопоставление по умолчанию для наиболее подробных MIP](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (второй самый подробный MIP)

![сопоставление по умолчанию для второго наиболее подробного MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Трехмерный мозаичный ресурс текстуры (наиболее подробный MIP)

Следующий код настраивает трехмерный ресурс мозаичного заполнения в наиболее подробной MIP.

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![наиболее подробное сопоставление трехмерного мозаичного ресурса](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Трехмерный мозаичный ресурс текстуры (второй самый подробный MIP)

Следующий код настраивает ресурс трехмерной мозаики, а второй самый подробный MIP:

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![второе наиболее подробное сопоставление трехмерного мозаичного ресурса](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>Трехмерный мозаичный ресурс текстуры (один элемент мозаики)

Следующий код настраивает один ресурс плитки:

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![одна плитка](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>Трехмерный мозаичный ресурс текстуры (унифицированное поле)

Следующий код устанавливает унифицированный мозаичный ресурс Box (Обратите внимание на инструкцию `trSize.bUseBox = true;) :`

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![Унифицированное поле](images/vtr-tex3d-uniform.png)

## <a name="d3d113-tiled-resource-apis"></a>API-интерфейсы мозаичного ресурса D3D 11.3

Для двумерных и трехмерных мозаичных ресурсов используются те же вызовы API:

Перечисления

-   [**D3D11 \_ Уровень МОЗАИЧных \_ ресурсов \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : определяет уровень поддержки мозаичных ресурсов.
-   [**D3D11 \_ FORMAT \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : используется для проверки поддержки мозаичных ресурсов.
-   [**D3D11 \_ Флажок "проверить \_ МНОГОвыборочные \_ \_ уровни \_ качества**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) ": определяет поддержку мозаичных ресурсов в многовыборочном ресурсе.
-   [**D3D11 \_ \_ \_ Флаги копирования плитки**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : содержит флаги для копирования в и из свиззлед мозаичных ресурсов и линейных буферов.

Структуры

-   [**D3D11 \_ \_ \_ КООРДИНАТа мозаичного ресурса**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : содержит координаты x, y и z, а также ссылки на подресурсы. Обратите внимание, что существует вспомогательный класс: CD3D11 \_ мозаичная \_ \_ координата ресурса.
-   [**D3D11 \_ \_ \_ Размер области плитки**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : определяет размер и число плиток мозаичного региона.
-   [**D3D11 \_ МОЗАИЧная \_ фигура**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : Мозаичная фигура в виде ширины, высоты и глубины в пикселей текстуры.
-   [**D3D11 \_ FEATURE \_ Data \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): содержит поддерживаемый уровень уровня ресурсов плитки.

Методы

-   [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : используется для определения того, какие функции и на каком уровне поддерживаются текущим оборудованием.
-   [**ID3D11DeviceContext2:: копитилес**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : копирует плитки из буфера в мозаичный ресурс или наоборот.
-   [**ID3D11DeviceContext2:: упдатетилемаппингс**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : обновляет сопоставления расположений плиток в мозаичных ресурсах с расположением в памяти в пуле плиток.
-   [**ID3D11DeviceContext2:: копитилемаппингс**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : копирует сопоставления из исходного мозаичного ресурса в целевой мозаичный ресурс.
-   [**ID3D11DeviceContext2:: жетресаурцетилинг**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : получает сведения о том, как мозаичный ресурс разбивается на плитки.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




