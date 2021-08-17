---
description: Прототип функции, используемый D3DXComputeIMTFromSignal для описания определяемого пользователем сигнала в u, v пространстве входной сетки. Функция вычисляет процедурный сигнал Усигналдименсион измерения в указанной координате u, v.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e4f6ffaa4c844e755d489aae52dd13b8390da1145734d50f5865bbe0e3cfc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728511"
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

## <a name="remarks"></a>Remarks

при объявлении функции обратного вызова необходимо указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) . В противном случае могут возникать переполняется стек.



| Требование               | Значение            |
|----------------|-------------|
| Заголовок         | d3dx9mesh. h |
| Библиотека импорта | d3dx9. lib   |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции обратного вызова](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
