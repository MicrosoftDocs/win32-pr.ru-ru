---
description: Находит дочерний фрейм корневого фрейма.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: Функция D3DXFrameFind (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f62cacabbf020d1fe9ff9e83c47acc6c58e52c4ab6be031586bda365745f595
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027664"
---
# <a name="d3dxframefind-function"></a>Функция D3DXFrameFind

Находит дочерний фрейм корневого фрейма.

## <a name="syntax"></a>Синтаксис


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфрамерут* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXFRAME**](d3dxframe.md) \***

Указатель на корневой фрейм. См. [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*Имя* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Имя дочернего фрейма, который нужно найти.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**

Возвращает дочерний фрейм, если он найден, или **значение NULL** в противном случае. См. [**D3DXFRAME**](d3dxframe.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции анимации](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
