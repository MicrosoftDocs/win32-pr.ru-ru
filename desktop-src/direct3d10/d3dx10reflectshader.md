---
description: Эта функция, которая создает объект отражения шейдера для получения сведений о скомпилированном шейдере, больше не существует. Вместо этого используйте D3DReflect или D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: Функция D3DX10ReflectShader (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 15201bcbde2792bbd31cbf4dad7b87d7ddac5053
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105651553"
---
# <a name="d3dx10reflectshader-function"></a>Функция D3DX10ReflectShader

Эта функция, которая создает объект отражения шейдера для получения сведений о скомпилированном шейдере, больше не существует. Вместо этого используйте [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) или [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пшадербитекоде* \[ окне\]
</dt> <dd>

Тип: **константа \* void**

Указатель на скомпилированный шейдер. Чтобы получить этот указатель, см. раздел [Получение указателя на скомпилированный шейдер](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

</dd> <dt>

*Битекоделенгс* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)**

Длина Пшадербитекоде.

</dd> <dt>

*ппрефлектор* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***

Адрес интерфейса отражения шейдера (см. [**интерфейс ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Комментарии

Ниже приведен пример создания объекта Shader-Reflection. В этом примере предполагается, что вы начинаете с скомпилированного шейдера (показанного как


```
pVSBuf
```



который можно просмотреть в [примере HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
