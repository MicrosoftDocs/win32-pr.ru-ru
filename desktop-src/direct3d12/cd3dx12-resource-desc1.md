---
title: Структура CD3DX12_RESOURCE_DESC1 (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать структуру [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) .
keywords:
- Структура CD3DX12_RESOURCE_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 87fe62c475e1d961258671355c4c9be133bf0a41
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813238"
---
# <a name="cd3dx12_resource_desc1-structure"></a>Структура CD3DX12_RESOURCE_DESC1

Вспомогательная структура, позволяющая легко инициализировать структуру [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) .

## <a name="syntax"></a>Синтаксис

```cpp
struct CD3DX12_RESOURCE_DESC1 : public D3D12_RESOURCE_DESC1
{
    CD3DX12_RESOURCE_DESC1();
    explicit CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1& o) noexcept;
    CD3DX12_RESOURCE_DESC1(
        D3D12_RESOURCE_DIMENSION dimension,
        UINT64 alignment,
        UINT64 width,
        UINT height,
        UINT16 depthOrArraySize,
        UINT16 mipLevels,
        DXGI_FORMAT format,
        UINT sampleCount,
        UINT sampleQuality,
        D3D12_TEXTURE_LAYOUT layout,
        D3D12_RESOURCE_FLAGS flags,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        UINT64 width,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex1D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex2D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        UINT sampleCount = 1,
        UINT sampleQuality = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex3D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 depth,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    inline UINT16 Depth() const noexcept;
    inline UINT16 ArraySize() const noexcept;
    inline UINT8 PlaneCount(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT Subresources(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice) noexcept;
};
inline bool operator==(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
inline bool operator!=(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
```

## <a name="members"></a>Члены

`CD3DX12_RESOURCE_DESC1`

Конструктор по умолчанию. Создает новый, неинициализированный экземпляр **CD3DX12_RESOURCE_DESC1**.

`CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1&)`

Конструктор, создающий новый экземпляр **CD3DX12_RESOURCE_DESC1** , инициализируемый с помощью содержимого структуры [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) .

`CD3DX12_RESOURCE_DESC1(D3D12_RESOURCE_DIMENSION, UINT64, UINT64, UINT, UINT16, UINT16, DXGI_FORMAT, UINT, UINT, D3D12_TEXTURE_LAYOUT, D3D12_RESOURCE_FLAGS, UINT = 0, UINT = 0, UINT = 0)`

Конструктор, создающий новый экземпляр **CD3DX12_RESOURCE_DESC1** , инициализируемый параметрами, переданными в него.

`Buffer(const D3D12_RESOURCE_ALLOCATION_INFO&, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE)`

Статическая функция, которая конструирует и возвращает новый экземпляр **CD3DX12_RESOURCE_DESC1** , инициализированный этими значениями.

|Элемент данных|Значение|
|-|-|
|Измерение|D3D12_RESOURCE_DIMENSION_BUFFER|
|Выравнивание|*ресаллоЦинфо*. Выравнивание|
|Ширина|*ресаллоЦинфо*. сизеинбитес|
|Высота|1|
|депсораррайсизе|1|
|миплевелс|1|
|Формат|DXGI_FORMAT_UNKNOWN|
|Сампледеск. Count|1|
|Сампледеск. качество|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Флаги|*flags*|
|Самплерфидбаккмипрегион. Width|0|
|Самплерфидбаккмипрегион. Height|0|
|Самплерфидбаккмипрегион. Глубина|0|

`Buffer(UINT64, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, UINT64 = 0)`

Статическая функция, которая конструирует и возвращает новый экземпляр **CD3DX12_RESOURCE_DESC1** , инициализированный этими значениями.

|Элемент данных|Значение|
|-|-|
|Измерение|D3D12_RESOURCE_DIMENSION_BUFFER|
|Выравнивание|*Выравнивание*|
|Ширина|*width*|
|Высота|1|
|депсораррайсизе|1|
|миплевелс|1|
|Формат|DXGI_FORMAT_UNKNOWN|
|Сампледеск. Count|1|
|Сампледеск. качество|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Флаги|*flags*|
|Самплерфидбаккмипрегион. Width|0|
|Самплерфидбаккмипрегион. Height|0|
|Самплерфидбаккмипрегион. Глубина|0|

`Tex1D(DXGI_FORMAT, UINT64, UINT16 = 1, UINT16 = 0, D3D12_RESOURCE_FLAGS D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Статическая функция, которая конструирует и возвращает новый экземпляр **CD3DX12_RESOURCE_DESC1** , инициализированный этими значениями.

|Элемент данных|Значение|
|-|-|
|Измерение|D3D12_RESOURCE_DIMENSION_TEXTURE1D|
|Выравнивание|*Выравнивание*|
|Ширина|*width*|
|Высота|1|
|депсораррайсизе|*Размера массива*|
|миплевелс|*миплевелс*|
|Формат|*format*|
|Сампледеск. Count|1|
|Сампледеск. качество|0|
|Layout|*режим*|
|Флаги|*flags*|
|Самплерфидбаккмипрегион. Width|0|
|Самплерфидбаккмипрегион. Height|0|
|Самплерфидбаккмипрегион. Глубина|0|

`Tex2D(DXGI_FORMAT, UINT64, UINT, UINT16 = 1, UINT16 = 0, UINT = 1, UINT = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0, UINT = 0, UINT = 0, UINT = 0)`

Статическая функция, которая конструирует и возвращает новый экземпляр **CD3DX12_RESOURCE_DESC1** , инициализированный этими значениями.

|Элемент данных|Значение|
|-|-|
|Измерение|D3D12_RESOURCE_DIMENSION_TEXTURE2D|
|Выравнивание|*Выравнивание*|
|Ширина|*width*|
|Высота|*height*|
|депсораррайсизе|*Размера массива*|
|миплевелс|*миплевелс*|
|Формат|*format*|
|Сампледеск. Count|*sampleCount*|
|Сампледеск. качество|*самплекуалити*|
|Layout|*режим*|
|Флаги|*flags*|
|Самплерфидбаккмипрегион. Width|*самплерфидбаккмипрегионвидс*|
|Самплерфидбаккмипрегион. Height|*самплерфидбаккмипрегионхеигхт*|
|Самплерфидбаккмипрегион. Глубина|*самплерфидбаккмипрегиондепс*|

`Tex3D(DXGI_FORMAT, UINT64, UINT, UINT16, UINT16 = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Статическая функция, которая конструирует и возвращает новый экземпляр **CD3DX12_RESOURCE_DESC1** , инициализированный этими значениями.

|Элемент данных|Значение|
|-|-|
|Измерение|D3D12_RESOURCE_DIMENSION_TEXTURE3D|
|Выравнивание|*Выравнивание*|
|Ширина|*width*|
|Высота|*height*|
|депсораррайсизе|*Длина*|
|миплевелс|*миплевелс*|
|Формат|*format*|
|Сампледеск. Count|1|
|Сампледеск. качество|0|
|Layout|*режим*|
|Флаги|*flags*|
|Самплерфидбаккмипрегион. Width|0|
|Самплерфидбаккмипрегион. Height|0|
|Самплерфидбаккмипрегион. Глубина|0|

`Depth`

Возвращает значение типа **UINT16** , содержащее глубину ресурса.

`ArraySize`

Возвращает значение типа **UINT16** , содержащее размер массива ресурса.

`PlaneCount(ID3D12Device*)`

Возвращает значение **UINT8** , содержащее число плоскостей для формата ресурса.

`Subresources(ID3D12Device*)`

Возвращает значение типа **uint** , содержащее количество подресурсов в ресурсе.

`CalcSubresource(UINT, UINT, UINT)`

Какулатес и возвращает значение **uint** , содержащее индекс подресурса для ресурса на основе переданных ему параметров.

`operator==(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Бесплатная функция, возвращающая значение, `true` Если два параметра являются равными по отношению к элементам; в противном случае — значение `false` .

`operator!=(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Бесплатная функция, возвращающая значение, `true` Если два параметра являются одноэлементными и не равны. в противном случае — значение `false` .

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также

* [D3DX12_RESOURCE_DESC1](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1)
* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
