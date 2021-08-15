---
description: 'Метод ID3DXMATRIXStack:: Лоадматрикс (D3dx9math. h) — загружает заданную матрицу в текущую матрицу.'
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: 'Метод ID3DXMATRIXStack:: Лоадматрикс (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1d34a8feff249471363d1b22f94bcd71128e512ab4bb9d506a99c4d2741020bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095894"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: Лоадматрикс (D3dx9math. h)

Загружает заданную матрицу в текущую матрицу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмат* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , загруженную в текущую матрицу.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Обратите внимание, что этот метод не добавляет элемент в стек; Вместо этого он заменяет текущую матрицу представленной матрицей.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Лоадидентити**](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




