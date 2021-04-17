---
description: Выполняет вычисление ограничивающей сферы всех сеток в иерархии фреймов.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: Функция D3DXFrameCalculateBoundingSphere (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f10043d2c897bf6ab24c442b8e134f31221c498e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703789"
---
# <a name="d3dxframecalculateboundingsphere-function"></a>Функция D3DXFrameCalculateBoundingSphere

Выполняет вычисление ограничивающей сферы всех сеток в иерархии фреймов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфрамерут* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXFRAME**](d3dxframe.md) \***

Указатель на корневой узел.

</dd> <dt>

*побжектцентер* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXVECTOR3**](d3dxvector3.md)**

Возвращает центр ограничивающей сферы.

</dd> <dt>

*побжектрадиус* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Возвращает радиус ограничивающей сферы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции анимации](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
