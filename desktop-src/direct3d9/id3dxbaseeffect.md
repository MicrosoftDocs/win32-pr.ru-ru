---
description: Предоставляет методы для получения и установки параметров эффектов, таких как константы, функции, шейдеры и приемы.
ms.assetid: dd5e107d-2f09-4f6c-ad6c-52cbcbe0cbd1
title: Интерфейс ID3DXBaseEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e72fabf7db8341821885afb160fa73cb0fc9f395
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157163"
---
# <a name="id3dxbaseeffect-interface"></a>Интерфейс ID3DXBaseEffect

Предоставляет методы для получения и установки параметров эффектов, таких как константы, функции, шейдеры и приемы.

## <a name="members"></a>Элементы

Интерфейс **ID3DXBaseEffect** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBaseEffect** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXBaseEffect** содержит следующие методы.



| Метод                                                                                    | Описание                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Заметка**](id3dxbaseeffect--getannotation.md)                                   | Возвращает маркер заметки. <br/>                                                                                                                                                                                     |
| [**жетаннотатионбинаме**](id3dxbaseeffect--getannotationbyname.md)                       | Возвращает маркер заметки путем поиска ее имени.<br/>                                                                                                                                                               |
| [**Bool**](id3dxbaseeffect--getbool.md)                                               | Возвращает логическое значение.<br/>                                                                                                                                                                                                     |
| [**жетбуларрай**](id3dxbaseeffect--getboolarray.md)                                     | Возвращает массив значений типа BOOL.<br/>                                                                                                                                                                                          |
| [**GetDesc**](id3dxbaseeffect--getdesc.md)                                               | Возвращает описание результата.<br/>                                                                                                                                                                                           |
| [**GetFloat**](id3dxbaseeffect--getfloat.md)                                             | Возвращает значение с плавающей запятой.<br/>                                                                                                                                                                                           |
| [**жетфлоатаррай**](id3dxbaseeffect--getfloatarray.md)                                   | Возвращает массив значений с плавающей запятой.<br/>                                                                                                                                                                                |
| [**GetFunction**](id3dxbaseeffect--getfunction.md)                                       | Возвращает маркер функции.<br/>                                                                                                                                                                                         |
| [**жетфунктионбинаме**](id3dxbaseeffect--getfunctionbyname.md)                           | Возвращает маркер функции путем поиска ее имени.<br/>                                                                                                                                                                  |
| [**жетфунктиондеск**](id3dxbaseeffect--getfunctiondesc.md)                               | Возвращает описание функции.<br/>                                                                                                                                                                                           |
| [**GetInt**](id3dxbaseeffect--getint.md)                                                 | Возвращает целое число.<br/>                                                                                                                                                                                                       |
| [**жетинтаррай**](id3dxbaseeffect--getintarray.md)                                       | Возвращает массив целых чисел.<br/>                                                                                                                                                                                             |
| [**Матрица**](id3dxbaseeffect--getmatrix.md)                                           | Возвращает матрицу нонтранспосед.<br/>                                                                                                                                                                                           |
| [**жетматриксаррай**](id3dxbaseeffect--getmatrixarray.md)                                 | Возвращает массив матриц нонтранспосед.<br/>                                                                                                                                                                               |
| [**жетматрикспоинтераррай**](id3dxbaseeffect--getmatrixpointerarray.md)                   | Возвращает массив указателей на нонтранспосед матрицы.<br/>                                                                                                                                                                   |
| [**жетматрикстранспосе**](id3dxbaseeffect--getmatrixtranspose.md)                         | Получает трансобъектную матрицу.<br/>                                                                                                                                                                                              |
| [**жетматрикстранспосеаррай**](id3dxbaseeffect--getmatrixtransposearray.md)               | Возвращает массив переданных матриц.<br/>                                                                                                                                                                                  |
| [**жетматрикстранспосепоинтераррай**](id3dxbaseeffect--getmatrixtransposepointerarray.md) | Возвращает массив указателей на перелагаемые матрицы.<br/>                                                                                                                                                                      |
| [**Параметром PARAMETERIZATION**](id3dxbaseeffect--getparameter.md)                                     | Возвращает маркер параметра верхнего уровня или параметра-члена структуры.<br/>                                                                                                                                              |
| [**жетпараметербинаме**](id3dxbaseeffect--getparameterbyname.md)                         | Возвращает маркер параметра верхнего уровня или параметра члена структуры путем поиска его имени.<br/>                                                                                                                       |
| [**жетпараметербисемантик**](id3dxbaseeffect--getparameterbysemantic.md)                 | Возвращает маркер параметра верхнего уровня или параметра-члена структуры путем поиска его семантики с поиском без учета регистра.<br/>                                                                                    |
| [**жетпараметердеск**](id3dxbaseeffect--getparameterdesc.md)                             | Возвращает описание параметра или заметки.<br/>                                                                                                                                                                            |
| [**жетпараметерелемент**](id3dxbaseeffect--getparameterelement.md)                       | Получение маркера параметра элемента массива.<br/>                                                                                                                                                                          |
| [**Проход**](id3dxbaseeffect--getpass.md)                                               | Возвращает маркер прохода.<br/>                                                                                                                                                                                             |
| [**жетпассбинаме**](id3dxbaseeffect--getpassbyname.md)                                   | Возвращает маркер прохода путем поиска его имени.<br/>                                                                                                                                                                      |
| [**жетпассдеск**](id3dxbaseeffect--getpassdesc.md)                                       | Возвращает описание этапа.<br/>                                                                                                                                                                                               |
| [**жетпикселшадер**](id3dxbaseeffect--getpixelshader.md)                                 | Возвращает шейдер пикселей.<br/>                                                                                                                                                                                                   |
| [**GetString**](id3dxbaseeffect--getstring.md)                                           | Возвращает строку.<br/>                                                                                                                                                                                                         |
| [**Метод "методом"**](id3dxbaseeffect--gettechnique.md)                                     | Возвращает маркер метода.<br/>                                                                                                                                                                                        |
| [**жеттечникуебинаме**](id3dxbaseeffect--gettechniquebyname.md)                         | Возвращает маркер метода путем поиска его имени.<br/>                                                                                                                                                                 |
| [**жеттечникуедеск**](id3dxbaseeffect--gettechniquedesc.md)                             | Возвращает описание метода.<br/>                                                                                                                                                                                          |
| [**Текстурирование**](id3dxbaseeffect--gettexture.md)                                         | Возвращает текстуру.<br/>                                                                                                                                                                                                        |
| [**GetValue**](id3dxbaseeffect--getvalue.md)                                             | Получение значения произвольного параметра или заметки, включая простые типы, структуры, массивы, строки, шейдеры и текстуры. Этот метод можно использовать вместо почти всех вызовов Жеткскскс в **ID3DXBaseEffect**.<br/> |
| [**Вектор**](id3dxbaseeffect--getvector.md)                                           | Возвращает вектор.<br/>                                                                                                                                                                                                         |
| [**жетвектораррай**](id3dxbaseeffect--getvectorarray.md)                                 | Возвращает массив векторов.<br/>                                                                                                                                                                                              |
| [**жетвертексшадер**](id3dxbaseeffect--getvertexshader.md)                               | Возвращает шейдер вершин.<br/>                                                                                                                                                                                                  |
| [**сетаррайранже**](id3dxbaseeffect--setarrayrange.md)                                   | Задайте диапазон массива для передачи на устройство.<br/>                                                                                                                                                                       |
| [**сетбул**](id3dxbaseeffect--setbool.md)                                               | Задает логическое значение.<br/>                                                                                                                                                                                                     |
| [**сетбуларрай**](id3dxbaseeffect--setboolarray.md)                                     | Задает массив логических значений.<br/>                                                                                                                                                                                       |
| [**SetFloat**](id3dxbaseeffect--setfloat.md)                                             | Устанавливает значение с плавающей запятой.<br/>                                                                                                                                                                                           |
| [**сетфлоатаррай**](id3dxbaseeffect--setfloatarray.md)                                   | Задает массив значений с плавающей запятой.<br/>                                                                                                                                                                                |
| [**SetInt**](id3dxbaseeffect--setint.md)                                                 | Задает целое число.<br/>                                                                                                                                                                                                       |
| [**сетинтаррай**](id3dxbaseeffect--setintarray.md)                                       | Задает массив целых чисел.<br/>                                                                                                                                                                                             |
| [**сетматрикс**](id3dxbaseeffect--setmatrix.md)                                           | Задает трансобъектную матрицу.<br/>                                                                                                                                                                                          |
| [**сетматриксаррай**](id3dxbaseeffect--setmatrixarray.md)                                 | Задает массив матриц нонтранспосед.<br/>                                                                                                                                                                               |
| [**сетматрикспоинтераррай**](id3dxbaseeffect--setmatrixpointerarray.md)                   | Задает массив указателей для нонтранспосед матриц.<br/>                                                                                                                                                                   |
| [**сетматрикстранспосе**](id3dxbaseeffect--setmatrixtranspose.md)                         | Задает трансобъектную матрицу.<br/>                                                                                                                                                                                              |
| [**сетматрикстранспосеаррай**](id3dxbaseeffect--setmatrixtransposearray.md)               | Задает массив переданных матриц.<br/>                                                                                                                                                                                  |
| [**сетматрикстранспосепоинтераррай**](id3dxbaseeffect--setmatrixtransposepointerarray.md) | Задает массив указателей на перекладываемые матрицы.<br/>                                                                                                                                                                      |
| [**SetString**](id3dxbaseeffect--setstring.md)                                           | Задает строку.<br/>                                                                                                                                                                                                         |
| [**сеттекстуре**](id3dxbaseeffect--settexture.md)                                         | Задает текстуру.<br/>                                                                                                                                                                                                        |
| [**SetValue**](id3dxbaseeffect--setvalue.md)                                             | Задайте значение произвольного параметра или заметки, включая простые типы, структуры, массивы, строки, шейдеры и текстуры. <br/>                                                                                        |
| [**сетвектор**](id3dxbaseeffect--setvector.md)                                           | Задает вектор.<br/>                                                                                                                                                                                                         |
| [**сетвектораррай**](id3dxbaseeffect--setvectorarray.md)                                 | Задает массив векторов.<br/>                                                                                                                                                                                              |



 

## <a name="remarks"></a>Комментарии

Тип LPD3DXBASEEFFECT определяется как указатель на этот интерфейс.


```
typedef interface ID3DXBaseEffect ID3DXBaseEffect;
typedef interface ID3DXBaseEffect *LPD3DXBASEEFFECT;
        
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы эффектов](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> </dl>

 

 
