---
description: Переключает состояние литерала для параметра. Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'Метод ID3DXEffectCompiler:: Сетлитерал (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d28ee64c1d1e52b4005c1a81ef4690c539a09e06eb7a8378a246184cf4d2fd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295835"
---
# <a name="id3dxeffectcompilersetliteral-method"></a>Метод ID3DXEffectCompiler:: Сетлитерал

Переключает состояние литерала для параметра. Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор параметра. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Литерал* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Задайте значение **true** , чтобы сделать параметр литералом, и **false** , если параметр может изменить значение во время жизни шейдера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Эти методы изменяют только то, является ли параметр литералом. Чтобы изменить значение параметра, используйте такой метод, как [**ID3DXBaseEffect:: сетбул**](id3dxbaseeffect--setbool.md) или [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).

Эта функция должна вызываться перед компиляцией результата. Ниже приведен пример того, как одна из этих функций может использоваться:


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Использование и литералы (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler::**](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
