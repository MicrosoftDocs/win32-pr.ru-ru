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
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354353"
---
# <a name="id3dxeffectcompilersetliteral-method"></a><span data-ttu-id="11522-104">Метод ID3DXEffectCompiler:: Сетлитерал</span><span class="sxs-lookup"><span data-stu-id="11522-104">ID3DXEffectCompiler::SetLiteral method</span></span>

<span data-ttu-id="11522-105">Переключает состояние литерала для параметра.</span><span class="sxs-lookup"><span data-stu-id="11522-105">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="11522-106">Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.</span><span class="sxs-lookup"><span data-stu-id="11522-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="11522-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11522-107">Syntax</span></span>


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a><span data-ttu-id="11522-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11522-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11522-109">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11522-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11522-110">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="11522-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="11522-111">Уникальный идентификатор параметра.</span><span class="sxs-lookup"><span data-stu-id="11522-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="11522-112">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="11522-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="11522-113">*Литерал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11522-113">*Literal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11522-114">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11522-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11522-115">Задайте значение **true** , чтобы сделать параметр литералом, и **false** , если параметр может изменить значение во время жизни шейдера.</span><span class="sxs-lookup"><span data-stu-id="11522-115">Set to **TRUE** to make the parameter a literal, and **FALSE** if the parameter can change value during the shader lifetime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11522-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11522-116">Return value</span></span>

<span data-ttu-id="11522-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="11522-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="11522-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="11522-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="11522-119">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="11522-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="11522-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11522-120">Remarks</span></span>

<span data-ttu-id="11522-121">Эти методы изменяют только то, является ли параметр литералом.</span><span class="sxs-lookup"><span data-stu-id="11522-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="11522-122">Чтобы изменить значение параметра, используйте такой метод, как [**ID3DXBaseEffect:: сетбул**](id3dxbaseeffect--setbool.md) или [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="11522-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

<span data-ttu-id="11522-123">Эта функция должна вызываться перед компиляцией результата.</span><span class="sxs-lookup"><span data-stu-id="11522-123">This function must be called before the effect is compiled.</span></span> <span data-ttu-id="11522-124">Ниже приведен пример того, как одна из этих функций может использоваться:</span><span class="sxs-lookup"><span data-stu-id="11522-124">Here is an example of how one might use this function:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="11522-125">Требования</span><span class="sxs-lookup"><span data-stu-id="11522-125">Requirements</span></span>



| <span data-ttu-id="11522-126">Требование</span><span class="sxs-lookup"><span data-stu-id="11522-126">Requirement</span></span> | <span data-ttu-id="11522-127">Значение</span><span class="sxs-lookup"><span data-stu-id="11522-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="11522-128">Header</span><span class="sxs-lookup"><span data-stu-id="11522-128">Header</span></span><br/>  | <dl> <span data-ttu-id="11522-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="11522-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="11522-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11522-130">Library</span></span><br/> | <dl> <span data-ttu-id="11522-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11522-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="11522-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11522-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11522-133">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="11522-133">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="11522-134">Использование и литералы (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="11522-134">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="11522-135">**ID3DXEffectCompiler::**</span><span class="sxs-lookup"><span data-stu-id="11522-135">**ID3DXEffectCompiler::GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
