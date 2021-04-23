---
title: Тип шейдера
description: Синтаксис объявления переменной шейдера в результате изменился с Direct3D 9 на Direct3D 10.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- Тип шейдера HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984056"
---
# <a name="shader-type"></a><span data-ttu-id="80657-104">Тип шейдера</span><span class="sxs-lookup"><span data-stu-id="80657-104">Shader Type</span></span>

<span data-ttu-id="80657-105">Синтаксис объявления переменной шейдера в результате изменился с Direct3D 9 на Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="80657-105">The syntax for declaring a shader variable in an effect changed from Direct3D 9 to Direct3D 10.</span></span>

## <a name="shader-type-for-direct3d-10"></a><span data-ttu-id="80657-106">Тип шейдера для Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="80657-106">Shader Type for Direct3D 10</span></span>

<span data-ttu-id="80657-107">Объявите переменную шейдера в рамках этапа (в Direct3D 10) с помощью синтаксиса типа шейдера:</span><span class="sxs-lookup"><span data-stu-id="80657-107">Declare a shader variable within an effect pass (in Direct3D 10) using the shader type syntax:</span></span>



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80657-108">**Сетпикселшадер** Compile ( **шадертаржет, шадерфунктион** ); **Сетжеометришадер** Compile ( **шадертаржет, шадерфунктион** ); **Сетвертексшадер** Compile ( **шадертаржет, шадерфунктион** );</span><span class="sxs-lookup"><span data-stu-id="80657-108">**SetPixelShader** Compile( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile( **ShaderTarget, ShaderFunction** );</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="80657-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="80657-109">Parameters</span></span>



