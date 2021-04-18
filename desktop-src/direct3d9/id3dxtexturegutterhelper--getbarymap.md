---
description: Получает координаты шаг текселя барицентрик.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'Метод ID3DXTextureGutterHelper:: Жетбаримап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703856"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a>Метод ID3DXTextureGutterHelper:: Жетбаримап

Получает координаты шаг текселя барицентрик.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбаридата* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , содержащую первые две координаты барицентрик каждого шаг текселя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="remarks"></a>Комментарии

Третья координата барицентрик предоставляется следующим образом:


```
    1 - ( pBaryData.x + pBaryData.y )
```



Координаты барицентрик всегда указываются по отношению к треугольнику, возвращенному [**ID3DXTextureGutterHelper:: жетфацемап**](id3dxtexturegutterhelper--getfacemap.md).

Координаты барицентрик, возвращаемые этим методом, допустимы только для допустимых пикселей текстуры (не являющихся классами 0). [**ID3DXTextureGutterHelper:: жетгуттермап**](id3dxtexturegutterhelper--getguttermap.md) будет возвращать ненулевые значения для допустимого пикселей текстуры.

[**Класс 2 пикселей текстуры**](id3dxtexturegutterhelper.md) сопоставляются с ближайшей точкой треугольника в шаг текселя пространстве.

Приложение должно выделить Пбаридата и управлять им.

Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника. Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




