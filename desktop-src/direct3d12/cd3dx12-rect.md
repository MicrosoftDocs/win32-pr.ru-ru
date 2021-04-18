---
title: Структура CD3DX12_RECT (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру Rect D3D12.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- Структура CD3DX12_RECT
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713515"
---
# <a name="cd3dx12_rect-structure"></a>\_Структура Rect CD3DX12

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ Rect D3D12**](d3d12-rect.md) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ Rect ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ Rect.

</dd> <dt>

**явный CD3DX12 \_ Rect (const D3D12 \_ Rect& o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ Rect, инициализируемый с помощью содержимого другой структуры [**D3D12 \_ Rect**](d3d12-rect.md) .

</dd> <dt>

**явный \_ прямоугольник CD3DX12 (длинный левый, длинный верхний, длинный правый, длинный нижний)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ Rect, инициализируя следующие параметры:

ДЛИННое левое

ДЛИННое сверху

ДЛИННое право

ДЛИННое нижнее

</dd> <dt>

**~ CD3DX12 \_ Rect ()**
</dt> <dd>

Уничтожает экземпляр \_ Rect CD3DX12.

</dd> <dt>

**Константа operator const D3D12 \_ RECT& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**D3D12 \_ Rect**](d3d12-rect.md)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





