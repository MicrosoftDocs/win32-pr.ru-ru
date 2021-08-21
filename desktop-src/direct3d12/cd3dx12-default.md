---
title: Структура CD3DX12_DEFAULT (D3dx12. h)
description: Передает D3D12 \_ по умолчанию в конструктор для каждой вспомогательной структуры. Эта структура просто используется в качестве механизма установки параметров по умолчанию для других вспомогательных структур.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- Структура CD3DX12_DEFAULT
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 876fbb5e666680e85854196fb9136bfd4d765d6eecf8f16bf6101bb321a7039a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531291"
---
# <a name="cd3dx12_default-structure"></a>\_Структура по умолчанию CD3DX12

Передает D3D12 \_ по умолчанию в конструктор для каждой вспомогательной структуры. Эта структура просто используется в качестве механизма установки параметров по умолчанию для других вспомогательных структур.

## <a name="remarks"></a>Remarks

Эта структура объявляется следующим образом:

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

Передает D3D12 \_ по умолчанию в конструктор для каждой вспомогательной структуры. Например, следующий конструктор объявлен в d3dx12. h:

\_Дескриптор CD3DX12 \_ ЦП \_ (CD3DX12 \_ по умолчанию) {PTR = 0;}

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





