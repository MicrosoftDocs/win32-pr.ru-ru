---
title: Функция D3D11Reflect
description: Возвращает указатель на интерфейс отражения.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- Функция D3D11Reflect HLSL
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157243"
---
# <a name="d3d11reflect-function"></a>Функция D3D11Reflect

Возвращает указатель на интерфейс отражения.

## <a name="syntax"></a>Синтаксис

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*псркдата* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](/windows/desktop/WinProg/windows-data-types)**

Указатель на исходные данные в виде скомпилированного кода HLSL.

</dd> <dt>

*Сркдатасизе* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Длина *псркдата*.

</dd> <dt>

*ппрефлектор* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***

Адрес указателя на интерфейс [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

Возвращает один из кодов возврата, описанных в разделе [коды возврата Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).

## <a name="remarks"></a>Примечания

Встроенная функция компилятора **D3D11Reflect** является оболочкой для функции компилятора [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) . **D3D11Reflect** может получать интерфейс [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) только из шейдера. **D3DReflect** может получить интерфейс **ID3D11ShaderReflection** или интерфейс отражения direct3d 10 или Direct3D 10,1, например [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).

Код шейдера содержит метаданные, которые можно проверить с помощью API-интерфейсов отражения.

В следующем коде показано, как получить интерфейс [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) из шейдера.


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DCompiler. inl</dt> </dl>     |
| Библиотека<br/> | <dl> <dt>D3dcompiler \_ 47. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dcompiler \_47.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

