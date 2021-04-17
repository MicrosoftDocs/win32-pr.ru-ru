---
description: Интерфейс ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Интерфейс ID3DXTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664966"
---
# <a name="id3dxtextureshader-interface"></a>Интерфейс ID3DXTextureShader

Интерфейс ID3DXTextureShader.

## <a name="members"></a>Элементы

Интерфейс **ID3DXTextureShader** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXTextureShader** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXTextureShader** содержит следующие методы.



| Метод                                                                                       | Описание                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**Константа**](id3dxtextureshader--getconstant.md)                                       | Возвращает константу путем поиска своего индекса.<br/>                         |
| [**жетконстантбуффер**](id3dxtextureshader--getconstantbuffer.md)                           | Возвращает указатель на таблицу констант.<br/>                             |
| [**жетконстантбинаме**](id3dxtextureshader--getconstantbyname.md)                           | Возвращает константу путем поиска ее имени.<br/>                          |
| [**жетконстантдеск**](id3dxtextureshader--getconstantdesc.md)                               | Возвращает указатель на массив констант в таблице констант.<br/>  |
| [**жетконстантелемент**](id3dxtextureshader--getconstantelement.md)                         | Получить константу из таблицы констант.<br/>                          |
| [**GetDesc**](id3dxtextureshader--getdesc.md)                                               | Возвращает описание таблицы констант.<br/>                        |
| [**GetFunction**](id3dxtextureshader--getfunction.md)                                       | Возвращает указатель на поток функции DWORD.<br/>                     |
| [**сетбул**](id3dxtextureshader--setbool.md)                                               | Задает логическое значение.<br/>                                               |
| [**сетбуларрай**](id3dxtextureshader--setboolarray.md)                                     | Задает массив значений типа BOOL.<br/>                                    |
| [**SetDefaults**](id3dxtextureshader--setdefaults.md)                                       | Устанавливает константы в значения по умолчанию, объявленные в шейдере.<br/> |
| [**SetFloat**](id3dxtextureshader--setfloat.md)                                             | Задает число с плавающей запятой.<br/>                                    |
| [**сетфлоатаррай**](id3dxtextureshader--setfloatarray.md)                                   | Задает массив чисел с плавающей запятой.<br/>                         |
| [**SetInt**](id3dxtextureshader--setint.md)                                                 | Задает целочисленное значение.<br/>                                           |
| [**сетинтаррай**](id3dxtextureshader--setintarray.md)                                       | Задает массив целых чисел.<br/>                                       |
| [**сетматрикс**](id3dxtextureshader--setmatrix.md)                                           | Задает трансобъектную матрицу.<br/>                                    |
| [**сетматриксаррай**](id3dxtextureshader--setmatrixarray.md)                                 | Задает массив нестандартных матриц.<br/>                        |
| [**сетматрикспоинтераррай**](id3dxtextureshader--setmatrixpointerarray.md)                   | Задает массив указателей на нестандартные матрицы.<br/>            |
| [**сетматрикстранспосе**](id3dxtextureshader--setmatrixtranspose.md)                         | Задает трансобъектную матрицу.<br/>                                        |
| [**сетматрикстранспосеаррай**](id3dxtextureshader--setmatrixtransposearray.md)               | Задает массив переданных матриц.<br/>                            |
| [**сетматрикстранспосепоинтераррай**](id3dxtextureshader--setmatrixtransposepointerarray.md) | Задает массив указателей на перекладываемые матрицы.<br/>                |
| [**SetValue**](id3dxtextureshader--setvalue.md)                                             | Задает таблицу констант с данными в буфере.<br/>             |
| [**сетвектор**](id3dxtextureshader--setvector.md)                                           | Задает вектор 4D.<br/>                                                |
| [**сетвектораррай**](id3dxtextureshader--setvectorarray.md)                                 | Задает массив векторов 4D.<br/>                                     |



 

## <a name="remarks"></a>Комментарии

Интерфейс **ID3DXTextureShader** получается путем вызова функции [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) .

Интерфейс **ID3DXTextureShader** , как и все COM-интерфейсы, наследует интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

Тип LPD3DXTEXTURESHADER определяется как указатель на интерфейс **ID3DXTextureShader** .


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
