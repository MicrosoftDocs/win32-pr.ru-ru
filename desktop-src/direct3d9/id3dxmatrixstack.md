---
description: Интерфейс ID3DXMATRIXStack. приложения используют методы интерфейса ID3DXMATRIXStack для управления стеком матрицы.
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Интерфейс ID3DXMATRIXStack (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62681c468fa7e78e6fd08c458798d98b467b992e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093322"
---
# <a name="id3dxmatrixstack-interface"></a>Интерфейс ID3DXMATRIXStack

Приложения используют методы интерфейса ID3DXMATRIXStack для управления стеком матрицы.

## <a name="members"></a>Элементы

Интерфейс **ID3DXMATRIXStack** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXMATRIXStack** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXMATRIXStack** содержит следующие методы.



| Метод                                                                       | Описание                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack--gettop.md)                                   | Извлекает текущую матрицу в верхней части стека.<br/>                                                                           |
| [**лоадидентити**](id3dxmatrixstack--loadidentity.md)                       | Загружает удостоверение в текущую матрицу.<br/>                                                                                           |
| [**лоадматрикс**](id3dxmatrixstack--loadmatrix.md)                           | Загружает заданную матрицу в текущую матрицу.<br/>                                                                                 |
| [**мултматрикс**](id3dxmatrixstack--multmatrix.md)                           | Определяет произведение текущей матрицы и заданную матрицу.<br/>                                                              |
| [**мултматрикслокал**](id3dxmatrixstack--multmatrixlocal.md)                 | Определяет произведение заданной матрицы и текущей матрицы.<br/>                                                              |
| [**Рор**](id3dxmatrixstack--pop.md)                                         | Удаляет текущую матрицу из верхней части стека.<br/>                                                                           |
| [**push**](id3dxmatrixstack--push.md)                                       | Добавляет матрицу в стек.<br/>                                                                                                     |
| [**ротатеаксис**](id3dxmatrixstack--rotateaxis.md)                           | Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.<br/>                                                          |
| [**ротатеаксислокал**](id3dxmatrixstack--rotateaxislocal.md)                 | Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.<br/>                                             |
| [**ротатэйавпитчролл**](id3dxmatrixstack--rotateyawpitchroll.md)           | Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.<br/>                                                          |
| [**ротатэйавпитчролллокал**](id3dxmatrixstack--rotateyawpitchrolllocal.md) | Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.<br/>                                             |
| [**Масштабирование**](id3dxmatrixstack--scale.md)                                     | Масштабировать текущую матрицу относительно источника координат мира.<br/>                                                                     |
| [**скалелокал**](id3dxmatrixstack--scalelocal.md)                           | Масштабировать текущую матрицу относительно источника объекта.<br/>                                                                               |
| [**Перевести**](id3dxmatrixstack--translate.md)                             | Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).<br/> |
| [**транслателокал**](id3dxmatrixstack--translatelocal.md)                   | Определяет продукт вычисленной матрицы перевода, определяемый заданными факторами (x, y и z) и текущей матрицей.<br/> |



 

## <a name="remarks"></a>Remarks

Интерфейс **ID3DXMATRIXStack** получается путем вызова функции [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) .

Тип LPD3DXMATRIXSTACK определяется как указатель на интерфейс **ID3DXMATRIXStack** .


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
