---
description: 'Метод ID3DXMATRIXStack:: Лоадидентити (D3DX10. h) — загружает удостоверение в текущую матрицу.'
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: 'Метод ID3DXMATRIXStack:: Лоадидентити (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f056a911b19c0ea18f5f728a6ce8c4403dd14587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107992"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a>Метод ID3DXMATRIXStack:: Лоадидентити (D3DX10. h)

Загружает удостоверение в текущую матрицу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Матрица идентификаторов — это матрица, в которой все коэффициенты составляют 0,0, за исключением \[ коэффициентов 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4 и 4 \] , для которых задано значение 1,0. Матрица идентификации является особой в том, что при применении к вершинам они не меняются. Матрица идентификаторов используется в качестве начальной точки для матриц, которые будут изменять значения вершин для создания поворотов, переводов и других преобразований, которые могут быть представлены матрицей 4x4.

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

 

 




