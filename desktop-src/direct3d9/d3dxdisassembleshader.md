---
description: Расформирование шейдера.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: Функция D3DXDisassembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6192b77c190ed73dc6e5038c9119152836eca375
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694162"
---
# <a name="d3dxdisassembleshader-function"></a>Функция D3DXDisassembleShader

Расформирование шейдера.

> [!Note]  
> Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пшадер* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на буфер памяти, содержащий данные шейдера.

</dd> <dt>

*Енаблеколоркоде* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Включите код цвета, чтобы упростить чтение дизассемблированного кода.

</dd> <dt>

*пкомментс* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Необязательная строка комментария, заканчивающаяся нулем. Это значение может быть **равно NULL**.

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
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
