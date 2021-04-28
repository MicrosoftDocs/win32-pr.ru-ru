---
description: LPD3DXFILL3D — тип функции, используемый функциями заливки текстур.
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c711459cffa3430b31ba7c91d77cc9519e6a43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114312"
---
# <a name="lpd3dxfill3d"></a>LPD3DXFILL3D

Тип функции, используемый функциями заливки текстур.

## <a name="syntax"></a>Синтаксис


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
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

[LPD3DXFILL2D](lpd3dxfill2d.md)
</dt> </dl>

 

 
