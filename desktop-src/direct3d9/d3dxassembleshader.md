---
description: Функция D3DXAssembleShader — формирование шейдера.
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: Функция D3DXAssembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4d3666342cbbd8999d6136e1a780e6cb0ba80970f0cc928f652338d4574f667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988844"
---
# <a name="d3dxassembleshader-function"></a>Функция D3DXAssembleShader

Сборка шейдера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXAssembleShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataLen,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псркдата* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на буфер памяти, содержащий данные шейдера.

</dd> <dt>

*Сркдатален* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Длина данных эффектов в байтах.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
</dt> <dt>

[**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 
