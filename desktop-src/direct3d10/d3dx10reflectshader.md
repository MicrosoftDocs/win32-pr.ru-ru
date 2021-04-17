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
# <a name="d3dx10reflectshader-function"></a><span data-ttu-id="7720f-104">Функция D3DX10ReflectShader</span><span class="sxs-lookup"><span data-stu-id="7720f-104">D3DX10ReflectShader function</span></span>

<span data-ttu-id="7720f-105">Эта функция, которая создает объект отражения шейдера для получения сведений о скомпилированном шейдере, больше не существует.</span><span class="sxs-lookup"><span data-stu-id="7720f-105">This function -- which creates a shader-reflection object for retrieving information about a compiled shader -- no longer exists.</span></span> <span data-ttu-id="7720f-106">Вместо этого используйте [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) или [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span><span class="sxs-lookup"><span data-stu-id="7720f-106">Instead, use [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) or [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7720f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7720f-107">Syntax</span></span>


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a><span data-ttu-id="7720f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7720f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7720f-109">*пшадербитекоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7720f-109">*pShaderBytecode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7720f-110">Тип: **константа \* void**</span><span class="sxs-lookup"><span data-stu-id="7720f-110">Type: **const void\***</span></span>

<span data-ttu-id="7720f-111">Указатель на скомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="7720f-111">A pointer to the compiled shader.</span></span> <span data-ttu-id="7720f-112">Чтобы получить этот указатель, см. раздел [Получение указателя на скомпилированный шейдер](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span><span class="sxs-lookup"><span data-stu-id="7720f-112">To get this pointer see [Getting a Pointer to a Compiled Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>

</dd> <dt>

<span data-ttu-id="7720f-113">*Битекоделенгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7720f-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7720f-114">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7720f-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7720f-115">Длина Пшадербитекоде.</span><span class="sxs-lookup"><span data-stu-id="7720f-115">Length of pShaderBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="7720f-116">*ппрефлектор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7720f-116">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7720f-117">Тип: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span><span class="sxs-lookup"><span data-stu-id="7720f-117">Type: **[**ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span></span>

<span data-ttu-id="7720f-118">Адрес интерфейса отражения шейдера (см. [**интерфейс ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)).</span><span class="sxs-lookup"><span data-stu-id="7720f-118">Address of a shader reflection interface (see [**ID3D10ShaderReflection1 Interface**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7720f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7720f-119">Return value</span></span>

<span data-ttu-id="7720f-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7720f-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7720f-121">Возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7720f-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7720f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7720f-122">Remarks</span></span>

<span data-ttu-id="7720f-123">Ниже приведен пример создания объекта Shader-Reflection.</span><span class="sxs-lookup"><span data-stu-id="7720f-123">Here is an example of creating a shader-reflection object.</span></span> <span data-ttu-id="7720f-124">В этом примере предполагается, что вы начинаете с скомпилированного шейдера (показанного как</span><span class="sxs-lookup"><span data-stu-id="7720f-124">The example assumes you start with a compiled shader (shown as</span></span>


```
pVSBuf
```



<span data-ttu-id="7720f-125">который можно просмотреть в [примере HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span><span class="sxs-lookup"><span data-stu-id="7720f-125">which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7720f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7720f-126">Requirements</span></span>



| <span data-ttu-id="7720f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7720f-127">Requirement</span></span> | <span data-ttu-id="7720f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7720f-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7720f-129">Header</span><span class="sxs-lookup"><span data-stu-id="7720f-129">Header</span></span><br/> | <dl> <span data-ttu-id="7720f-130"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7720f-130"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7720f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7720f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7720f-132">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="7720f-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
