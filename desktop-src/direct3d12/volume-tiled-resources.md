---
title: Ресурсы для мозаичного заполнения тома (Direct3D 12)
description: Объемные (трехмерные) текстуры можно использовать в качестве мозаичных ресурсов, отметив, что разрешение плитки состоит из трех измерений.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d6e9b4d7ae9ad4b93bae5cf29749c293bf7f55ea7fa35a1e1ca71040218e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123509"
---
# <a name="volume-tiled-resources-direct3d-12"></a>Ресурсы для мозаичного заполнения тома (Direct3D 12)

Объемные (трехмерные) текстуры можно использовать в качестве мозаичных ресурсов, отметив, что разрешение плитки состоит из трех измерений.

## <a name="overview"></a>Обзор

Мозаичные ресурсы, связанные с объектом ресурсов Direct3D из резервной памяти (ресурсы в прошлом имели отношение 1:1 с резервной памятью). Это позволяет использовать различные интересные сценарии, такие как потоковая передача данных текстуры и повторное использование или уменьшение использования памяти.

в Direct3D 11,2 поддерживаются мозаичные ресурсы двухмерной текстуры. Дополнительная поддержка трехмерных мозаичных текстур доступна для Direct3D 12 и Direct3D 11,3 (см. [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

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

Обратите внимание, что следующие форматы не поддерживаются для мозаичных ресурсов: 96bpp formats, Video formats, **R1_UNORM**, **R8G8_B8G8_UNORM**, **R8R8_G8B8_UNORM**.

На приведенных ниже схемах темно-серый цвет представляет НУЛЕВые плитки.

* [Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (наиболее подробное MIP)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
* [Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (второй самый подробный MIP)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
* [Трехмерный мозаичный ресурс текстуры (наиболее подробный MIP)](#texture-3d-tiled-resource-most-detailed-mip)
* [Трехмерный мозаичный ресурс текстуры (второй самый подробный MIP)](#texture-3d-tiled-resource-second-most-detailed-mip)
* [Трехмерный мозаичный ресурс текстуры (один элемент мозаики)](#texture-3d-tiled-resource-single-tile)
* [Трехмерный мозаичный ресурс текстуры (унифицированное поле)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (наиболее подробно MIP)

![сопоставление по умолчанию для мозаичного трехмерного ресурса](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Сопоставление трехмерных ресурсов мозаичного распределения по умолчанию (второе — наиболее подробное MIP)

![показывает второе — подробное MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Трехмерный мозаичный ресурс текстуры (наиболее детальный MIP)

Следующий код настраивает трехмерный ресурс мозаичного заполнения в наиболее подробной MIP.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord{};
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize{};
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![наиболее детальные MIP для трехмерной текстуры](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Трехмерный мозаичный ресурс текстуры (второй-самый подробный MIP)

Следующий код настраивает ресурс трехмерной мозаики и второй наиболее подробный MIP.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![Второе — подробное MIP для трехмерной текстуры](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>Трехмерный мозаичный ресурс текстуры (один элемент мозаики)

Следующий код настраивает один ресурс плитки.

```cpp
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

![трехмерный ресурс с одним мозаичным заполнением](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>Трехмерный мозаичный ресурс текстуры (унифицированное поле)

Следующий код устанавливает унифицированный мозаичный ресурс Box (Обратите внимание на инструкцию `trSize.bUseBox = true;) :`

```cpp
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

Одни и те же вызовы API используются как для двумерных, так и для трехмерных мозаичных ресурсов.

Перечисления

* [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : определяет уровень поддержки мозаичных ресурсов.
* [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2) : используется для проверки поддержки мозаичных ресурсов.
* [**D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : определяет поддержку мозаичных ресурсов в многовыборочном ресурсе.
* [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : содержит флаги для копирования в и из свиззлед мозаичных ресурсов и линейных буферов.

Структуры

* [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : содержит координаты x, y и z, а также ссылки на подресурсы. Обратите внимание, что имеется вспомогательная структура: [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).
* [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) : определяет размер и число плиток мозаичного региона.
* [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) : Мозаичная фигура в виде ширины, высоты и глубины в пикселей текстуры.
* [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : содержит поддерживаемый уровень уровня ресурсов плитки и логическое значение *волуметиледресаурцессуппортед*, указывающее, поддерживаются ли ресурсы мозаичного распределения томов.

Методы

* [**ID3D12Device:: чеккфеатуресуппорт**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : используется для определения того, какие функции и на каком уровне поддерживаются текущим оборудованием.
* [**ID3D12GraphicsCommandList:: копитилес**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : копирует плитки из буфера в мозаичный ресурс или наоборот.
* [**ID3D12CommandQueue:: упдатетилемаппингс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : обновляет сопоставления расположений плиток в мозаичных ресурсах с расположениями в памяти в куче ресурсов.
* [**ID3D12CommandQueue:: копитилемаппингс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : копирует сопоставления из исходного мозаичного ресурса в целевой мозаичный ресурс.
* [**ID3D12Device:: жетресаурцетилинг**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : получает сведения о том, как мозаичный ресурс разбивается на плитки.

## <a name="related-topics"></a>Связанные темы

* [Привязка ресурсов](resource-binding.md)
