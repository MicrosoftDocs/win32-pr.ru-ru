---
description: Функция D3DXCreateEffectCompiler — создает компилятор эффектов из описания ASCII-результата.
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: Функция D3DXCreateEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 38ab58ed15609d468d25f4406353448e4fd6adb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115772"
---
# <a name="d3dxcreateeffectcompiler-function"></a>Функция D3DXCreateEffectCompiler

Создает компилятор эффектов из описания ASCII Effect.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псркдата* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на буфер, содержащий описание действия.

</dd> <dt>

*Сркдатален* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Длина данных эффектов в байтах.

</dd> <dt>

*пдефинес* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***

Необязательный завершающий **нуль** массив структур [**D3DXMACRO**](d3dxmacro.md) , описывающих определения препроцессора. Это значение может быть **равно NULL**.

</dd> <dt>

*пинклуде* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include. Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Параметры компиляции, определяемые различными флагами (см. раздел [Флаги D3DXSHADER](d3dxshader-flags.md)). Компилятор Direct3D 10 HLSL теперь является значением по умолчанию. Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .

</dd> <dt>

*ппеффекткомпилер* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***

Адрес указателя на интерфейс [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , содержащий компилятор эффектов.

</dd> <dt>

*пппарсиррорс* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , содержащий любые сообщения об ошибках, произошедшие во время компиляции. Этот параметр может иметь значение **null** , чтобы игнорировать сообщения об ошибках.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции эффектов](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
