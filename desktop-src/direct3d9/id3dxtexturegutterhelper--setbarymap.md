---
description: Задает координаты шаг текселя барицентрик.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'Метод ID3DXTextureGutterHelper:: Сетбаримап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6a82a28308b3236d81159a555219f2a459dd7d9738f1d42f22148af343da5f0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893234"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a>Метод ID3DXTextureGutterHelper:: Сетбаримап

Задает координаты шаг текселя барицентрик.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбаридата* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , содержащую первые две координаты барицентрик каждого шаг текселя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="remarks"></a>Remarks

Третья координата барицентрик предоставляется следующим образом:


```
1 - ( pBaryData.x + pBaryData.y )
```



Входные координаты барицентрик для этого метода допустимы только для допустимых пикселей текстуры (не являющихся классами 0). [**ID3DXTextureGutterHelper:: жетгуттермап**](id3dxtexturegutterhelper--getguttermap.md) будет возвращать ненулевые значения для допустимого пикселей текстуры.

Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника. Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](http://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




