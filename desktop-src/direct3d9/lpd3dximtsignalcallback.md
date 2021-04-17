---
description: Прототип функции, используемый D3DXComputeIMTFromSignal для описания определяемого пользователем сигнала в u, v пространстве входной сетки. Функция вычисляет процедурный сигнал Усигналдименсион измерения в указанной координате u, v.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710561"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Прототип функции, используемый [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) для описания определяемого пользователем сигнала в u, v пространстве входной сетки. Функция вычисляет процедурный сигнал Усигналдименсион измерения в указанной координате u, v.

## <a name="syntax"></a>Синтаксис


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a>Параметры

\[в \] UV — указатель на вектор, содержащий координату текстуры вершины.

\[в \] упримитивеид — индекс входного треугольника в сетке, для которого должен быть вычислен сигнал.

\[в \] усигналдименсион — количество элементов типа float для хранения в массиве данных сигнала (пфсигналаут).

\[в \] пусердата — указатель Пусердата, переданный в [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).

\[out \] пфсигналаут — массив float, который содержит данные сигнала.

## <a name="return-value"></a>Возвращаемое значение

Эта функция должна быть реализована для возврата значения S \_ ОК.

## <a name="remarks"></a>Комментарии

Не забудьте указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) при объявлении функции обратного вызова. В противном случае могут возникать переполняется стек.



|                |             |
|----------------|-------------|
| Header         | d3dx9mesh. h |
| Библиотека импорта | d3dx9. lib   |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции обратного вызова](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
