---
title: Функция D3DX11CompileFromResource (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать функции ресурсов, а затем компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать один из API-интерфейсов компиляции HLSL, таких как API D3DCompile. Компиляция шейдера или воздействия ресурса.
ms.assetid: ececa469-f5e3-4cb3-befe-0ed1a5a57671
keywords:
- D3DX11CompileFromResource функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26eeb825a1d3b6bcda9f77eae24c99c3cec168b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000446"
---
# <a name="d3dx11compilefromresource-function"></a>Функция D3DX11CompileFromResource

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

> [!Note]  
> Вместо использования этой функции рекомендуется использовать [функции ресурсов](/windows/desktop/menurc/resources-functions), а затем компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать один из API-интерфейсов компиляции HLSL, таких как API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .

 

Компиляция шейдера или воздействия ресурса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсркмодуле* \[ окне\]
</dt> <dd>

Тип: **[ **хмодуле**](/windows/desktop/WinProg/windows-data-types)**

Обработчик для модуля ресурсов, содержащего шейдер. ХМОДУЛЕ можно получить с помощью [функции ошибка GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*псркресаурце* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Имя ресурса, содержащего шейдер. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае тип данных разрешается в LPCSTR.

</dd> <dt>

*псркфиленаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Необязательный параметр. Имя файла эффектов, которое используется только для сообщений об ошибках. Может иметь **значение NULL**.

</dd> <dt>

*пдефинес* \[ окне\]
</dt> <dd>

Тип: **\* const [**D3D10ный \_ \_ макрос шейдера**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**

Необязательный параметр. Указатель на массив определений макросов (см. раздел [**D3D10 \_ Shader \_ Macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). Последняя структура в массиве выступает в качестве признака конца, и все члены должны иметь значение 0. Если не используется, задайте  для Пдефинес **значение NULL**.

</dd> <dt>

*пинклуде* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Необязательный параметр. Указатель на интерфейс для обработки включаемых файлов. Установка **значения NULL** приведет к ошибке компиляции, если шейдер содержит \# include.

</dd> <dt>

*пфунктионнаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Имя функции-точки входа шейдера, где начинается выполнение шейдера. При компиляции результата **D3DX11CompileFromResource** игнорирует *пфунктионнаме*; рекомендуется установить *пфунктионнаме* в **значение NULL** , так как рекомендуется установить параметр указателя равным **null** , если вызываемая функция не будет ее использовать.

</dd> <dt>

*ппрофиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Строка, указывающая модель шейдера; может быть любым профилем в шейдере Model 2, Shader Model 3, Shader Model 4 или Shader Model 5. Профиль также может иметь тип действия (например, FX \_ 4 \_ 1).

</dd> <dt>

*Flags1* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

[**Флаги компиляции**](/windows/desktop/direct3dhlsl/d3dcompile-constants)шейдера.

</dd> <dt>

*Flags2* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

[**Флаги компиляции**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)эффектов. При компиляции шейдера, а не файла эффектов **D3DX11CompileFromResource** игнорирует *Flags2*. рекомендуется установить *Flags2* в нулевое значение, так как рекомендуется установить неуказательный параметр в нуль, если вызываемая функция не будет ее использовать.

</dd> <dt>

*ппумп* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md)). Используйте **null** , чтобы указать, что эта функция не должна возвращать значение до ее завершения.

</dd> <dt>

*ппшадер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Указатель на память, которая содержит скомпилированный шейдер, а также любые внедренные сведения о отладочной и символьной таблицах.

</dd> <dt>

*пперрормсгс* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Указатель на память, которая содержит список ошибок и предупреждений, произошедших во время компиляции. Эти ошибки и предупреждения идентичны отладочным данным отладчика.

</dd> <dt>

*фресулт* \[ заполняет\]
</dt> <dd>

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Указатель на возвращаемое значение. Может иметь **значение NULL**. Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

**D3DX11CompileFromResource** возвращает E \_ INVALIDARG, если параметр *фресулт* предоставляет значение, отличное от **null** , при указании **значения NULL** для параметра *ппумп* . Дополнительные сведения об этой ситуации см. в разделе Примечания.

## <a name="remarks"></a>Примечания

Дополнительные сведения о **D3DX11CompileFromResource** см. в разделе [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).

Если параметру *ппумп* также присвоено **значение NULL** , необходимо указать **значение NULL** для параметра *фресулт* . В противном случае вы не сможете создать шейдер с помощью скомпилированного кода шейдера, который **D3DX11CompileFromResource** возвращает в памяти, на которую указывает параметр *ппшадер* . Чтобы создать шейдер из скомпилированного кода шейдера, необходимо вызвать один из следующих методов интерфейса [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :

-   [**креатекомпутешадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**креатедомаиншадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**креатежеометришадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**креатежеометришадервисстреамаутпут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**креатехуллшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**креатепикселшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**креатевертексшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Кроме того, если вы передаете значение, отличное от **null** , *фресулт* при указании значения **null** для *ппумп*, **D3DX11CompileFromResource** возвращает \_ код ошибки E INVALIDARG.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

