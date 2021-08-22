---
description: 'Метод ID3DXSkinInfo:: Жетфвф — получает значение фиксированной вершины функции.'
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'Метод ID3DXSkinInfo:: Жетфвф (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e7419e116cddd20aebfc61d7813ea2bd403ce04b897aa821f03a2ad48eae6965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492294"
---
# <a name="id3dxskininfogetfvf-method"></a>Метод ID3DXSkinInfo:: Жетфвф

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: Сетфвф**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
