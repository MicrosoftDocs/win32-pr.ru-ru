---
description: Возвращает размер вершины для гибкого формата вершин (ФВФ).
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: Функция D3DXGetFVFVertexSize (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f00faa489481faf436a30fe6e6313429d446cd8000173131d823442e960b5a08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119214"
---
# <a name="d3dxgetfvfvertexsize-function"></a>Функция D3DXGetFVFVertexSize

Возвращает размер вершины для гибкого формата вершин (ФВФ).

## <a name="syntax"></a>Синтаксис


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Фвф* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

ФВФ для запроса. Сочетание [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Размер вершины ФВФ в байтах.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
