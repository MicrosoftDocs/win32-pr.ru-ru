---
description: Определяет метод объявления вершины, который представляет собой предопределенную операцию, выполняемую тесселяцией (или любую процедурную геометрию для данных вершин во время тесселяции).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Перечисление D3DDECLMETHOD (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354383"
---
# <a name="d3ddeclmethod-enumeration"></a>Перечисление D3DDECLMETHOD

Определяет метод объявления вершины, который представляет собой предопределенную операцию, выполняемую тесселяцией (или любую процедурную геометрию для данных вершин во время тесселяции).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ по умолчанию**
</dt> <dd>

Значение по умолчанию. Тесселяция копирует данные вершин (данные сплайна для исправлений) без дополнительных вычислений. При использовании тесселяции этот элемент интерполируются. В противном случае данные вершин копируются во входной регистр. Тип входных и выходных данных может иметь любое значение, но всегда один и тот же тип.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ партиалу**
</dt> <dd>

Выполняет вычисление тангенса в точке с обновлением прямоугольника или треугольника в направлении U. Тип входных данных может быть одним из следующих:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Тип выходных данных всегда D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ партиалв**
</dt> <dd>

Выполняет вычисление тангенса в точке с обновлением прямоугольника или треугольника в направлении V. Тип входных данных может быть одним из следующих:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Тип выходных данных всегда D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ кроссув**
</dt> <dd>

Выполняет вычисление нормали в точке на исправлении прямоугольника или треугольника, выполнив перекрестное произведение двух тангенсов. Тип входных данных может быть одним из следующих:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Тип выходных данных всегда D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ UV**
</dt> <dd>

Скопируйте значения U, V в точку с обновлением прямоугольника или треугольника. В результате получается 2D с плавающей запятой. Для типа входных данных должно быть задано значение D3DDECLTYPE не \_ используется. Тип выходных данных всегда D3DDECLTYPE \_ FLOAT2. Входной поток и смещение также не являются неиспользуемыми (но должны иметь значение 0).

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD \_ Поиск**
</dt> <dd>

Найдите карту смещения. Тип входных данных может быть одним из следующих:

-   D3DDECLTYPE \_ FLOAT2
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4

Для поиска текстурных карт используются только компоненты x и y. Тип выходных данных всегда D3DDECLTYPE \_ FLOAT1. Устройство должно поддерживать сопоставление смещений. Дополнительные сведения о сопоставлении замещения см. в разделе [сопоставление смещения (Direct3D 9)](displacement-mapping.md). Эта константа поддерживается только программируемым конвейером для N-патчных данных, если N — исправления включены.

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ лукуппресамплед**
</dt> <dd>

Поиск предустановленной схемы смещения. Для входного типа необходимо задать значение D3DDECLTYPE не \_ используется; индекс потока и смещение потока должны быть установлены в значение 0. Тип выходных данных для этой операции всегда D3DDECLTYPE \_ FLOAT1. Устройство должно поддерживать сопоставление смещений. Дополнительные сведения о сопоставлении замещения см. в разделе [сопоставление смещения (Direct3D 9)](displacement-mapping.md). Эта константа поддерживается только программируемым конвейером для N-патчных данных, если N — исправления включены. Этот метод можно использовать только с примером D3DDECLUSAGE \_ .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Тесселяция просматривает метод, чтобы определить, какие данные следует вычислить из данных вершин во время тесселяции. В данных сетки должно использоваться значение по умолчанию. Исправления могут использовать любой из других реализованных типов.

Данные вершин объявляются с помощью массива структур [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Каждый элемент массива содержит метод объявления вершины.

Помимо использования D3DDECLMETHOD \_ по умолчанию, обычная сетка может использовать методы D3DDECLMETHOD \_ Lookup и D3DDECLMETHOD \_ Лукуппресамплед, если N-патчи включены.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




