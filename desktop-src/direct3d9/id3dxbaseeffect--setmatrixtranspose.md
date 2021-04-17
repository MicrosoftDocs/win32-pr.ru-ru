---
description: Задает трансобъектную матрицу.
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: 'Метод ID3DXBaseEffect:: Сетматрикстранспосе (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f62847f7b15899389cbd5f207ce810b0ed0dd119
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720863"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a>Метод ID3DXBaseEffect:: Сетматрикстранспосе

Задает трансобъектную матрицу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*пматрикс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на переустановленную матрицу. См. [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.

Если целевая матрица меньше, чем исходная матрица, дополнительные компоненты исходной матрицы будут пропущены.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**жетматрикстранспосе**](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




