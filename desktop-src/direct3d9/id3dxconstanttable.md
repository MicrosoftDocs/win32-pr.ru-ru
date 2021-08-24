---
description: Интерфейс ID3DXConstantTable используется для доступа к таблице констант. Эта таблица содержит переменные, используемые в высокоуровневой шейдере и эффектах языка.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Интерфейс ID3DXConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ead9e594e79daf8bd43bf4125b857030482028f7128c8063196413d52c9a8b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675484"
---
# <a name="id3dxconstanttable-interface"></a>Интерфейс ID3DXConstantTable

Интерфейс ID3DXConstantTable используется для доступа к таблице констант. Эта таблица содержит переменные, используемые в высокоуровневой шейдере и эффектах языка.

## <a name="members"></a>Элементы

Интерфейс **ID3DXConstantTable** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXConstantTable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXConstantTable** содержит следующие методы.



| Метод                                                                                       | Описание                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**жетбуфферпоинтер**](id3dxconstanttable--getbufferpointer.md)                             | Возвращает указатель на буфер, содержащий таблицу констант.<br/>                                                          |
| [**жетбуфферсизе**](id3dxconstanttable--getbuffersize.md)                                   | Возвращает размер буфера таблицы констант.<br/>                                                                             |
| [**Константа**](id3dxconstanttable--getconstant.md)                                       | Возвращает константу путем поиска своего индекса.<br/>                                                                                |
| [**жетконстантбинаме**](id3dxconstanttable--getconstantbyname.md)                           | Возвращает константу путем поиска ее имени.<br/>                                                                                 |
| [**жетконстантдеск**](id3dxconstanttable--getconstantdesc.md)                               | Возвращает указатель на массив константных описаний в таблице констант.<br/>                                              |
| [**жетконстантелемент**](id3dxconstanttable--getconstantelement.md)                         | Возвращает константу из массива констант. Массив состоит из элементов.<br/>                                            |
| [**GetDesc**](id3dxconstanttable--getdesc.md)                                               | Возвращает описание таблицы констант.<br/>                                                                               |
| [**жетсамплериндекс**](id3dxconstanttable--getsamplerindex.md)                               | Возвращает индекс образца.<br/>                                                                                              |
| [**сетбул**](id3dxconstanttable--setbool.md)                                               | Задает логическое значение.<br/>                                                                                                   |
| [**сетбуларрай**](id3dxconstanttable--setboolarray.md)                                     | Задает массив логических значений.<br/>                                                                                        |
| [**SetDefaults**](id3dxconstanttable--setdefaults.md)                                       | Устанавливает константы в значения по умолчанию. Значения по умолчанию объявляются в объявлениях переменных в шейдере.<br/> |
| [**SetFloat**](id3dxconstanttable--setfloat.md)                                             | Задает число с плавающей запятой.<br/>                                                                                           |
| [**сетфлоатаррай**](id3dxconstanttable--setfloatarray.md)                                   | Задает массив чисел с плавающей запятой.<br/>                                                                                |
| [**SetInt**](id3dxconstanttable--setint.md)                                                 | Задает целочисленное значение.<br/>                                                                                                  |
| [**сетинтаррай**](id3dxconstanttable--setintarray.md)                                       | Задает массив целых чисел.<br/>                                                                                              |
| [**сетматрикс**](id3dxconstanttable--setmatrix.md)                                           | Задает матрицу нонтранспосед.<br/>                                                                                            |
| [**сетматриксаррай**](id3dxconstanttable--setmatrixarray.md)                                 | Задает массив матриц нонтранспосед.<br/>                                                                                |
| [**сетматрикспоинтераррай**](id3dxconstanttable--setmatrixpointerarray.md)                   | Задает массив указателей для нонтранспосед матриц.<br/>                                                                    |
| [**сетматрикстранспосе**](id3dxconstanttable--setmatrixtranspose.md)                         | Задает трансобъектную матрицу.<br/>                                                                                               |
| [**сетматрикстранспосеаррай**](id3dxconstanttable--setmatrixtransposearray.md)               | Задает массив переданных матриц.<br/>                                                                                   |
| [**сетматрикстранспосепоинтераррай**](id3dxconstanttable--setmatrixtransposepointerarray.md) | Задает массив указателей на перекладываемые матрицы.<br/>                                                                       |
| [**SetValue**](id3dxconstanttable--setvalue.md)                                             | Устанавливает содержимое буфера в таблицу констант.<br/>                                                                  |
| [**сетвектор**](id3dxconstanttable--setvector.md)                                           | Задает вектор 4D.<br/>                                                                                                       |
| [**сетвектораррай**](id3dxconstanttable--setvectorarray.md)                                 | Задает массив векторов 4D.<br/>                                                                                            |



 

## <a name="remarks"></a>Remarks

Тип LPD3DXCONSTANTTABLE определяется как указатель на интерфейс **ID3DXConstantTable** .


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
