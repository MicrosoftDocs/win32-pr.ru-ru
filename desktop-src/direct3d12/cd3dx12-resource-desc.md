---
title: Структура CD3DX12_RESOURCE_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру ресурсов D3D12 \_ .
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- Структура CD3DX12_RESOURCE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c9d92953abdb0cf77a7a55f7b64341b857a111baaef0d84d4d44855b02efb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028304"
---
# <a name="cd3dx12_resource_desc-structure"></a>\_Структура ресурсов \_ CD3DX12

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ ресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ ресурс \_ DESC ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ ресурса \_ DESC.

</dd> <dt>

**явное CD3DX12 \_ ресурса \_ DESC (const D3D12 \_ ресурс \_ DESC& o)**
</dt> <dd>

Создает новый экземпляр \_ ресурса CD3DX12 \_ DESC, инициализированного с содержимым другой структуры [**ресурса D3D12 ( \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) ).

</dd> <dt>

**CD3DX12 \_ Resource \_ DESC ( \_ \_ измерение измерения ресурса D3D12, выравнивание UInt64, ширина UInt64, высота uint, UInt16 депсораррайсизе, UInt16 МИПЛЕВЕЛС, \_ Формат формата DXGI, uint SAMPLECOUNT, uint самплекуалити, D3D12 \_ \_ Макет макета текстуры, \_ \_ Флаги D3D12 ресурсов)**
</dt> <dd>

Создает новый экземпляр \_ ресурса CD3DX12 \_ DESC, инициализируя следующие параметры:

[**D3D12 \_ Измерение \_ измерения ресурса**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)

Выравнивание UINT64

Ширина UINT64

Высота UINT

UINT16 Депсораррайсизе

UINT16 Миплевелс

[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

UINT sampleCount

UINT Самплекуалити

[**D3D12 \_ Макет \_ текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)

[**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags)

</dd> <dt>

**статический встроенный буфер (const D3D12 \_ \_ сведения о выделении ресурсов \_& ресаллоЦинфо, флаги \_ \_ флагов ресурсов D3D12 = D3D12 \_ ресурс \_ флаг \_ None)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ \_ \_ Сведения о выделении ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& ресаллоЦинфо

участие [**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = \_ флаг ресурса D3D12 \_ \_ нет

</dd> <dt>

**статический встроенный буфер (ширина UINT64, флаги \_ \_ флагов ресурсов D3D12 = D3D12 \_ ресурс \_ флаг \_ None, выравнивание UINT64 = 0)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

Ширина UINT64

участие [**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = \_ флаг ресурса D3D12 \_ \_ нет

участие UINT64 выравнивание = 0

</dd> <dt>

**static Inline Tex1D ( \_ Формат формата DXGI, ширина UINT64, UINT16 размера массива = 1, UINT16 миплевелс = 0, флаги \_ \_ флагов ресурсов D3D12 = D3D12 \_ ресурс \_ флаг \_ None, \_ D3D12 \_ Макет макета = D3D12 \_ \_ Макет текстуры \_ Unknown, выравнивание UINT64 = 0)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Ширина UINT64

участие UINT16 размера массива = 1

участие UINT16 Миплевелс = 0

участие [**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = \_ флаг ресурса D3D12 \_ \_ нет

участие [**D3D12 \_ Макет \_ текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) — \_ \_ НЕизвестный макет текстуры \_ D3D12

участие UINT64 выравнивание = 0

</dd> <dt>

**static Inline Tex2D ( \_ Формат формата DXGI, ширина UINT64, высота uint, UINT16 размера массива = 1, UINT16 миплевелс = 0, uint sampleCount = 1, uint самплекуалити = 0, флаги \_ \_ флагов ресурсов D3D12 = D3D12, \_ \_ флаг \_ , параметр D3D12, макет \_ текстуры \_ = \_ D3D12 \_ \_**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Ширина UINT64

Высота UINT

участие UINT16 размера массива = 1

участие UINT16 Миплевелс = 0

участие UINT sampleCount = 1

участие UINT Самплекуалити = 0

участие [**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = \_ флаг ресурса D3D12 \_ \_ нет

участие [**D3D12 \_ Макет \_ текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) — \_ \_ НЕизвестный макет текстуры \_ D3D12

участие UINT64 выравнивание = 0

</dd> <dt>

**статическое встроенное Tex3D ( \_ Формат формата DXGI, ширина UINT64, высота uint, длина UInt16, UInt16 миплевелс = 0, \_ \_ Флаги флагов ресурсов D3D12 = D3D12 \_ ресурс \_ флаг \_ None, D3D12 макет \_ \_ макета текстуры = D3D12 \_ \_ Макет текстуры \_ Unknown, выравнивание UINT64 = 0)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Ширина UINT64

Высота UINT

Глубина UINT16

участие UINT16 Миплевелс = 0

участие [**D3D12 \_ Флаги \_ флагов ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = \_ флаг ресурса D3D12 \_ \_ нет

участие [**D3D12 \_ Макет \_ текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) — \_ \_ НЕизвестный макет текстуры \_ D3D12

участие UINT64 выравнивание = 0

</dd> <dt>

**Константа встроенной глубины ()**
</dt> <dd>

Если Dimension = = [**D3D12 \_ TEXTURE3D \_ измерения**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ , возвращает депсораррайсизе. Если Dimension! = D3D12 \_ \_ TEXTURE3D измерения \_ , возвращает 1.

</dd> <dt>

**Inline размера массива () const**
</dt> <dd>

Если Dimension! = D3D12 \_ \_ TEXTURE3D ресурса измерения \_ , возвращает депсораррайсизе. Если Dimension = = D3D12 \_ \_ TEXTURE3D измерения \_ , возвращает 1. См. раздел [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.

</dd> <dt>

**Inline Планекаунт (ID3D12Device \* пдевице) const**
</dt> <dd>

Возвращает D3D12GetFormatPlaneCount (Пдевице, Format). См. раздел [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) and [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).

</dd> <dt>

**Встроенные подресурсы (ID3D12Device \* пдевице) const**
</dt> <dd>

Возвращает количество подресурсов, вычисленное как Миплевелс \* размера массива () \* Планекаунт (пдевице).

</dd> <dt>

**Inline Калксубресаурце (UINT Мипслице, UINT Аррайслице, UINT Планеслице)**
</dt> <dd>

Вычисляет индекс подресурса с помощью [**D3D12CalcSubresource**](d3d12calcsubresource.md).

</dd> <dt>

**Оператор const D3D12 \_ ресурса \_ DESC& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> <dt>

**оператор = = (const D3D12 \_ Resource \_ DESC& l, const D3D12 \_ ресурс \_ DESC& r)**
</dt> <dd>

Возвращает значение true, если все члены каждой структуры идентичны.

</dd> <dt>

**operator! = (const D3D12 \_ ресурс \_ DESC& l, const D3D12 \_ Resource \_ DESC& r)**
</dt> <dd>

Возвращает значение false, если все члены каждой структуры идентичны.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**D3D12 \_ ресурс \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

