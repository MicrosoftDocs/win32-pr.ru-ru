---
description: Создает кватернион с заданными значения нутации, шагом и рулоном.
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: Функция D3DXQuaternionRotationYawPitchRoll (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d0df60149643db0d9243afe57e394320f81d08c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703773"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a>Функция D3DXQuaternionRotationYawPitchRoll (D3dx9math. h)

Создает кватернион с заданными значения нутации, шагом и рулоном.

## <a name="syntax"></a>Синтаксис


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.

</dd> <dt>

*Значения нутации* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Значения нутации вокруг оси y (в радианах).

</dd> <dt>

*Шаг* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Шаг вокруг оси x в радианах.

</dd> <dt>

*Рулон* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Поворот вокруг оси z в радианах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) с указанными значения нутации, шагом и рулоном.

## <a name="remarks"></a>Комментарии

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXQuaternionRotationYawPitchRoll** может использоваться в качестве параметра для другой функции.

Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
</dt> <dt>

[**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
