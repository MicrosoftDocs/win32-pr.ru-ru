---
description: Уничтожает поддерево фреймов в корне, включая корень.
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: Функция D3DXFrameDestroy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1c0809ff61abec6f55564ca17a116ad4c826bca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713687"
---
# <a name="d3dxframedestroy-function"></a>Функция D3DXFrameDestroy

Уничтожает поддерево фреймов в корне, включая корень.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфрамерут* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**

Указатель на корневой узел.

</dd> <dt>

*паллок* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Интерфейс выделения, используемый для освобождения узлов иерархии фреймов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции анимации](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




