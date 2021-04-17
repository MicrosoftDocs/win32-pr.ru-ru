---
description: Возвращает количество вершин в сетке.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'Метод ID3DX10Mesh:: Жетвертекскаунт (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703891"
---
# <a name="id3dx10meshgetvertexcount-method"></a>Метод ID3DX10Mesh:: Жетвертекскаунт

Возвращает количество вершин в сетке. Сетка может содержать несколько буферов вершин (т. е. один буфер вершин может содержать все данные о положении, другой может состоять из всех данных о координатах текстуры и т. д.), однако каждый буфер вершин будет содержать одинаковое число элементов.

## <a name="syntax"></a>Синтаксис


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число вершин в сетке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
