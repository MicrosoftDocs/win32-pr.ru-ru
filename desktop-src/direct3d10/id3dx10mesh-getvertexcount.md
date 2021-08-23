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
ms.openlocfilehash: 00fd0cd84aedb32e2da567a92ffc421f41394a991872f9216b06a4f28f895183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566894"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
