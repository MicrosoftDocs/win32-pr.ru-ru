---
description: Получает трансобъектную матрицу.
ms.assetid: 255c1e20-0a60-49eb-abaa-66a67322ce73
title: 'Метод ID3DXBaseEffect:: Жетматрикстранспосе (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 59a23e8cde059446dea33d65f90dca9fb7cb2aaf41ab00949e02e34189420b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987784"
---
# <a name="id3dxbaseeffectgetmatrixtranspose-method"></a>Метод ID3DXBaseEffect:: Жетматрикстранспосе

Получает трансобъектную матрицу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMatrixTranspose(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*пматрикс* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Возвращает переустановленную матрицу. См. [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.

Если целевая матрица больше, чем исходная матрица, будут заполнены только верхние левые элементы целевой матрицы, а остальные компоненты матрицы назначения будут иметь нулевое значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**сетматрикстранспосе**](id3dxbaseeffect--setmatrixtranspose.md)
</dt> </dl>

 

 




