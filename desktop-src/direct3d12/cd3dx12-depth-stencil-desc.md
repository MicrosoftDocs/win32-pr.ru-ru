---
title: Структура CD3DX12_DEPTH_STENCIL_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ структуры набора элементов глубины D3D12 \_ .
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- Структура CD3DX12_DEPTH_STENCIL_DESC
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647820"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a>CD3DX12 \_ \_ Структура набора элементов глубины \_

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ набора элементов \_ глубины D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ \_ трафарета глубины \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ набора элементов глубины D3DX12 \_ DESC.

</dd> <dt>

**CD3DX12 \_ \_ "DESC" явное описание трафарета глубины \_ (const D3D12 \_ \_ набор элементов глубины \_& o)**
</dt> <dd>

Создает новый экземпляр D3DX12 \_ \_ трафарета глубины \_ , инициализированный с содержимым другой структуры [**\_ \_ трафарета \_ глубины D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

</dd> <dt>

**DESC явного CD3DX12 в \_ \_ наборе элементов глубины \_ ( \_ по умолчанию CD3DX12)**
</dt> <dd>

Создает новый экземпляр D3DX12 \_ \_ трафарета глубины \_ , инициализированный параметрами по умолчанию.

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

**явная CD3DX12 \_ \_ набор элементов глубины \_ (bool депсенабле, D3D12 \_ \_ маска записи, \_ депсвритемаск, D3D12 \_ Сравнение \_ Func ДЕПСФУНК, bool СТЕНЦИЛЕНАБЛЕ, UINT8 СтенЦилреадмаск, UINT8 стенЦилвритемаск, D3D12 \_ трафарет \_ Op frontStencilFailOp, D3D12 \_ трафарет \_ Op \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ frontStencilDepthFailOp, D3D12 набор элементов frontStencilPassOp, D3D12 frontStencilFunc D3D12, backStencilFailOp трафарет D3D12 backStencilDepthFailOp, трафарет Func D3D12)**
</dt> <dd>

Создает новый экземпляр D3DX12 \_ \_ набора элементов глубины \_ , инициализируя следующие параметры:

BOOL Депсенабле

[**D3D12 \_ Депсвритемаск \_ \_ маска записи глубины**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask)

[**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) депсфунк

BOOL СтенЦиленабле

UINT8 СтенЦилреадмаск

UINT8 СтенЦилвритемаск

[**D3D12 \_ ФронтстенЦилфаилоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ ФронтстенЦилдепсфаилоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ ФронтстенЦилпассоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) фронтстенЦилфунк

[**D3D12 \_ БаккстенЦилфаилоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ БаккстенЦилдепсфаилоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ БаккстенЦилпассоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) баккстенЦилфунк

</dd> <dt>

**~ CD3DX12 \_ \_ трафарет \_ DESC ()**
</dt> <dd>

Уничтожает экземпляр \_ \_ набора элементов глубины CD3DX12 \_ DESC.

</dd> <dt>

**Константа "operator const D3D12 \_ \_ \_ -трафарет DESC& () const"**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**D3D12 \_ \_ трафарета \_ глубины**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





