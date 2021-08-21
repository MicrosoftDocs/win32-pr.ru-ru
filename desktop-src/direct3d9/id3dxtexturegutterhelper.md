---
description: Интерфейс ID3DXTextureGutterHelper используется для создания областей переплета и управления ими в текстуре. Области переплета разделяют текстуры и позволяют билинейной интерполяцию, чтобы избежать артефактов отрисовки на границах текстур.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Интерфейс ID3DXTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8e72814c036e297111a4a2f3825574a2a088310cb17d484902c59875958e7e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118093958"
---
# <a name="id3dxtexturegutterhelper-interface"></a>Интерфейс ID3DXTextureGutterHelper

Интерфейс ID3DXTextureGutterHelper используется для создания областей переплета и управления ими в текстуре. Области переплета разделяют текстуры и позволяют билинейной интерполяцию, чтобы избежать артефактов отрисовки на границах текстур.

Получение... методы предоставляют доступ к структурам данных, используемым функцией Apply... метод.

## <a name="members"></a>Элементы

Интерфейс **ID3DXTextureGutterHelper** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXTextureGutterHelper** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXTextureGutterHelper** содержит следующие методы.



| Метод                                                                   | Описание                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**апплигуттерсфлоат**](id3dxtexturegutterhelper--applyguttersfloat.md) | Применяет переплет к буферу текстуры с плавающей запятой.<br/>                                                  |
| [**апплигуттерспрт**](id3dxtexturegutterhelper--applyguttersprt.md)     | Применяет переплет к объекту [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.<br/>               |
| [**апплигуттерстекс**](id3dxtexturegutterhelper--applygutterstex.md)     | Применяет переплет к объекту текстуры [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/>        |
| [**жетбаримап**](id3dxtexturegutterhelper--getbarymap.md)               | Получает координаты шаг текселя барицентрик.<br/>                                                    |
| [**жетфацемап**](id3dxtexturegutterhelper--getfacemap.md)               | Извлекает индекс грани сетки, к которой принадлежит каждый шаг текселя.<br/>                           |
| [**жетгуттермап**](id3dxtexturegutterhelper--getguttermap.md)           | Получает значение класса шаг текселя, которое указывает класс шаг текселя в соответствии с расположением каждого шаг текселя.<br/> |
| [**Высота**](id3dxtexturegutterhelper--getheight.md)                 | Получает высоту текстуры в пикселях.<br/>                                             |
| [**жеттекселмап**](id3dxtexturegutterhelper--gettexelmap.md)             | Извлекает координаты текстуры (u, v) каждого шаг текселя.<br/>                                     |
| [**Полуширинные**](id3dxtexturegutterhelper--getwidth.md)                   | Получает ширину текстуры в пикселях.<br/>                                              |
| [**ресамплетекс**](id3dxtexturegutterhelper--resampletex.md)             | Ресамплинг текстуры в гуттерхелпер параметризации.<br/>                              |
| [**сетбаримап**](id3dxtexturegutterhelper--setbarymap.md)               | Задает координаты шаг текселя барицентрик.<br/>                                                         |
| [**сетфацемап**](id3dxtexturegutterhelper--setfacemap.md)               | Задает индекс грани сетки, к которой принадлежит каждый шаг текселя.<br/>                                |
| [**сетгуттермап**](id3dxtexturegutterhelper--setguttermap.md)           | Задает значение класса шаг текселя, указывающее класс шаг текселя в соответствии с расположением каждого шаг текселя.<br/>     |
| [**сеттекселмап**](id3dxtexturegutterhelper--settexelmap.md)             | Задает координаты текстуры (u, v) каждого шаг текселя.<br/>                                          |



 

## <a name="remarks"></a>Remarks

> [!Note]  
> При использовании с предварительно вычисленным радианценым переносом (PRT) Этот интерфейс требует уникальной параметризации модели. Каждый шаг текселя должен соответствовать одной точке на поверхности модели и наоборот. Если модель включает несколько текстур, ее необходимо разделить на отдельные части, каждая из которых содержит один вспомогательный объект для каждой текстуры.

 

Этот интерфейс можно использовать для создания карты в пространстве текстуры, в которой каждый шаг текселя находится в одном из четырех классов.



| Класс шаг текселя | Расположение шаг текселя                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Недопустимая точка; шаг текселя не будет использоваться.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Внутри треугольника.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Внутренняя часть.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Внутреннее внутреннее поле; шаг текселя будет оцениваться как полный пример в методах [**ID3DXTextureGutterHelper:: апплигуттерсфлоат**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: апплигуттерстекс**](id3dxtexturegutterhelper--applygutterstex.md)или [**ID3DXTextureGutterHelper:: апплигуттерспрт**](id3dxtexturegutterhelper--applyguttersprt.md) . |



 

Для классов 1 и 2 шаг текселя хранится с лицевой стороны, а также с координатами барицентрик первых двух вершин этого лица. Вершины переплета назначаются ближайшей границе в пространстве текстуры.

Отсутствует класс шаг текселя 3.

Интерфейс **ID3DXTextureGutterHelper** получается путем вызова функции [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) .

Тип LPD3DXTEXTUREGUTTERHELPER определяется как указатель на интерфейс **ID3DXTextureGutterHelper** .


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
