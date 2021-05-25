---
description: Компилирует шейдер из действия, содержащего одну или несколько функций.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'Метод ID3DXEffectCompiler:: Компилешадер (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3e8d1d72fccd5c4ad47d21d05ee46013860a7743
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343629"
---
# <a name="id3dxeffectcompilercompileshader-method"></a>Метод ID3DXEffectCompiler:: Компилешадер

Компилирует шейдер из действия, содержащего одну или несколько функций.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфунктион* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор компилируемой функции. Это значение не должно быть **равно NULL**. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*птаржет* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на профиль шейдера, который определяет набор инструкций шейдера. Список доступных профилей см. в разделе [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) или [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Параметры компиляции, определяемые различными флагами. Компилятор Direct3D 10 HLSL теперь является значением по умолчанию. Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .

</dd> <dt>

*ппшадер* \[ out, retval\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Буфер, содержащий скомпилированный шейдер. Шейдер компилятора — это массив DWORD. Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*пперрормсгс* \[ out, retval\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Буфер, содержащий по крайней мере первое сообщение об ошибке компиляции. Это относится к ошибкам компилятора и ошибкам при компиляции на высоком уровне. Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ппконстанттабле* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Возвращает интерфейс [**ID3DXConstantTable**](id3dxconstanttable.md) , который можно использовать для доступа к константам шейдера. Это значение может быть **равно NULL**. Если приложение компилируется как большой адрес (то есть для работы с адресами, превышающими 2 ГБ, используется параметр компоновщика/LARGEADDRESSAWARE), этот параметр использовать нельзя, и его значение должно быть равно **null**. Вместо этого необходимо использовать функцию [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) , чтобы извлечь таблицу-константу шейдера, внедренную в шейдер. В этом вызове **D3DXGetShaderConstantTableEx** необходимо передать флаг **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** в параметр *flags* , чтобы указать, чтобы получить доступ к 4 ГБ виртуального адресного пространства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ .

Если аргументы недопустимы, метод возвратит D3DERR \_ инвалидкалл.

Если метод завершается с ошибкой, возвращается значение E \_ Failed.

## <a name="remarks"></a>Remarks

Целевые объекты можно указать для шейдеров вершин, шейдеров пикселей и функций заливки текстур.



| Целевые объекты                      | Функции                                                                      |
|-----------------------|-----------------------------------------------------------------------|
| Цели шейдера вершин | VS \_ 1 \_ , vs 2 \_ \_ 0, VS \_ 2 \_ SW, VS \_ 3 \_ 0                               |
| Цели шейдера пикселей  | PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4, PS \_ 2 \_ 0, PS \_ 2 \_ SW, PS \_ 3 \_ 0 |
| Цели заливки текстур  | TX \_ 0, TX \_ 1                                                          |



 

Этот метод компилирует шейдер из функции, написанной на языке C. Подробнее: [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
