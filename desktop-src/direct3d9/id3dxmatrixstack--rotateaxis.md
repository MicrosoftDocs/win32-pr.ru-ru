---
description: 'Метод ID3DXMATRIXStack:: Ротатеаксис (D3dx9math. h) — поворачивает (относительно мирового пространства координат) вокруг произвольной оси.'
ms.assetid: b7ae5195-a2af-429f-9a0d-51cd7e955362
title: 'Метод ID3DXMATRIXStack:: Ротатеаксис (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ea62b65bca73eb3fe7b2cd962e1afd9b35d53bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093492"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: Ротатеаксис (D3dx9math. h)

Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на произвольную ось поворота. См. [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*Угол* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Угол поворота для произвольной оси в радианах. Углы измеряются против часовой стрелки при просмотре произвольной оси в направлении к источнику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



Так как поворот разворачивается вправо до стека матрицы, вращение происходит относительно пространства координат мира.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Ротатеаксислокал**](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Ротатэйавпитчролл**](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Ротатэйавпитчролллокал**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
