---
description: Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: 'Метод ID3DXMATRIXStack:: Ротатэйавпитчролл (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5020cb6ff3af41b9ef32ef77bb71607f6cd5ea6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713548"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: Ротатэйавпитчролл (D3dx9math. h)

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

## <a name="remarks"></a>Комментарии

Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



Так как поворот разворачивается вправо до стека матрицы, вращение происходит относительно пространства координат мира.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Ротатеаксис**](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Ротатеаксислокал**](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Ротатэйавпитчролллокал**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
