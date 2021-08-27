---
description: Описывает Векторный ключ для использования в анимации по ключевым кадрам. Задает вектор в заданный момент времени. Используется для ключей масштабирования и преобразования.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: Структура D3DXKEY_VECTOR3 (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0214582b3fb1267caeb30a6cca905cbf7243ecf5dd1af40365841b315359317f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119184"
---
# <a name="d3dxkey_vector3-structure"></a>\_Структура VECTOR3 D3DXKEY

Описывает Векторный ключ для использования в анимации по ключевым кадрам. Задает вектор в заданный момент времени. Используется для ключей масштабирования и преобразования.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a>Члены

<dl> <dt>

**Время**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Метка времени ключевого кадра.

</dd> <dt>

**Значение**
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)**

</dd> <dd>

[**D3DXVECTOR3**](d3dxvector3.md) трехмерный вектор, предоставляющий значения для масштабирования и (или) преобразования.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
