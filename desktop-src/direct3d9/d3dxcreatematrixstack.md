---
description: Создает экземпляр интерфейса ID3DXMATRIXStack.
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: Функция D3DXCreateMatrixStack (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694254"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a>Функция D3DXCreateMatrixStack (D3dx9math. h)

Создает экземпляр интерфейса [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Не реализован. Укажите нуль.

</dd> <dt>

*ппстакк* \[ заполняет\]
</dt> <dd>

Тип: **LPD3DXMATRIXSTACK \***

Адрес указателя, заполненного указателем интерфейса [**ID3DXMATRIXStack**](id3dxmatrixstack.md) , если функция выполнена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
