---
title: Структура CD3DX12_DEPTH_STENCIL_DESC1 (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру DESC1 шаблона глубины D3D12 \_ .
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- Структура CD3DX12_DEPTH_STENCIL_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647817"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a>\_ \_ Структура DESC1 набора элементов глубины CD3DX12 \_

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ \_ DESC1 шаблона глубины D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ \_ трафарет \_ DESC1 ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1.

</dd> <dt>

**Explicit CD3DX12 \_ \_ трафарет \_ DESC1 (const D3D12 \_ трафарет глубины \_ \_ DESC1& o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, скопированными из структуры [**\_ \_ \_ DESC1 набора элементов глубины D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .

</dd> <dt>

**явный CD3DX12 \_ \_ трафарет \_ DESC1 (const D3D12 \_ трафарет глубины \_ , \_ DESC& o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, скопированными из структуры [**\_ \_ набора элементов \_ глубины D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

а дополнительный элемент **депсбаундстестенабле** имеет значение **false**.

</dd> <dt>

**явное \_ CD3DX12 \_ шаблона глубины \_ DESC1 ( \_ по умолчанию CD3DX12)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, который инициализируется с состоянием по умолчанию, предписанным D3DX12:

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

**явный CD3DX12 \_ \_ трафарет \_ DESC1 (bool депсенабле, D3D12- \_ \_ маска записи \_ , депсвритемаск, D3D12 \_ Сравнение \_ Func ДЕПСФУНК, bool СТЕНЦИЛЕНАБЛЕ, UINT8 СтенЦилреадмаск, UINT8 стенЦилвритемаск, D3D12 \_ трафарет \_ Op frontStencilFailOp, D3D12 \_ трафарет \_ Op \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ frontStencilDepthFailOp, D3D12 трафарет Op frontStencilPassOp, D3D12-, frontStencilFunc, D3D12 наборов элементов**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, передаваемыми в списке параметров.

</dd> <dt>

**~ CD3DX12 \_ \_ трафарет \_ DESC1 ()**
</dt> <dd>

Уничтожает экземпляр D3DX12 \_ \_ трафарета глубины \_ DESC1.

</dd> <dt>

**const const D3D12 \_ \_ шаблона глубины \_ DESC1& () константа**
</dt> <dd>

Неявное преобразование в \_ \_ структуру DESC1 шаблона глубины D3D12 \_ . Так как \_ D3D12 \_ \_ DESC1 трафарет является базовым типом CD3DX12 \_ \_ набора элементов глубины \_ DESC1, он просто возвращается в виде const D3D12 \_ \_ шаблона глубины \_ DESC1 ссылкой на самого себя.

</dd> <dt>

**const const D3D12 \_ \_ шаблона глубины \_ "оператор"**
</dt> <dd>

Неявное преобразование в \_ \_ значение структуры D3D12 в трафарете глубины \_ . Поскольку D3D12 \_ \_ в наборе элементов глубины не \_ является базовым типом \_ CD3DX12 \_ DESC1 трафарета глубины \_ , \_ создается новый \_ экземпляр набора элементов глубины D3D12, который \_ возвращается по значению. Обратите внимание, что D3D12 в \_ \_ наборе элементов глубины не \_ включает элемент **депсбаундстестенабле** , поэтому это значение теряется при преобразовании.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ \_ трафарета глубины \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[**D3D12 \_ \_ трафарета \_ глубины**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





