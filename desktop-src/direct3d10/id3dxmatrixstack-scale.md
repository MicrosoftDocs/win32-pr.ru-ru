---
description: 'Метод ID3DXMATRIXStack:: Scale (D3DX10. h). масштабирование текущей матрицы относительно источника координат мира.'
ms.assetid: d0f4b341-b3b6-42e4-84df-78f203c3728e
title: 'Метод ID3DXMATRIXStack:: Scale (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 788c26f129bbd5078a63827653f0ec9b053321f1ca609f6cb1bda032f37c371c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461502"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a>Метод ID3DXMATRIXStack:: Scale (D3DX10. h)

Масштабировать текущую матрицу относительно источника координат мира.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*x* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Компонент масштабирования по оси x.

</dd> <dt>

*y* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Компонент масштабирования в направлении y.

</dd> <dt>

*z* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Компонент масштабирования в направлении z.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод дает право на Умножение текущей матрицы на вычисленную матрицу масштабирования. Преобразование относится к текущему источнику мира.


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a>Requirements (Требования)



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

 

 
