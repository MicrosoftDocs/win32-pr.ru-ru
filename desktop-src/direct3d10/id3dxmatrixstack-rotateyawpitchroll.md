---
description: 'Метод ID3DXMATRIXStack:: Ротатэйавпитчролл (D3DX10. h) — поворачивает (относительно мирового пространства координат) вокруг произвольной оси.'
ms.assetid: 35e237f6-40f2-4001-adb0-f489d61f64e7
title: 'Метод ID3DXMATRIXStack:: Ротатэйавпитчролл (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e43422e5872708a61b5f066725e61c16e55d04dd94f5c8527c7b86e1f7a543c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128336"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx10h"></a>Метод ID3DXMATRIXStack:: Ротатэйавпитчролл (D3DX10. h)

Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Значения нутации* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Значения нутации вокруг оси y в радианах.

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

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



Так как поворот разворачивается вправо до стека матрицы, вращение происходит относительно пространства координат мира.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
