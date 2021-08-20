---
description: Создает объявление вершины вывода из объявления ввода. Объявление вывода предназначено для использования функциями тесселяции сетки.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: Функция D3DXGenerateOutputDecl (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1f74440ce7bbd72f62aa35de242ea48f615a4ed02d82c5782f7f0eaff1d5bc25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096049"
---
# <a name="d3dxgenerateoutputdecl-function"></a>Функция D3DXGenerateOutputDecl

Создает объявление вершины вывода из объявления ввода. Объявление вывода предназначено для использования функциями тесселяции сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паутпут* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***

Указатель на объявление выходной вершины. См. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*пинпут* \[ окне\]
</dt> <dd>

Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Указатель на объявление входного вершины. См. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается с ошибкой, возвращаемое значение может быть одним из следующих значений: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




