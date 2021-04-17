---
description: Использует левую систему координат для создания линии.
ms.assetid: 0d2ef331-9edf-4b0a-ace4-ecb8bb2f7352
title: Функция D3DXCreateLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cf7d75ca63d64be39733b36a1b7d7a1b464238e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694124"
---
# <a name="d3dxcreateline-function"></a>Функция D3DXCreateLine

Использует левую систему координат для создания линии.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateLine(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXLINE        *ppLine
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с сеткой созданных Box.

</dd> <dt>

*пплине* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXLINE**](id3dxline.md)\***

Указатель на интерфейс [**ID3DXLine**](id3dxline.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
