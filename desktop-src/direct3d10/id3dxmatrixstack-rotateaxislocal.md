---
description: 'Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3DX10. h) — поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.'
ms.assetid: 90837762-9bfe-4065-94b3-1ca61184a78e
title: 'Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a81a4c4bd9a2f738274f98ce925799b34986fbb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107882"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx10h"></a>Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3DX10. h)

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

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на произвольную ось поворота. См. [**D3DXVECTOR3**](d3d10-d3dxvector3.md).

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
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Так как поворот влево умножается на стек матрицы, поворот происходит относительно локального пространства координат объекта.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
