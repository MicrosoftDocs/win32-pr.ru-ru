---
title: Структура CD3DX12_VIEWPORT (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры окна просмотра D3D12.
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- Структура CD3DX12_VIEWPORT
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713965"
---
# <a name="cd3dx12_viewport-structure"></a>\_Структура окна просмотра CD3DX12

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ окна просмотра D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Окно просмотра CD3DX12 ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ окна просмотра CD3DX12.

</dd> <dt>

**явное \_ окно просмотра CD3DX12 (const D3D12 \_ окно просмотра& o)**
</dt> <dd>

Создает новый экземпляр \_ окна просмотра CD3DX12, инициализируя следующие параметры:

\_окно просмотра const D3D12& o

</dd> <dt>

**явное \_ окно просмотра CD3DX12 (float топлефткс, float топлефти, Width float, float с плавающей запятой, float миндепс = D3D12 \_ min \_ Depth, float MaxDepth = D3D12 \_ Максимальная \_ глубина)**
</dt> <dd>

Создает новый экземпляр \_ окна просмотра CD3DX12, инициализируя следующие параметры:

Топлефткс с плавающей запятой

Топлефти с плавающей запятой

Ширина плавающей запятой

Высота с плавающей запятой

FLOAT Миндепс = \_ Минимальная \_ глубина D3D12

FLOAT maxDepth = \_ Максимальная \_ глубина D3D12

</dd> <dt>

**явное \_ окно просмотра CD3DX12 (тип данных ID3D12Resource, тип данных \* , uint мипслице = 0, float топлефткс = 0,0 f, float топлефти = 0,0 f, float МИНДЕПС = D3D12 \_ min \_ , float MaxDepth = D3D12 \_ Max \_ Depth)**
</dt> <dd>

Создает новый экземпляр \_ окна просмотра CD3DX12, инициализируя следующие параметры:

\*Исходный ID3D12Resource

UINT Мипслице = 0

FLOAT Топлефткс = 0,0 f

FLOAT Топлефти = 0,0 f

FLOAT Миндепс = \_ Минимальная \_ глубина D3D12

FLOAT maxDepth = \_ Максимальная \_ глубина D3D12

</dd> <dt>

**\_Окно просмотра ~ CD3DX12 ()**
</dt> <dd>

Уничтожает экземпляр \_ окна просмотра D3DX12.

</dd> <dt>

**окно "operator const D3D12" \_ окна просмотра& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Окно просмотра D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





