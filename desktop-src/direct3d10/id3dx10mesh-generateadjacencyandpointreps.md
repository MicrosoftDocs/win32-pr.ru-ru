---
description: 'Метод ID3DX10Mesh:: Женератеаджаценциандпоинтрепс — создает список границ сетки, а также список лиц, совместно использующих каждое ребро.'
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'Метод ID3DX10Mesh:: Женератеаджаценциандпоинтрепс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e496f96f36805d411c71e9aba1e2560b0dcbe3c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083982"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a>Метод ID3DX10Mesh:: Женератеаджаценциандпоинтрепс

Создание списка границ сетки, а также списка лиц, совместно использующих каждое ребро.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Эпсилон* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Указывает, что вершины, отличающиеся от позиций меньше Эпсилон, должны рассматриваться как коинЦидент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

После того как приложение создаст сведения о смежности для сетки, данные сетки можно оптимизировать для повышения производительности рисования.

Порядок записей в смежном буфере определяется порядком индексов вершин в буфере индекса. Смежный треугольник 0 всегда соответствует границе между индексами углов 0 и 1. Смежный треугольник 1 всегда соответствует границе между индексами углов 1 и 2, а смежный треугольник 2 соответствует границе между индексами углов 2 и 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
