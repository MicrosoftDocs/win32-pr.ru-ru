---
description: Задает значение класса шаг текселя, указывающее класс шаг текселя в соответствии с расположением каждого шаг текселя.
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'Метод ID3DXTextureGutterHelper:: Сетгуттермап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703941"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a>Метод ID3DXTextureGutterHelper:: Сетгуттермап

Задает значение класса шаг текселя, указывающее класс шаг текселя в соответствии с расположением каждого шаг текселя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуттердата* \[ окне\]
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
