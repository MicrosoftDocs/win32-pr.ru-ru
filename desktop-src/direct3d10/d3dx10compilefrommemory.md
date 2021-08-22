---
description: Примечание. вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API D3DCompile. Скомпилируйте шейдер или результат, который загружается в память.
ms.assetid: c6458d82-a649-402c-8180-5b7320f9fdb0
title: Функция D3DX10CompileFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: f5cd6772079f872fe575a3a2f49fee536b89dab00f29a62dba151842dbc99b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281714"
---
# <a name="d3dx10compilefrommemory-function"></a>Функция D3DX10CompileFromMemory

> [!Note]  
> Вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .

 

Скомпилируйте шейдер или результат, который загружается в память.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псркдата* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на шейдер в памяти.

</dd> <dt>

*Сркдатален* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)**

Размер шейдера в памяти.

</dd> <dt>

*пфиленаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Имя файла, содержащего код шейдера.

</dd> <dt>

*пдефинес* \[ окне\]
</dt> <dd>

Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**

Необязательный элемент. Указатель на массив определений макросов (см. [**\_ \_ макрос D3D Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). Последняя структура в массиве выступает в качестве признака конца, и все члены должны иметь значение 0. Если не используется, задайте  для Пдефинес **значение NULL**.

</dd> <dt>

*пинклуде* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Необязательный элемент. Указатель на интерфейс интерфейса [**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) для обработки включаемых файлов. Установка **значения NULL** приведет к ошибке компиляции, если шейдер содержит \# include.

</dd> <dt>

*пфунктионнаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Имя функции-точки входа шейдера, где начинается выполнение шейдера. При компиляции результата **D3DX10CompileFromMemory** игнорирует *пфунктионнаме*; рекомендуется установить *пфунктионнаме* в **значение NULL** , так как рекомендуется установить параметр указателя равным **null** , если вызываемая функция не будет ее использовать.

</dd> <dt>

*ппрофиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Строка, указывающая модель шейдера; может быть любым профилем в [шейдере Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)или [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).

</dd> <dt>

*Flags1* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

[Флаги компиляции шейдера](d3d10-shader.md).

</dd> <dt>

*Flags2* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

[Флаги компиляции эффектов](d3d10-graphics-reference-effect-constants.md). При компиляции шейдера, а не файла эффектов **D3DX10CompileFromMemory** игнорирует *Flags2*. рекомендуется установить *Flags2* в нулевое значение, так как рекомендуется установить неуказательный параметр в нуль, если вызываемая функция не будет ее использовать.

</dd> <dt>

*ппумп* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)). Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.

</dd> <dt>

*ппшадер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , содержащий скомпилированный шейдер, а также любые внедренные сведения о отладочной и символьной таблицах.

</dd> <dt>

*пперрормсгс* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , содержащий список ошибок и предупреждений, произошедших во время компиляции. Эти ошибки и предупреждения идентичны отладочным данным отладчика.

</dd> <dt>

*фресулт* \[ заполняет\]
</dt> <dd>

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Указатель на возвращаемое значение. Может иметь **значение NULL**. Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
