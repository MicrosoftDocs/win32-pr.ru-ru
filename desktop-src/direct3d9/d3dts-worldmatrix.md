---
description: Карты индексы в диапазоне от 0 до 255 для соответствующих состояний преобразования.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: Макрос D3DTS_WORLDMATRIX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 03a93753790378a7066f4a3ffa6bc6b7fb8139b77f9096886161013653312bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850064"
---
# <a name="d3dts_worldmatrix-macro"></a>\_Макрос D3DTS ворлдматрикс

Карты индексы в диапазоне от 0 до 255 для соответствующих состояний преобразования.

## <a name="syntax"></a>Синтаксис


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*index* 
</dt> <dd>

Значение индекса в диапазоне от 0 до 255.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) , сопоставляемый с данным *индексом*.

## <a name="remarks"></a>Remarks

Состояния преобразования в диапазоне от 256 до 511 зарезервированы для хранения до 256 матриц, которые можно индексировать с помощью 8-разрядных индексов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**сеттрансформ**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
