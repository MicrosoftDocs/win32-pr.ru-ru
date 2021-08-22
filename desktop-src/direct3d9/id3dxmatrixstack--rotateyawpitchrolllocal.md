---
description: 'Метод ID3DXMATRIXStack:: Ротатэйавпитчролллокал (D3dx9math. h) — поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.'
ms.assetid: c69f5ea7-5d14-4187-9405-1ceff8230185
title: 'Метод ID3DXMATRIXStack:: Ротатэйавпитчролллокал (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cd1355039a570f0ef0e3546150cb9d8ebed5900b88ba14b6640f3d8a1799150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493193"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: Ротатэйавпитчролллокал (D3dx9math. h)

Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RotateYawPitchRollLocal(
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
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Так как поворот влево умножается на стек матрицы, поворот происходит относительно локального пространства координат объекта.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Ротатеаксис**](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Ротатеаксислокал**](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Ротатэйавпитчролл**](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> </dl>

 

 
