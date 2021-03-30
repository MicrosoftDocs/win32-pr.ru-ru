---
description: Возвращает значение фиксированной вершины функции.
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
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354070"
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

## <a name="remarks"></a>Комментарии

Этот метод может возвращать значение 0, если формат вершин не может быть напрямую сопоставлен с кодом ФВФ. Это произойдет для сетки, созданной из объявления вершины, которая не имеет тех же порядка и элементов, которые поддерживаются кодами ФВФ.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: Сетфвф**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
