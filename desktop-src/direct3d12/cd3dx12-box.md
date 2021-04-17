---
title: Структура CD3DX12_BOX (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру бокса D3D12.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- Структура CD3DX12_BOX
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694110"
---
# <a name="cd3dx12_box-structure"></a>\_Структура Box CD3DX12

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ бокса D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Поле CD3DX12 ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ поля CD3DX12.

</dd> <dt>

**явное \_ поле CD3DX12 (const D3D12 \_ Box& o)**
</dt> <dd>

Создает новый экземпляр \_ поля CD3DX12, инициализированного с содержимым другой структуры [**\_ Box D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .

</dd> <dt>

**Explicit CD3DX12 \_ (слева, длинное право)**
</dt> <dd>

Создает новый экземпляр \_ поля CD3DX12, инициализируя следующие параметры:

ДЛИННое левое

ДЛИННое право

</dd> <dt>

**Explicit CD3DX12 \_ (длинный левый, длинный верхний, длинный правый, длинный нижний)**
</dt> <dd>

Создает новый экземпляр \_ поля CD3DX12, инициализируя следующие параметры:

ДЛИННое левое

ДЛИННое сверху

ДЛИННое право

ДЛИННое нижнее

</dd> <dt>

**явный CD3DX12 \_ (длинный левый, длинный верхний, длинный передний, длинный правый, длинный нижний, длинный)**
</dt> <dd>

Создает новый экземпляр \_ поля CD3DX12, инициализируя следующие параметры:

ДЛИННое левое

ДЛИННое сверху

ДЛИННая спереди

ДЛИННое право

ДЛИННое нижнее

ДЛИННая резервная копия

</dd> <dt>

**~ CD3DX12 \_ Box ()**
</dt> <dd>

Уничтожает экземпляр \_ поля CD3DX12.

</dd> <dt>

**Оператор const D3D12 \_ BOX& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Поле D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





