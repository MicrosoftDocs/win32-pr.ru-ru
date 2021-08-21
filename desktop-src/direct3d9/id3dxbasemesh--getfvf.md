---
description: 'Метод ID3DXBaseMesh:: Жетфвф — получает значение фиксированной вершины функции.'
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'Метод ID3DXBaseMesh:: Жетфвф (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 814f14645e5e7f0aa883f04e689f0774441482b86223bf485fa1fc8a395618c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987624"
---
# <a name="id3dxbasemeshgetfvf-method"></a>Метод ID3DXBaseMesh:: Жетфвф

Возвращает значение фиксированной вершины функции.

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Возвращает коды гибких форматов вершин (ФВФ).

## <a name="remarks"></a>Remarks

Этот метод может возвращать значение 0, если формат вершин не может быть напрямую сопоставлен с кодом ФВФ. Это произойдет для сетки, созданной из объявления вершины, которая не имеет тех же порядка и элементов, которые поддерживаются кодами ФВФ.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
