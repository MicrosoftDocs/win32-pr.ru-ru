---
description: Функция D3DXAssembleShaderFromFile — формирование шейдера.
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: Функция D3DXAssembleShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91aaf2924638b1db5b0e8ec0782b90fa964a9543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116032"
---
# <a name="d3dxassembleshaderfromfile-function"></a>Функция D3DXAssembleShaderFromFile

Сборка шейдера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXAssembleShaderFromFile(
  _In_        LPCTSTR       pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псркфиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Указатель на строку, указывающую имя файла. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае строковый тип данных разрешается в LPCSTR. См. заметки.

</dd> <dt>

*пдефинес* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***

Необязательный массив структур [**D3DXMACRO**](d3dxmacro.md) , заканчивающийся **нулевым значением** . Это значение может быть **равно NULL**.

</dd> <dt>

*пинклуде* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include. Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Параметры компиляции, определяемые различными флагами. Компилятор Direct3D 10 HLSL теперь является значением по умолчанию. Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .

</dd> <dt>

*ппшадер* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Возвращает буфер, содержащий созданный шейдер. Этот буфер содержит скомпилированный код шейдера, а также любые внедренные сведения о таблицах отладки и символов.

</dd> <dt>

*пперрормсгс* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Возвращает буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции. Это те же сообщения, которые отладчик отображает при работе в режиме отладки. Это значение может быть **равно NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXAssembleShaderFromFileW. В противном случае вызов функции разрешается в D3DXAssembleShaderFromFileA, так как используются строки ANSI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
