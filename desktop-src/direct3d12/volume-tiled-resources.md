---
title: Ресурсы для мозаичного заполнения тома (Direct3D 12)
description: Объемные (трехмерные) текстуры можно использовать в качестве мозаичных ресурсов, отметив, что разрешение плитки состоит из трех измерений.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42679155bbd8dc2cec560d2724e430c860f54bc0
ms.sourcegitcommit: 05e7efd3d8de6926d08802669f37e825a2fa2f46
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/12/2020
ms.locfileid: "104548936"
---
# <a name="volume-tiled-resources-direct3d-12"></a>Ресурсы для мозаичного заполнения тома (Direct3D 12)

Объемные (трехмерные) текстуры можно использовать в качестве мозаичных ресурсов, отметив, что разрешение плитки состоит из трех измерений.

-   [Обзор](#overview)
-   [API-интерфейсы мозаичного ресурса](#tiled-resource-apis)
-   [Связанные темы](#related-topics)

## <a name="overview"></a>Обзор

Мозаичные ресурсы, связанные с объектом-ресурсами D3D из резервной памяти (ресурсы в прошлом имели отношение 1:1 с резервной памятью). Это позволяет использовать различные интересные сценарии, такие как потоковая передача данных текстуры и повторное использование или уменьшение использования памяти.

ресурсы мозаичного заполнения двухмерной текстуры поддерживаются в D3D 11.2. Необязательная поддержка трехмерных мозаичных текстур доступна для D3D12 и D3D 11.3 (см. [**\_ \_ \_ уровень мозаичных ресурсов D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

К типичным измерениям ресурсов, используемым при мозаичном заполнении, относятся 4 x 4 плитки для двумерных текстур и 4 x 4 x 4 плитки для трехмерных текстур.



| Бит/пиксель (1 образец или пиксель) | Размеры мозаики (в пикселях, w x x d) |
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

![сопоставление по умолчанию для мозаичного трехмерного ресурса](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (второй самый подробный MIP)

![показывает второй наиболее подробный MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Трехмерный мозаичный ресурс текстуры (наиболее подробный MIP)

Следующий код настраивает трехмерный ресурс мозаичного заполнения в наиболее подробной MIP.

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![наиболее подробный MIP для трехмерной текстуры](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Трехмерный мозаичный ресурс текстуры (второй самый подробный MIP)

Следующий код настраивает ресурс трехмерной мозаики, а второй самый подробный MIP:

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![второй наиболее подробный MIP для трехмерной текстуры](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>Трехмерный мозаичный ресурс текстуры (один элемент мозаики)

Следующий код настраивает один ресурс плитки:

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![один мозаичный трехмерный ресурс](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>Трехмерный мозаичный ресурс текстуры (унифицированное поле)

Следующий код устанавливает унифицированный мозаичный ресурс Box (Обратите внимание на инструкцию `trSize.bUseBox = true;) :`

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![Унифицированное поле](images/vtr-tex3d-uniform.png)

## <a name="tiled-resource-apis"></a>API-интерфейсы мозаичного ресурса

Для двумерных и трехмерных мозаичных ресурсов используются те же вызовы API:

Перечисления

-   [**D3D12 \_ Уровень МОЗАИЧных \_ ресурсов \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : определяет уровень поддержки мозаичных ресурсов.
-   [**D3D12 \_ FORMAT \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : используется для проверки поддержки мозаичных ресурсов.
-   [**D3D12 \_ \_ \_ \_ Флаги уровня качества**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) для нескольких образцов: определяет поддержку мозаичных ресурсов в многовыборочном ресурсе.
-   [**D3D12 \_ \_ \_ Флаги копирования плитки**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : содержит флаги для копирования в и из свиззлед мозаичных ресурсов и линейных буферов.

Структуры

-   [**D3D12 \_ \_ \_ КООРДИНАТа мозаичного ресурса**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : содержит координаты x, y и z, а также ссылки на подресурсы. Обратите внимание, что существует вспомогательная структура: [**CD3DX12 \_ Мозаичное \_ \_ координата ресурса**](cd3dx12-tiled-resource-coordinate.md).
-   [**D3D12 \_ \_ \_ Размер области плитки**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : определяет размер и число плиток мозаичного региона.
-   [**D3D12 \_ МОЗАИЧная \_ фигура**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : Мозаичная фигура в виде ширины, высоты и глубины в пикселей текстуры.
-   [**D3D12 \_ \_ \_ \_ Параметры D3D12 данных функции**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : содержит поддерживаемый уровень уровня ресурсов плитки и логическое значение, *волуметиледресаурцессуппортед*, указывающее, поддерживаются ли ресурсы мозаичного распределения томов.

Методы

-   [**ID3D12Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : используется для определения того, какие функции и на каком уровне поддерживаются текущим оборудованием.
-   [**ID3D12GraphcisCommandList:: копитилес**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : копирует плитки из буфера в мозаичный ресурс или наоборот.
-   [**ID3D12CommandQueue:: упдатетилемаппингс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : обновляет сопоставления расположений плиток в мозаичных ресурсах с расположениями в памяти в куче ресурсов.
-   [**ID3D12CommandQueue:: копитилемаппингс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : копирует сопоставления из исходного мозаичного ресурса в целевой мозаичный ресурс.
-   [**ID3D12Device:: жетресаурцетилинг**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : получает сведения о том, как мозаичный ресурс разбивается на плитки.

## <a name="related-topics"></a>Связанные темы
* [Привязка ресурсов](resource-binding.md)
