---
description: LPD3DXFILL2D — тип функции, используемый функциями заливки текстур.
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8046c324511f2b308243d62fec1b6508a1d483ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087972"
---
# <a name="lpd3dxfill2d"></a>LPD3DXFILL2D

Тип функции, используемый функциями заливки текстур.

## <a name="syntax"></a>Синтаксис


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a>Параметры

Тоска — указатель на вектор, который функция использует для возврата результата. X, Y, Z и W будут сопоставлены с R, G, B и A соответственно.

Птекскурд — указатель на вектор, содержащий координаты шаг текселя, который в настоящее время вычисляется. Компоненты координат текстуры для текстуры и текстуры тома находятся в диапазоне от 0 до 1. Компоненты координат текстуры для текстур Куба находятся в диапазоне от-1 до 1.

Птекселсизе — указатель на вектор, содержащий измерения текущего шаг текселя.

pData — указатель на данные пользователя.

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Не забудьте указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) при объявлении функции обратного вызова. В противном случае могут возникать переполняется стек.



|                          |            |
|--------------------------|------------|
| Header                   | d3dx9tex. h |
| Библиотека импорта           | d3dx9. lib  |
| Минимальная операционная система | Windows 98 |



 

## <a name="related-topics"></a>Связанные разделы

<dl> <dt>

[Функции обратного вызова](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL3D](lpd3dxfill3d.md)
</dt> </dl>

 

 
