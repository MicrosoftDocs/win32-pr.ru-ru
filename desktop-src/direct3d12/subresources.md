---
title: Подресурсы (графика Direct3D 12)
description: Описывает разделение ресурса на подресурсы и ссылку на один, несколько или срез подресурсов.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fc4478e71bbafb8a21897f838ee8091592024a4e3c761280911e395f8ae491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911975"
---
# <a name="subresources-direct3d-12-graphics"></a>Подресурсы (графика Direct3D 12)

Описывает разделение ресурса на подресурсы и ссылку на один, несколько или срез подресурсов.

-   [Примеры подресурсов](#example-subresources)
    -   [Индексирование подресурсов](#subresource-indexing)
    -   [Срез MIP](#mip-slice)
    -   [Срез массива](#array-slice)
    -   [Срез плоскости](#plane-slice)
    -   [Несколько подресурсов](#multiple-subresources)
-   [API-интерфейсы подресурсов](#subresource-apis)
-   [Связанные темы](#related-topics)

## <a name="example-subresources"></a>Примеры подресурсов

Если ресурс содержит буфер, то он просто содержит один подресурс с индексом 0. Если ресурс содержит текстуру (или массив текстуры), то ссылки на подресурсы сложнее.

Некоторые интерфейсы API обращаются ко всему ресурсу (например, к методу [**ID3D12GraphicsCommandList:: копиресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) ), а другие обращаются к части ресурса (например, к методу [**ID3D12Resource:: реадфромсубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ). Методы, обращающиеся к части ресурса, обычно используют описание представления (например, структуру [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) ) для указания подресурсов для доступа. Полный список см. в разделе [API-интерфейсы подресурсов](#subresource-apis) .

### <a name="subresource-indexing"></a>Индексирование подресурсов

Чтобы индексировать конкретный вложенный ресурс, уровни MIP индексируются Первыми при индексировании каждой записи массива.

![индексирование подресурсов](images/subresource-index.png)

### <a name="mip-slice"></a>Срез MIP

Срез MIP содержит по одному уровню mipmap для каждой текстуры в массиве, как показано на следующем рисунке.

![срезы MIP подресурсов](images/subresource-mip-slice.png)

### <a name="array-slice"></a>Срез массива

Учитывая массив текстур, каждая текстура с MIP-карты, срез массива включает одну текстуру и все ее MIP уровни, как показано на следующем рисунке.

![срезы массива подресурсов](images/subresource-array-slices.png)

### <a name="plane-slice"></a>Срез плоскости

Обычно плоские форматы не используются для хранения данных RGBA, но в тех случаях, когда это (возможно, 24 RGB-данные), одна плоскость может представлять красный рисунок, один зеленый и один синий. Хотя одна плоскость не обязательно является одним цветом, два или более цвета можно объединить в одну плоскость. Обычно плоские данные используются для подвыборки Икбкр и Depth-Stencil данных. Depth-Stencil является единственным форматом, который полностью поддерживает MIP-карты, массивы и несколько плоскостей (часто плоскости 0 для глубины и плоскости 1 для набора элементов).

Ниже показано индексирование подресурсов для массива из двух Depth-Stencil изображений, каждый из которых имеет три уровня MIP.

![индексирование трафаретов глубины](images/depth-stencil-indexing.png)

Подвыборка Икбкр поддерживает массивы и имеет плоскости, но не поддерживает MIP-карты. Изображения Икбкр имеют две плоскости: один для светимости (Y), с которой важнее человеческий глаз, и один для чроминанце (как CB, так и CR), который менее чувствителен к человеческим глазу. Этот формат обеспечивает сжатие значений чроминанце, чтобы сжать изображение, не влияя на светимость, и является распространенным форматом сжатия видео по этой причине, хотя он используется для сжатия изображений по-прежнему. На рисунке ниже показан формат NV12, указывая, что чроминанце был сжат в один квартал разрешения светимости, то есть ширина каждой плоскости идентична, а плоскость чроминанце — половина высоты плоскости освещенности. Плоскости будут индексироваться как подресурсы аналогичным образом Depth-Stencil примере выше.

![формат NV12](images/ycbcr.png)

Плоские форматы существовали в Direct3D 11, но отдельные плоскости не могут быть адресованы по отдельности, скажем, для операций копирования или сопоставления. Это было изменено в Direct3D 12, чтобы каждая плоскость получала свой идентификатор подресурса. Сравните два следующих метода для вычисления идентификатора подресурса.

Direct3D 11

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

Direct3D 12

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

Большинство аппаратных средств предполагает, что память для плоскости N всегда выделяется сразу после плоскости N-1.

Альтернативой использованию подресурсов является то, что приложение может выделить полностью отдельный ресурс на плоскость. В этом случае приложение понимает данные как плоские и использует несколько ресурсов для их представления.

### <a name="multiple-subresources"></a>Несколько подресурсов

В представлении "шейдер — ресурс" можно выбрать любую прямоугольную область подресурсов, используя один из срезов, описанных выше, и разумное использование полей в структурах представления (например, [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), как показано на рисунке.

![Выбор нескольких подресурсов](images/subresource-multiple.png)

Представление визуализации-целевого объекта может использовать только один подресурс или срез MIP и не может включать подресурсы из нескольких срезов MIP. Это значит, что каждая текстура в представлении целевого объекта должна иметь одинаковый размер. В представлении "шейдер — ресурс" можно выбрать любую прямоугольную область подресурсов, как показано на изображении.

## <a name="subresource-apis"></a>API-интерфейсы подресурсов

Следующие API ссылаются и работают с подресурсами:

Перечисления:

-   [**\_ \_ Тип копирования текстур \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

Следующие структуры содержат индексы *планеслице* , большинство из которых содержат индексы *мипслице* .

-   [**D3D12 \_ TEX2D \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2D \_ array \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ массив \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Следующие структуры содержат индексы *аррайслице* , большинство из которых содержат индексы *мипслице* .

-   [**Представление \_ \_ источника данных массива D3D12 TEX1D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**Представление \_ \_ источника данных массива D3D12 TEX2D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**Представление \_ \_ источника данных массива D3D12 TEX2DMS \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**D3D12 \_ TEX1D \_ array \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ array \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ array \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX1D \_ массив \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ массив \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ массив \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX1D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Следующие структуры содержат индексы *мипслице* , но ни *Аррайслице* , ни *планеслице* индексы.

-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ РТВ**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

Следующие структуры также ссылаются на подресурсы:

-   [**D3D12 \_ УДАЛИТЬ \_ регион**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : структура, используемая при подготовке к отмене ресурса.
-   [**D3D12 \_ Размещение размещенных \_ \_ подресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) . добавляет смещение в ресурс к базовому объему.
-   [**D3D12 \_ \_ \_ Барьер переключения ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : описывает переход подресурсов между различными использованиями (ресурс шейдера, целевой объект прорисовки и т. д.).
-   [**D3D12 \_ \_Данные подресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : данные о подресурсе включают сами данные, а также шаг строки и срез.
-   [**D3D12 \_ \_Занимаемое ПОДресурсом**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) место: формат, ширина, высота, глубина и шаг строки для вложенного ресурса.
-   [**D3D12 \_ \_Сведения о ПОДресурсе**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : содержит смещение, шаг строки и шаг глубины для вложенного ресурса.
-   [**D3D12 \_ \_Мозаичное заполнение подресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) . Описание тома подресурсов мозаики (см. раздел [ресурсы для мозаичного размещения томов](volume-tiled-resources.md)).
-   [**D3D12 \_ \_ \_ Расположение для копирования текстуры**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : описывает часть текстуры для копирования.
-   [**D3D12 \_ \_ \_ КООРДИНАТа мозаичного ресурса**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : описывает координаты мозаичного ресурса.

Методы:

-   [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : получает сведения о ресурсе, чтобы обеспечить возможность копирования.
-   [**ID3D12Device:: жетресаурцетилинг**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : получает сведения о том, как мозаичный ресурс разбивается на плитки.
-   [**ID3D12GraphicsCommandList:: ресолвесубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : копирует многовыборочный составной ресурс в многовыборочную подресурс.
-   [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : возвращает указатель на указанные данные в ресурсе и запрещает доступ GPU к подресурсу.
-   [**ID3D12Resource:: реадфромсубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : копирует данные из подресурса или прямоугольной области подресурса.
-   [**ID3D12Resource::**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) unmaps: отменяет сопоставление указанного диапазона памяти и делает указатель на ресурс недействительным. Возобновление доступа GPU к подресурсу.
-   [**ID3D12Resource:: вритетосубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : копирует данные во подресурс или прямоугольную область подресурса.

Текстуры должны находиться в состоянии [**\_ ресурса D3D12 \_ \_ Общее**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) состояние для доступа ЦП через [**вритетосубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) , а [**реадфромсубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) — как юридические, но буферы — нет. Доступ ЦП к ресурсу обычно осуществляется через сопоставление [**сопоставления**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Привязка ресурсов](resource-binding.md)
</dt> </dl>

 

 




