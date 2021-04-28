---
description: 'Метод ID3DXMATRIXStack:: Лоадидентити (D3dx9math. h) — загружает удостоверение в текущую матрицу.'
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: 'Метод ID3DXMATRIXStack:: Лоадидентити (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 663559db0746b9d689066e537c1473f467341cbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093562"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: Лоадидентити (D3dx9math. h)

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
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Лоадматрикс**](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




