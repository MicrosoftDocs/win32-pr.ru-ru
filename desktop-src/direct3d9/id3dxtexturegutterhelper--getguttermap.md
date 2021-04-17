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
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647853"
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

## <a name="remarks"></a>Комментарии

Приложение должно выделить Пгуттердата и управлять им с размером, определенным:


```
texture width * texture height * sizeof(BYTE)
```



Ширина и высота текстуры возвращаются [**ID3DXTextureGutterHelper:: полуширинные**](id3dxtexturegutterhelper--getwidth.md) и [**ID3DXTextureGutterHelper:: Height**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
