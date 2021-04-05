---
description: Выполняет Catmull-Rom интерполяцию с использованием указанных векторов 4D.
ms.assetid: e3a10989-e25e-46fa-b72e-bade936cacf1
title: Функция D3DXVec4CatmullRom (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 8e027272a038f17a77dbeda861d6be909afa2f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000335"
---
# <a name="d3dxvec4catmullrom-function-d3dx10mathh"></a>Функция D3DXVec4CatmullRom (D3DX10Math. h)

Выполняет Catmull-Rom интерполяцию с использованием указанных векторов 4D.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Указатель на [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , который является результатом операции.

</dd> <dt>

*pV0* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Указатель на исходную структуру D3DXVECTOR4, вектор позиции.

</dd> <dt>

*pV1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Указатель на исходную структуру D3DXVECTOR4, вектор позиции.

</dd> <dt>

*pV2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Указатель на исходную структуру D3DXVECTOR4, вектор позиции.

</dd> <dt>

*pV3* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Указатель на исходную структуру D3DXVECTOR4, вектор позиции.

</dd> <dt>

*s* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Весовой коэффициент. См. заметки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Указатель на структуру D3DXVECTOR4, которая является результатом интерполяции Catmull-Rom.

## <a name="remarks"></a>Комментарии

Учитывая четыре точки (P1, P2, P3, P4), найдите функцию Q (с) таким образом:


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



Catmull-Rom сплайн может быть производным от сплайна Хермите, настроив:


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



где:

значение v1 является содержимым pV0.

v2 в содержимом pV1.

P3 — это содержимое pV2.

P4 — это содержимое pV3.

С помощью уравнения сплайна Хермите:


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



и подстановка для v1, v2, T1, T2 выдает:


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



Его можно расположить следующим образом:


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
