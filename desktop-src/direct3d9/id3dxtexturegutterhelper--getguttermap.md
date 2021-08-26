---
description: Получает значение класса шаг текселя, которое указывает класс шаг текселя в соответствии с расположением каждого шаг текселя.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'Метод ID3DXTextureGutterHelper:: Жетгуттермап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ef2ed7b088e54dd82b1cc99422e1488139199ffe034e810de8e0a0bdb242f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095694"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a>Метод ID3DXTextureGutterHelper:: Жетгуттермап

Получает значение класса шаг текселя, которое указывает класс шаг текселя в соответствии с расположением каждого шаг текселя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуттердата* \[ в, out\]
</dt> <dd>

Тип: **[ **Byte**](../winprog/windows-data-types.md)\***

Указатель на класс шаг текселя. Возможны следующие классы шаг текселя. Отсутствует класс шаг текселя 3.



| Класс шаг текселя | Расположение шаг текселя                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Недопустимая точка; шаг текселя не будет использоваться.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Внутри треугольника.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Внутренняя часть.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Внутреннее внутреннее поле; шаг текселя будет оцениваться как полный пример в методах [**ID3DXTextureGutterHelper:: апплигуттерсфлоат**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: апплигуттерстекс**](id3dxtexturegutterhelper--applygutterstex.md)или [**ID3DXTextureGutterHelper:: апплигуттерспрт**](id3dxtexturegutterhelper--applyguttersprt.md) . |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="remarks"></a>Remarks

Приложение должно выделить Пгуттердата и управлять им с размером, определенным:


```
texture width * texture height * sizeof(BYTE)
```



Ширина и высота текстуры возвращаются [**ID3DXTextureGutterHelper:: полуширинные**](id3dxtexturegutterhelper--getwidth.md) и [**ID3DXTextureGutterHelper:: Height**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
