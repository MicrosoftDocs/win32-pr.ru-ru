---
title: Структура CD3DX12_CLEAR_VALUE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию структуры D3D12ного \_ \_ значения.
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- Структура CD3DX12_CLEAR_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785ab3c8312949bfc692fcd7c8d1dace28734ce08e5763387a744eb28f2000f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988494"
---
# <a name="cd3dx12_clear_value-structure"></a>\_Структура открытого \_ значения CD3DX12

Вспомогательная структура, позволяющая упростить инициализацию структуры [**D3D12ного \_ \_ значения**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12ое \_ \_ значение Clear ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ значения Clear.

</dd> <dt>

**явное \_ CD3DX12 \_ значение Clear (const D3D12 \_ очистить \_ значение &o)**
</dt> <dd>

Создает новый экземпляр \_ значения CD3DX12 Clear \_ , инициализированного с содержимым другой структуры [**D3D12 \_ clear \_ value**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .

</dd> <dt>

**CD3DX12 \_ \_ значение Clear ( \_ Формат формата DXGI, КОНСТАНТа с плавающей запятой, цвет \[ 4 \] )**
</dt> <dd>

Создает новый экземпляр \_ значения CD3DX12 Clear \_ , инициализируя следующие параметры:

[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Цвет 4 с плавающей запятой \[\]

</dd> <dt>

**CD3DX12 \_ \_ значение Clear ( \_ Формат формата DXGI, глубина float, набор элементов UINT8)**
</dt> <dd>

Создает новый экземпляр \_ значения CD3DX12 Clear \_ , инициализируя следующие параметры:

[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Глубина плавающего числа

Набор элементов UINT8

</dd> <dt>

**Оператор const D3D12 \_ clear \_ значение& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**D3D12ое \_ \_ значение**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

