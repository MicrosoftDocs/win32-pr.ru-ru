---
description: Сопоставляет индексы в диапазоне от 0 до 255 с соответствующими состояниями преобразования.
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
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547858"
---
# <a name="d3dts_worldmatrix-macro"></a>\_Макрос D3DTS ворлдматрикс

Сопоставляет индексы в диапазоне от 0 до 255 с соответствующими состояниями преобразования.

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

## <a name="remarks"></a>Комментарии

Состояния преобразования в диапазоне от 256 до 511 зарезервированы для хранения до 256 матриц, которые можно индексировать с помощью 8-разрядных индексов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**сеттрансформ**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
