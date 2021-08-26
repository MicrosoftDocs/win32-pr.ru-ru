---
title: Отправка данных текстуры через буферы
description: Передача данных двухмерной или трехмерной текстуры аналогична передаче данных 1D, за исключением того, что приложениям необходимо обратить особое внимание на выравнивание данных, связанное с шагом строки.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c095d93237a44369cb249d6de9e514fa7021a91fb78430ddc428c88e4e71b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027994"
---
# <a name="uploading-texture-data-through-buffers"></a>Отправка данных текстуры через буферы

Передача данных двухмерной или трехмерной текстуры аналогична передаче данных 1D, за исключением того, что приложениям необходимо обратить особое внимание на выравнивание данных, связанное с шагом строки. Буферы можно использовать последовательно и параллельно из нескольких частей графического конвейера, и они являются очень гибкими.

-   [Upload Данные текстуры через буферы](#upload-texture-data-via-buffers)
-   [Идет](#copying)
-   [Сопоставление и отмена сопоставления](#mapping-and-unmapping)
-   [Выравнивание буфера](#buffer-alignment)
-   [Связанные темы](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>Upload Данные текстуры через буферы

Приложения должны передавать данные через [**ID3D12GraphicsCommandList:: копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) или [**ID3D12GraphicsCommandList:: копибуфферрегион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion). Данные текстуры, скорее всего, будут более крупными, доступными для многократного доступа и преимуществами улучшенной согласованности в кэше для нелинейных макетов памяти, чем для других данных ресурсов. Когда буферы используются в D3D12, приложения получают полный контроль над размещением и упорядочением данных, связанными с копированием данных ресурсов, при условии, что требования к выравниванию памяти удовлетворяются.

Пример демонстрирует, где приложение просто выполняет сведение 2D-данных в 1D перед помещением в буфер. В случае 2D-сценария mipmap приложение может либо свести каждый дискретными к подресурсу, либо быстро использовать алгоритм подраспределений 1D, или использовать более сложный способ плоского выделения, чтобы свести к минимальному использованию видеопамяти. Первый метод должен использоваться чаще, чем проще. Второй способ может быть полезен при упаковке данных на диск или по сети. В любом случае приложение по-прежнему должно вызывать API копирования для каждого подресурса.

```cpp
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

Обратите внимание на использование вспомогательных [**структур \_ CD3DX12 \_ Свойства кучи**](cd3dx12-heap-properties.md) и [**\_ \_ \_ расположения CD3DX12 текстуры**](cd3dx12-texture-copy-location.md), а также методы [**креатекоммиттедресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) и [**копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

## <a name="copying"></a>Копирование

Методы D3D12 позволяют приложениям заменять начальные данные D3D11 [**упдатесубресаурце**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**кописубресаурцерегион**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)и Resource. В буферных ресурсах может размещаться один трехмерный подресурс с данными текстуры по строкам. [**Копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) может копировать данные текстуры из буфера в ресурс текстуры с неизвестной структурой текстуры и наоборот. Приложения должны предпочесть этот тип приема для заполнения часто используемых ресурсов GPU, создавая большие буферы в куче передачи при создании часто используемых ресурсов GPU в куче по УМОЛЧАНИю без доступа к ЦП. Такой метод эффективно поддерживает отдельные GPU и их большой объем памяти, недоступной для ЦП, без частого нарушения архитектуры.

Обратите внимание на две следующие константы:

```cpp
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**\_Объем ПОДРЕСУРСОВ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**D3D12 \_ размещенных \_ подресурсов \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**\_ \_ Расположение копии текстуры \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**\_ \_ Тип копирования текстур \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList:: Копиресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList:: Копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList:: Копибуфферрегион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList:: Копитилес**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue:: Упдатетилемаппингс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>Сопоставление и отмена сопоставления

[**Сопоставление**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) и [**Отмена сопоставления могут**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) безопасно вызываться несколькими потоками. Первый вызов функции **Map** выделяет диапазон ВИРТУАЛЬНЫХ адресов ЦП для ресурса. Последний вызов метода **сопоставления** освобождает диапазон ВИРТУАЛЬНЫХ адресов ЦП. Виртуальный адрес ЦП обычно возвращается приложению.

Всякий раз, когда данные передаются между ЦП и GPU через ресурсы в кучах реадбакк, для поддержки всех систем, D3D12 поддерживаются, необходимо использовать [**сопоставление**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) и [**сопоставление**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) . Максимально эффективное поддержание диапазонов в системах, требующих диапазонов (см. [**D3D12 \_ Range**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).

Производительность средств отладки не только заключается в точном использовании диапазонов во всех вызовах [**сопоставления карты**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , но и из приложений, которые отменяют сопоставление ресурсов, когда изменения ЦП больше не будут выполняться.

Метод D3D11 с использованием [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (с набором параметров Discard) для переименования ресурсов не поддерживается в D3D12. Приложения должны самостоятельно реализовывать переименование ресурсов. Все вызовы **карт** неявно не \_ переписываются и многопоточные. Необходимо, чтобы все необходимые действия GPU, содержащиеся в списках команд, были завершены до получения доступа к данным с помощью ЦП. Вызовы D3D12 для **Map** не выполняют неявное очистку буферов команд и не блокируют ожидание завершения работы GPU. В результате в некоторых сценариях можно даже оптимизировать **сопоставление** [**и сопоставление**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) .

## <a name="buffer-alignment"></a>Выравнивание буфера

Ограничения выравнивания буфера:

-   При копировании линейных подресурсов должно быть выравниваться до 512 байт (со высотам строки, выровненной по D3D12у \_ \_ \_ выравнивания по высоте данных текстуры \_ ).
-   Число константных операций чтения данных должно быть кратно 256 байт от начала кучи (т. е. только по адресам, поддерживающим 256 байт).
-   Считывание данных индекса должно быть кратным размеру типа данных индекса (т. е. только из адресов, которые естественным образом выровнены для данных).
-   [**ID3D12GraphicsCommandList:: ексекутеиндирект**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) данные должны относиться к значениям смещения, кратным 4 (т. е. только из адресов, которые имеют ВЫРАВНИВАЕМАЯ по значению DWORD).

## <a name="related-topics"></a>Связанные темы

* [Подраспределение в буферах](large-buffers.md)
