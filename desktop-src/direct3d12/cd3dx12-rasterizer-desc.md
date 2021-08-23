---
title: Структура CD3DX12_RASTERIZER_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать структуру D3D12 средства программной \_ прорисовки \_ .
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- Структура CD3DX12_RASTERIZER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa95dde87aea8e3c61d0d1fb6de6845f33717f6a46db4df7996a23afd7590b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729434"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a>Структура CD3DX12 средства программной \_ прорисовки \_

Вспомогательная структура, позволяющая легко инициализировать структуру D3D12 средства программной [**\_ прорисовки \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 средство программной \_ прорисовки \_ DESC ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр экземпляра средства создания программной \_ прорисовки CD3DX12 \_ DESC.

</dd> <dt>

**явный CD3DX12 средство программной \_ прорисовки \_ DESC (const D3D12 средство \_ прорисовки \_ DESC& o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 средства \_ прорисовки \_ DESC, инициализированного с содержимым другой структуры средства [**\_ прорисовки D3D12 ( \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) ).

</dd> <dt>

**явное CD3DX12 средство программной \_ прорисовки \_ DESC (CD3DX12 \_ по умолчанию)**
</dt> <dd>

Создает новый экземпляр CD3DX12 средства \_ прорисовки \_ DESC, инициализируемый параметрами по умолчанию.

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

**Explicit CD3DX12, \_ \_ DESC, \_ \_ ФИЛЛМОДЕ, D3D12 режим D3D12, \_ \_ Куллмоде, bool Фронткаунтерклокквисе, int Депсбиас, float Депсбиаскламп, float Слопескаледдепсбиас, BOOL depthClipEnable, bool MultisampleEnable, bool antialiasedLineEnable, uint forcedSampleCount, D3D12 \_ консервативный \_ \_ режим растрирования conservativeRaster)**
</dt> <dd>

Создает новый экземпляр CD3DX12 средства создания программной \_ прорисовки \_ DESC, инициализируя следующие параметры:

[**D3D12 \_ Филлмоде \_ режима заполнения**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode)

[**D3D12 \_ Куллмоде \_ режима отбора**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)

BOOL Фронткаунтерклокквисе

INT Депсбиас

Депсбиаскламп с плавающей запятой

Слопескаледдепсбиас с плавающей запятой

BOOL Депсклипенабле

BOOL Мултисамплинабле

BOOL Антиалиаседлининабле

UINT Форцедсамплекаунт

[**D3D12 \_ КОНСЕРВАТИВНый \_ \_ режим растрирования**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) консервативерастер

</dd> <dt>

**~ CD3DX12ное средство программной \_ прорисовки \_ DESC ()**
</dt> <dd>

Уничтожает экземпляр CD3DX12 средства \_ прорисовки данных \_ DESC.

</dd> <dt>

**Оператор const D3D12 средство программной \_ прорисовки \_ DESC& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**D3D12 средство программной \_ прорисовки \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





