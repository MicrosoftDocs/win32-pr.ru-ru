---
title: Структура CD3DX12_RT_FORMAT_ARRAY (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру массива формата D3D12 RT \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- Структура CD3DX12_RT_FORMAT_ARRAY
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9c153b98e84176d2682f028657176902fb68ebc0e8e1e52c69c196842dc2fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988365"
---
# <a name="cd3dx12_rt_format_array-structure"></a>\_ \_ Структура массива формата CD3DX12 RT \_

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ \_ массива формата D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ Массив формата CD3DX12 RT \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ массива формата CD3DX12 RT \_ .

</dd> <dt>

**явный \_ \_ массив формата CD3DX12 RT \_ (const D3D12 \_ \_ массив формата RT \_& o)**
</dt> <dd>

Создает новый экземпляр \_ \_ массива формата CD3DX12 RT \_ , инициализируемый значениями, скопированными из структуры [**\_ \_ \_ массива формата RT D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> <dt>

**явный \_ \_ массив формата CD3DX12 RT \_ (const \_ ПФОРМАТС формата DXGI \* , uint нумформатс)**
</dt> <dd>

Создает новый экземпляр \_ \_ массива формата CD3DX12 RT \_ , инициализируемый значениями, передаваемыми в списке параметров. Содержимое массива, заданного параметром *пформатс* , копируется в массив элементов **ртформатс**. Предполагается, что массив, заданный параметром *пформатс* , имеет тот же размер, что и **ртформатс**.

</dd> <dt>

**Константа Array const D3D12 \_ \_ формата RT \_& () const**
</dt> <dd>

Неявное преобразование в структуру [**\_ \_ \_ массива формата D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) . Поскольку \_ \_ массив формата D3D12 RT \_ является базовым типом CD3DX12 \_ \_ DESC1 трафарета глубины \_ , объект просто возвращается как \_ ссылка на массив формата const D3D12 \_ RT \_ .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_ \_ Массив формата D3D12 \_ RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