| <span data-ttu-id="80657-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="80657-110">Item</span></span>                                                                                                                             | <span data-ttu-id="80657-111">Описание</span><span class="sxs-lookup"><span data-stu-id="80657-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80657-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**сетксксксшадер**</span><span class="sxs-lookup"><span data-stu-id="80657-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span></span><br/>         | <span data-ttu-id="80657-113">Вызов API Direct3D, который создает объект шейдера.</span><span class="sxs-lookup"><span data-stu-id="80657-113">The Direct3D API call that creates the shader object.</span></span> <span data-ttu-id="80657-114">Может быть либо: **сетпикселшадер** , либо **Сетжеометришадер** , либо **сетвертексшадер**.</span><span class="sxs-lookup"><span data-stu-id="80657-114">Can be either: **SetPixelShader** or **SetGeometryShader** or **SetVertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="80657-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**шадертаржет**</span><span class="sxs-lookup"><span data-stu-id="80657-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>         | <span data-ttu-id="80657-116">Модель шейдера для компиляции.</span><span class="sxs-lookup"><span data-stu-id="80657-116">The shader model to compile against.</span></span> <span data-ttu-id="80657-117">Это допустимо для любого целевого объекта, включая все целевые объекты Direct3D 9, а также целевые объекты [модели шейдеров 4](dx-graphics-hlsl-sm4.md) : VS \_ 4 \_ 0, GS \_ 4 \_ 0 и PS \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="80657-117">This is valid for any target including all Direct3D 9 targets plus the [shader model 4](dx-graphics-hlsl-sm4.md) targets: vs\_4\_0, gs\_4\_0, and ps\_4\_0.</span></span><br/>                                                                                                                                                                                                                                          |
| <span data-ttu-id="80657-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**шадерфунктион**</span><span class="sxs-lookup"><span data-stu-id="80657-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span></span><br/> | <span data-ttu-id="80657-119">Строка ASCII, содержащая имя функции точки входа шейдера; Это функция, которая начинает выполнение при вызове шейдера.</span><span class="sxs-lookup"><span data-stu-id="80657-119">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="80657-120">(...) Представляет аргументы шейдера; Это те же аргументы, которые передаются в API создания шейдера: [**вссетшадер**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) или [**гссетшадер**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) или [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="80657-120">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) or [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) or [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="80657-121">Например, .</span><span class="sxs-lookup"><span data-stu-id="80657-121">Example</span></span>

<span data-ttu-id="80657-122">Ниже приведен пример создания шейдера вершин и объекта шейдера пикселей, скомпилированного для конкретной модели шейдера.</span><span class="sxs-lookup"><span data-stu-id="80657-122">Here is an example that creates a vertex shader and pixel shader object, compiled for a particular shader model.</span></span> <span data-ttu-id="80657-123">В примере Direct3D 10 нет шейдера Geometry, поэтому указатель имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="80657-123">In the Direct3D 10 example, there is no geometry shader, so the pointer is set to **NULL**.</span></span>


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a><span data-ttu-id="80657-124">Тип шейдера для Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="80657-124">Shader Type for Direct3D 9</span></span>

<span data-ttu-id="80657-125">Объявите переменную шейдера в рамках этапа (для Direct3D 9) с помощью синтаксиса типа шейдера:</span><span class="sxs-lookup"><span data-stu-id="80657-125">Declare a shader variable within an effect pass (for Direct3D 9) using the shader type syntax:</span></span>



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80657-126">**PixelShader** = компилировать **шадертаржет шадерфунктион (...); Вертексшадер** = компилировать **шадертаржет шадерфунктион (...);**</span><span class="sxs-lookup"><span data-stu-id="80657-126">**PixelShader** = compile **ShaderTarget ShaderFunction(...);VertexShader** = compile **ShaderTarget ShaderFunction(...);**</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="80657-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="80657-127">Parameters</span></span>



| <span data-ttu-id="80657-128">Элемент</span><span class="sxs-lookup"><span data-stu-id="80657-128">Item</span></span>                                                                                                                                                 | <span data-ttu-id="80657-129">Описание</span><span class="sxs-lookup"><span data-stu-id="80657-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80657-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**ксксксшадер**</span><span class="sxs-lookup"><span data-stu-id="80657-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span></span><br/>                                         | <span data-ttu-id="80657-131">Переменная шейдера, представляющая Скомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="80657-131">A shader variable, which represents the compiled shader.</span></span> <span data-ttu-id="80657-132">Может быть либо: **PixelShader** , либо **вертексшадер**.</span><span class="sxs-lookup"><span data-stu-id="80657-132">Can be either: **PixelShader** or **VertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="80657-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**шадертаржет**</span><span class="sxs-lookup"><span data-stu-id="80657-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>                             | <span data-ttu-id="80657-134">[Модель шейдера](dx-graphics-hlsl-models.md) для компиляции; зависит от типа переменной шейдера.</span><span class="sxs-lookup"><span data-stu-id="80657-134">The [shader model](dx-graphics-hlsl-models.md) to compile against; depends on the type of shader variable.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="80657-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**Шадерфунктион (...)**</span><span class="sxs-lookup"><span data-stu-id="80657-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span></span><br/> | <span data-ttu-id="80657-136">Строка ASCII, содержащая имя функции точки входа шейдера; Это функция, которая начинает выполнение при вызове шейдера.</span><span class="sxs-lookup"><span data-stu-id="80657-136">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="80657-137">(...) Представляет аргументы шейдера; Это те же аргументы, которые передаются в API создания шейдера: [**сетвертексшадер**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) или [**сетпикселшадер**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span><span class="sxs-lookup"><span data-stu-id="80657-137">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) or [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="80657-138">Например, .</span><span class="sxs-lookup"><span data-stu-id="80657-138">Example</span></span>

<span data-ttu-id="80657-139">Ниже приведен пример шейдера вершин и объекта шейдера пикселей, скомпилированного для определенной модели шейдера.</span><span class="sxs-lookup"><span data-stu-id="80657-139">Here is an example of a vertex shader and pixel shader object, compiled for a particular shader model.</span></span>


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a><span data-ttu-id="80657-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80657-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80657-141">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80657-141">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

