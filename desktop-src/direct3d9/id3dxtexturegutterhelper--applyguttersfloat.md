---
description: Применяет переплет к буферу текстуры с плавающей запятой.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'Метод ID3DXTextureGutterHelper:: Апплигуттерсфлоат (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c0401a6d0692331adf9e80c800530690e59eeec5e6a9463b57425af1a3f9330
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800367"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a>Метод ID3DXTextureGutterHelper:: Апплигуттерсфлоат

Применяет переплет к буферу текстуры с плавающей запятой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на буфер данных текстуры с плавающей запятой.

</dd> <dt>

*Нумкоеффс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Число скаляров на цветовой канал, используемое в памяти для хранения образцов. Каждый шаг текселя содержит значения Нумкоеффс FLOAT.

</dd> <dt>

*Ширина* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Ширина текстуры в пикселях, полученная из [**ID3DXTextureGutterHelper:: полуширинные**](id3dxtexturegutterhelper--getwidth.md).

</dd> <dt>

*Высота* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Высота текстуры (в пикселях), полученная из [**ID3DXTextureGutterHelper:: Height**](id3dxtexturegutterhelper--getheight.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="remarks"></a>Remarks

[**Класс 2 пикселей текстуры**](id3dxtexturegutterhelper.md) создается путем повторной выборки класса 1 и 4 пикселей текстуры.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
