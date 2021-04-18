---
description: Возвращает имя высокоуровневого профиля языка шейдеров (HLSL), поддерживаемого данным устройством.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Функция D3DXGetVertexShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f7ccaeba60bdd1d7c512cee3fb4da29289408a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713661"
---
# <a name="d3dxgetvertexshaderprofile-function"></a><span data-ttu-id="14f3c-103">Функция D3DXGetVertexShaderProfile</span><span class="sxs-lookup"><span data-stu-id="14f3c-103">D3DXGetVertexShaderProfile function</span></span>

<span data-ttu-id="14f3c-104">Возвращает имя высокоуровневого профиля языка шейдеров (HLSL), поддерживаемого данным устройством.</span><span class="sxs-lookup"><span data-stu-id="14f3c-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f3c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14f3c-105">Syntax</span></span>


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="14f3c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14f3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14f3c-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14f3c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f3c-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="14f3c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="14f3c-109">Указатель на устройство.</span><span class="sxs-lookup"><span data-stu-id="14f3c-109">Pointer to the device.</span></span> <span data-ttu-id="14f3c-110">См. [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="14f3c-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14f3c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14f3c-111">Return value</span></span>

<span data-ttu-id="14f3c-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14f3c-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14f3c-113">Имя профиля HLSL.</span><span class="sxs-lookup"><span data-stu-id="14f3c-113">The HLSL profile name.</span></span>

<span data-ttu-id="14f3c-114">Если устройство не поддерживает шейдеры вершин, функция возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="14f3c-114">If the device does not support vertex shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="14f3c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14f3c-115">Remarks</span></span>

<span data-ttu-id="14f3c-116">Профиль шейдера указывает версию шейдера сборки для использования и возможности, доступные компилятору HLSL при компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="14f3c-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="14f3c-117">В следующей таблице перечислены поддерживаемые профили шейдеров вершин.</span><span class="sxs-lookup"><span data-stu-id="14f3c-117">The following table lists the vertex shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14f3c-118">Профиль шейдера</span><span class="sxs-lookup"><span data-stu-id="14f3c-118">Shader Profile</span></span></th>
<th><span data-ttu-id="14f3c-119">Описание</span><span class="sxs-lookup"><span data-stu-id="14f3c-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="14f3c-120">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="14f3c-120">vs_1_1</span></span></td>
<td><span data-ttu-id="14f3c-121">Компилировать до vs_1_1 версии.</span><span class="sxs-lookup"><span data-stu-id="14f3c-121">Compile to vs_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14f3c-122">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="14f3c-122">vs_2_0</span></span></td>
<td><span data-ttu-id="14f3c-123">Компилировать до vs_2_0 версии.</span><span class="sxs-lookup"><span data-stu-id="14f3c-123">Compile to vs_2_0 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14f3c-124">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="14f3c-124">vs_2_a</span></span></td>
<td><span data-ttu-id="14f3c-125">То же, что и профиль vs_2_0, со следующими дополнительными возможностями, доступными для целевого компилятора:</span><span class="sxs-lookup"><span data-stu-id="14f3c-125">Same as the vs_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="14f3c-126">Количество временных регистров (r #) больше или равно 13.</span><span class="sxs-lookup"><span data-stu-id="14f3c-126">Number of Temporary Registers (r#) is greater than or equal to 13.</span></span></li>
<li><span data-ttu-id="14f3c-127">Динамическая Инструкция по управлению потоком.</span><span class="sxs-lookup"><span data-stu-id="14f3c-127">Dynamic flow control instruction.</span></span></li>
<li><span data-ttu-id="14f3c-128">Затенения.</span><span class="sxs-lookup"><span data-stu-id="14f3c-128">Predication.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14f3c-129">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="14f3c-129">vs_3_0</span></span></td>
<td><span data-ttu-id="14f3c-130">Компилировать до vs_3_0 версии.</span><span class="sxs-lookup"><span data-stu-id="14f3c-130">Compile to vs_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="14f3c-131">Дополнительные сведения о различиях между версиями шейдера см. в разделе [различия шейдеров вершин](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span><span class="sxs-lookup"><span data-stu-id="14f3c-131">For more information about the differences between shader versions, see [Vertex Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14f3c-132">Требования</span><span class="sxs-lookup"><span data-stu-id="14f3c-132">Requirements</span></span>



| <span data-ttu-id="14f3c-133">Требование</span><span class="sxs-lookup"><span data-stu-id="14f3c-133">Requirement</span></span> | <span data-ttu-id="14f3c-134">Значение</span><span class="sxs-lookup"><span data-stu-id="14f3c-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f3c-135">Header</span><span class="sxs-lookup"><span data-stu-id="14f3c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="14f3c-136"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="14f3c-136"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="14f3c-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14f3c-137">Library</span></span><br/> | <dl> <span data-ttu-id="14f3c-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14f3c-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="14f3c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14f3c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f3c-140">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="14f3c-140">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
