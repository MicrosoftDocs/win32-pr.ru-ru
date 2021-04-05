---
description: Возвращает имя высокоуровневого профиля языка шейдеров (HLSL), поддерживаемого данным устройством.
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: Функция D3DXGetPixelShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ad1f430a95b1ff2173dceb1e0561dccf3d0ee88d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000360"
---
# <a name="d3dxgetpixelshaderprofile-function"></a><span data-ttu-id="b79ff-103">Функция D3DXGetPixelShaderProfile</span><span class="sxs-lookup"><span data-stu-id="b79ff-103">D3DXGetPixelShaderProfile function</span></span>

<span data-ttu-id="b79ff-104">Возвращает имя высокоуровневого профиля языка шейдеров (HLSL), поддерживаемого данным устройством.</span><span class="sxs-lookup"><span data-stu-id="b79ff-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b79ff-105">Syntax</span></span>


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="b79ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b79ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b79ff-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b79ff-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b79ff-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b79ff-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b79ff-109">Указатель на устройство.</span><span class="sxs-lookup"><span data-stu-id="b79ff-109">Pointer to the device.</span></span> <span data-ttu-id="b79ff-110">См. [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="b79ff-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b79ff-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b79ff-111">Return value</span></span>

<span data-ttu-id="b79ff-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b79ff-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b79ff-113">Имя профиля HLSL.</span><span class="sxs-lookup"><span data-stu-id="b79ff-113">The HLSL profile name.</span></span>

<span data-ttu-id="b79ff-114">Если устройство не поддерживает шейдеры пикселей, функция возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b79ff-114">If the device does not support pixel shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b79ff-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b79ff-115">Remarks</span></span>

<span data-ttu-id="b79ff-116">Профиль шейдера указывает версию шейдера сборки для использования и возможности, доступные компилятору HLSL при компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="b79ff-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="b79ff-117">В следующей таблице перечислены поддерживаемые профили шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="b79ff-117">The following table lists the pixel shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b79ff-118">Профиль шейдера</span><span class="sxs-lookup"><span data-stu-id="b79ff-118">Shader Profile</span></span></th>
<th><span data-ttu-id="b79ff-119">Описание</span><span class="sxs-lookup"><span data-stu-id="b79ff-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b79ff-120">ps_1_1</span><span class="sxs-lookup"><span data-stu-id="b79ff-120">ps_1_1</span></span></td>
<td><span data-ttu-id="b79ff-121">Компилировать до ps_1_1 версии.</span><span class="sxs-lookup"><span data-stu-id="b79ff-121">Compile to ps_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b79ff-122">ps_1_2</span><span class="sxs-lookup"><span data-stu-id="b79ff-122">ps_1_2</span></span></td>
<td><span data-ttu-id="b79ff-123">Компилировать до ps_1_2 версии.</span><span class="sxs-lookup"><span data-stu-id="b79ff-123">Compile to ps_1_2 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b79ff-124">ps_1_3</span><span class="sxs-lookup"><span data-stu-id="b79ff-124">ps_1_3</span></span></td>
<td><span data-ttu-id="b79ff-125">Компилировать до ps_1_3 версии.</span><span class="sxs-lookup"><span data-stu-id="b79ff-125">Compile to ps_1_3 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b79ff-126">ps_1_4</span><span class="sxs-lookup"><span data-stu-id="b79ff-126">ps_1_4</span></span></td>
<td><span data-ttu-id="b79ff-127">Компилировать до ps_1_4 версии.</span><span class="sxs-lookup"><span data-stu-id="b79ff-127">Compile to ps_1_4 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b79ff-128">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="b79ff-128">ps_2_0</span></span></td>
<td><span data-ttu-id="b79ff-129">Компилировать до ps_2_0 версии.</span><span class="sxs-lookup"><span data-stu-id="b79ff-129">Compile to ps_2_0 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b79ff-130">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="b79ff-130">ps_2_a</span></span></td>
<td><span data-ttu-id="b79ff-131">То же, что и профиль ps_2_0, со следующими дополнительными возможностями, доступными для целевого компилятора:</span><span class="sxs-lookup"><span data-stu-id="b79ff-131">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="b79ff-132">Количество временных регистров (r #) больше или равно 22.</span><span class="sxs-lookup"><span data-stu-id="b79ff-132">Number of Temporary Registers (r#) is greater than or equal to 22.</span></span></li>
<li><span data-ttu-id="b79ff-133">Произвольный источник свиззле.</span><span class="sxs-lookup"><span data-stu-id="b79ff-133">Arbitrary source swizzle.</span></span></li>
<li><span data-ttu-id="b79ff-134">Инструкции по градиенту: ДСКС, ДСИ.</span><span class="sxs-lookup"><span data-stu-id="b79ff-134">Gradient instructions: dsx, dsy.</span></span></li>
<li><span data-ttu-id="b79ff-135">Затенения.</span><span class="sxs-lookup"><span data-stu-id="b79ff-135">Predication.</span></span></li>
<li><span data-ttu-id="b79ff-136">Нет ограничения на чтение зависимой текстуры.</span><span class="sxs-lookup"><span data-stu-id="b79ff-136">No dependent texture read limit.</span></span></li>
<li><span data-ttu-id="b79ff-137">Нет ограничений на количество инструкций текстуры.</span><span class="sxs-lookup"><span data-stu-id="b79ff-137">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b79ff-138">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="b79ff-138">ps_2_b</span></span></td>
<td><span data-ttu-id="b79ff-139">То же, что и профиль ps_2_0, со следующими дополнительными возможностями, доступными для целевого компилятора:</span><span class="sxs-lookup"><span data-stu-id="b79ff-139">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="b79ff-140">Количество временных регистров (r #) больше или равно 32.</span><span class="sxs-lookup"><span data-stu-id="b79ff-140">Number of Temporary Registers (r#) is greater than or equal to 32.</span></span></li>
<li><span data-ttu-id="b79ff-141">Нет ограничений на количество инструкций текстуры.</span><span class="sxs-lookup"><span data-stu-id="b79ff-141">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b79ff-142">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="b79ff-142">ps_3_0</span></span></td>
<td><span data-ttu-id="b79ff-143">Компилировать до ps_3_0 версии.</span><span class="sxs-lookup"><span data-stu-id="b79ff-143">Compile to ps_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b79ff-144">Дополнительные сведения о различиях между версиями шейдера см. в разделе [различия шейдеров пикселей](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b79ff-144">For more information about the differences between shader versions, see [Pixel Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b79ff-145">Требования</span><span class="sxs-lookup"><span data-stu-id="b79ff-145">Requirements</span></span>



| <span data-ttu-id="b79ff-146">Требование</span><span class="sxs-lookup"><span data-stu-id="b79ff-146">Requirement</span></span> | <span data-ttu-id="b79ff-147">Значение</span><span class="sxs-lookup"><span data-stu-id="b79ff-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b79ff-148">Header</span><span class="sxs-lookup"><span data-stu-id="b79ff-148">Header</span></span><br/>  | <dl> <span data-ttu-id="b79ff-149"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b79ff-149"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b79ff-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b79ff-150">Library</span></span><br/> | <dl> <span data-ttu-id="b79ff-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b79ff-151"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b79ff-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b79ff-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79ff-153">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="b79ff-153">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
