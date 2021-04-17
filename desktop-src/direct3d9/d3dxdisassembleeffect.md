---
description: Расформирование результата.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: Функция D3DXDisassembleEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 945c30319d16264a2b7489d1dc0849a4678cbede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703793"
---
# <a name="d3dxdisassembleeffect-function"></a>Функция D3DXDisassembleEffect

Расформирование результата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пеффект* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)**

Указатель на интерфейс [**ID3DXEffect**](id3dxeffect.md) , который содержит результат.

</dd> <dt>

*Енаблеколоркоде* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Включите выделение цветом, чтобы облегчить чтение дизассемблированного кода.

</dd> <dt>

*ппдисассембли* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Возвращает буфер, содержащий десобранный шейдер. См. [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции эффектов](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
