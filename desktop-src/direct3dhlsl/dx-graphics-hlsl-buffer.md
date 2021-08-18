---
title: Тип буфера
description: Чтобы объявить переменную буфера, используйте следующий синтаксис.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Тип буфера HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78d0b452a387ed1d4bf750062963996d0248fa249954a99be581118560866123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120348"
---
# <a name="buffer-type"></a>Тип буфера

Чтобы объявить переменную буфера, используйте следующий синтаксис.



| Buffer< >  *имя* типа; |
|------------------------------|



 

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Двойной**
</dt> <dd>

Обязательное ключевое слово.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Тип*
</dt> <dd>

Один из типов [скалярных](dx-graphics-hlsl-scalar.md), [векторных](dx-graphics-hlsl-vector.md)и некоторых [матричных](dx-graphics-hlsl-matrix.md) HLSL. Можно объявить переменную буфера с матрицей, если она умещается в 4 32-разрядном количестве. Итак, можно написать `Buffer<float2x2>` . Но `Buffer<float4x4>` слишком большой, и компилятор выдаст ошибку.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*
</dt> <dd>

Строка ASCII, однозначно определяющая имя переменной.

</dd> </dl>

## <a name="example"></a>Пример

Ниже приведен пример объявления буфера из файла Пипесгс. FX в [примере пипесгс](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).


```
Buffer<float4> g_Buffer;
```



Данные считываются из буфера с помощью перегруженной версии встроенной функции [**Load**](dx-graphics-hlsl-to-load.md) HLSL, которая принимает один входной параметр (целочисленный индекс). Доступ к буферу осуществляется как к массиву элементов. Поэтому в этом примере считывается второй элемент.


```
float4 bufferData = g_Buffer.Load( 1 );
```



Используйте [этап потокового вывода](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) для вывода данных в буфер.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Типы данных (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 