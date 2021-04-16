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
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720889"
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

**Time**
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
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
