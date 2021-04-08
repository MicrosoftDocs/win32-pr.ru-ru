---
description: Подсчитывает количество кадров в поддереве с именами, отличными от NULL.
ms.assetid: bc1cb985-acd1-4ba0-bb3c-3e86fea559da
title: Функция D3DXFrameNumNamedMatrices (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameNumNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c2d535a41d15987df7816cfc23f1bb213b6adc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000362"
---
# <a name="d3dxframenumnamedmatrices-function"></a>Функция D3DXFrameNumNamedMatrices

Подсчитывает количество кадров в поддереве с именами, отличными от NULL.

## <a name="syntax"></a>Синтаксис


```C++
UINT D3DXFrameNumNamedMatrices(
  _In_ const D3DXFRAME *pFrameRoot
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфрамерут* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXFRAME**](d3dxframe.md) \***

Указатель на корневой узел поддерева.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Возвращает число кадров.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции анимации](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
