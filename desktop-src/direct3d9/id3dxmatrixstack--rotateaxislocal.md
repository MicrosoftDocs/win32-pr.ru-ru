---
description: Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: 'Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8488f6314eb926495baa2e42df9ea01616131507
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713550"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3dx9math. h)

Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RotateAxisLocal(
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

## <a name="remarks"></a>Комментарии

Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Так как поворот влево умножается на стек матрицы, поворот происходит относительно локального пространства координат объекта.

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

[**ID3DXMATRIXStack:: Ротатэйавпитчролл**](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Ротатэйавпитчролллокал**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
