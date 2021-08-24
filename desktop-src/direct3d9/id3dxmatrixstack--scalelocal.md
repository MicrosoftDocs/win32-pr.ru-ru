---
description: 'Метод ID3DXMATRIXStack:: Скалелокал (D3dx9math. h) — масштабирование текущей матрицы относительно источника объекта.'
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: 'Метод ID3DXMATRIXStack:: Скалелокал (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 193026cee7e8b483afd0159da87cd356bd479987f776c5e82f7ea3543df77c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748064"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: Скалелокал (D3dx9math. h)

Масштабировать текущую матрицу относительно источника объекта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ScaleLocal(
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

Этот метод Left — Умножает текущую матрицу на вычисленную матрицу масштабирования. Преобразование относится к локальному источнику объекта.


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Scale**](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
