---
description: Интерфейс ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Интерфейс ID3DXTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664966"
---
# <a name="id3dxtextureshader-interface"></a><span data-ttu-id="be6ed-103">Интерфейс ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="be6ed-103">ID3DXTextureShader interface</span></span>

<span data-ttu-id="be6ed-104">Интерфейс ID3DXTextureShader.</span><span class="sxs-lookup"><span data-stu-id="be6ed-104">The ID3DXTextureShader interface.</span></span>

## <a name="members"></a><span data-ttu-id="be6ed-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="be6ed-105">Members</span></span>

<span data-ttu-id="be6ed-106">Интерфейс **ID3DXTextureShader** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="be6ed-106">The **ID3DXTextureShader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be6ed-107">**ID3DXTextureShader** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be6ed-107">**ID3DXTextureShader** also has these types of members:</span></span>

-   [<span data-ttu-id="be6ed-108">Методы</span><span class="sxs-lookup"><span data-stu-id="be6ed-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be6ed-109">Методы</span><span class="sxs-lookup"><span data-stu-id="be6ed-109">Methods</span></span>

<span data-ttu-id="be6ed-110">Интерфейс **ID3DXTextureShader** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="be6ed-110">The **ID3DXTextureShader** interface has these methods.</span></span>



| <span data-ttu-id="be6ed-111">Метод</span><span class="sxs-lookup"><span data-stu-id="be6ed-111">Method</span></span>                                                                                       | <span data-ttu-id="be6ed-112">Описание</span><span class="sxs-lookup"><span data-stu-id="be6ed-112">Description</span></span>                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="be6ed-113">**Константа**</span><span class="sxs-lookup"><span data-stu-id="be6ed-113">**GetConstant**</span></span>](id3dxtextureshader--getconstant.md)                                       | <span data-ttu-id="be6ed-114">Возвращает константу путем поиска своего индекса.</span><span class="sxs-lookup"><span data-stu-id="be6ed-114">Gets a constant by looking up its index.</span></span><br/>                         |
| [<span data-ttu-id="be6ed-115">**жетконстантбуффер**</span><span class="sxs-lookup"><span data-stu-id="be6ed-115">**GetConstantBuffer**</span></span>](id3dxtextureshader--getconstantbuffer.md)                           | <span data-ttu-id="be6ed-116">Возвращает указатель на таблицу констант.</span><span class="sxs-lookup"><span data-stu-id="be6ed-116">Get a pointer to the constant table.</span></span><br/>                             |
| [<span data-ttu-id="be6ed-117">**жетконстантбинаме**</span><span class="sxs-lookup"><span data-stu-id="be6ed-117">**GetConstantByName**</span></span>](id3dxtextureshader--getconstantbyname.md)                           | <span data-ttu-id="be6ed-118">Возвращает константу путем поиска ее имени.</span><span class="sxs-lookup"><span data-stu-id="be6ed-118">Gets a constant by looking up its name.</span></span><br/>                          |
| [<span data-ttu-id="be6ed-119">**жетконстантдеск**</span><span class="sxs-lookup"><span data-stu-id="be6ed-119">**GetConstantDesc**</span></span>](id3dxtextureshader--getconstantdesc.md)                               | <span data-ttu-id="be6ed-120">Возвращает указатель на массив констант в таблице констант.</span><span class="sxs-lookup"><span data-stu-id="be6ed-120">Gets a pointer to the array of constants in the constant table.</span></span><br/>  |
| [<span data-ttu-id="be6ed-121">**жетконстантелемент**</span><span class="sxs-lookup"><span data-stu-id="be6ed-121">**GetConstantElement**</span></span>](id3dxtextureshader--getconstantelement.md)                         | <span data-ttu-id="be6ed-122">Получить константу из таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="be6ed-122">Get a constant from the constant table.</span></span><br/>                          |
| [<span data-ttu-id="be6ed-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="be6ed-123">**GetDesc**</span></span>](id3dxtextureshader--getdesc.md)                                               | <span data-ttu-id="be6ed-124">Возвращает описание таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="be6ed-124">Gets a description of the constant table.</span></span><br/>                        |
| [<span data-ttu-id="be6ed-125">**GetFunction**</span><span class="sxs-lookup"><span data-stu-id="be6ed-125">**GetFunction**</span></span>](id3dxtextureshader--getfunction.md)                                       | <span data-ttu-id="be6ed-126">Возвращает указатель на поток функции DWORD.</span><span class="sxs-lookup"><span data-stu-id="be6ed-126">Gets a pointer to the function DWORD stream.</span></span><br/>                     |
| [<span data-ttu-id="be6ed-127">**сетбул**</span><span class="sxs-lookup"><span data-stu-id="be6ed-127">**SetBool**</span></span>](id3dxtextureshader--setbool.md)                                               | <span data-ttu-id="be6ed-128">Задает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="be6ed-128">Sets a BOOL value.</span></span><br/>                                               |
| [<span data-ttu-id="be6ed-129">**сетбуларрай**</span><span class="sxs-lookup"><span data-stu-id="be6ed-129">**SetBoolArray**</span></span>](id3dxtextureshader--setboolarray.md)                                     | <span data-ttu-id="be6ed-130">Задает массив значений типа BOOL.</span><span class="sxs-lookup"><span data-stu-id="be6ed-130">Sets an array of BOOL values.</span></span><br/>                                    |
| [<span data-ttu-id="be6ed-131">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="be6ed-131">**SetDefaults**</span></span>](id3dxtextureshader--setdefaults.md)                                       | <span data-ttu-id="be6ed-132">Устанавливает константы в значения по умолчанию, объявленные в шейдере.</span><span class="sxs-lookup"><span data-stu-id="be6ed-132">Sets the constants to the default values declared in the shader.</span></span><br/> |
| [<span data-ttu-id="be6ed-133">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="be6ed-133">**SetFloat**</span></span>](id3dxtextureshader--setfloat.md)                                             | <span data-ttu-id="be6ed-134">Задает число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="be6ed-134">Sets a floating-point number.</span></span><br/>                                    |
| [<span data-ttu-id="be6ed-135">**сетфлоатаррай**</span><span class="sxs-lookup"><span data-stu-id="be6ed-135">**SetFloatArray**</span></span>](id3dxtextureshader--setfloatarray.md)                                   | <span data-ttu-id="be6ed-136">Задает массив чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="be6ed-136">Sets an array of floating-point numbers.</span></span><br/>                         |
| [<span data-ttu-id="be6ed-137">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="be6ed-137">**SetInt**</span></span>](id3dxtextureshader--setint.md)                                                 | <span data-ttu-id="be6ed-138">Задает целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="be6ed-138">Sets an integer value.</span></span><br/>                                           |
| [<span data-ttu-id="be6ed-139">**сетинтаррай**</span><span class="sxs-lookup"><span data-stu-id="be6ed-139">**SetIntArray**</span></span>](id3dxtextureshader--setintarray.md)                                       | <span data-ttu-id="be6ed-140">Задает массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="be6ed-140">Sets an array of integers.</span></span><br/>                                       |
| [<span data-ttu-id="be6ed-141">**сетматрикс**</span><span class="sxs-lookup"><span data-stu-id="be6ed-141">**SetMatrix**</span></span>](id3dxtextureshader--setmatrix.md)                                           | <span data-ttu-id="be6ed-142">Задает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="be6ed-142">Sets a non-transposed matrix.</span></span><br/>                                    |
| [<span data-ttu-id="be6ed-143">**сетматриксаррай**</span><span class="sxs-lookup"><span data-stu-id="be6ed-143">**SetMatrixArray**</span></span>](id3dxtextureshader--setmatrixarray.md)                                 | <span data-ttu-id="be6ed-144">Задает массив нестандартных матриц.</span><span class="sxs-lookup"><span data-stu-id="be6ed-144">Sets an array of non-transposed matrices.</span></span><br/>                        |
| [<span data-ttu-id="be6ed-145">**сетматрикспоинтераррай**</span><span class="sxs-lookup"><span data-stu-id="be6ed-145">**SetMatrixPointerArray**</span></span>](id3dxtextureshader--setmatrixpointerarray.md)                   | <span data-ttu-id="be6ed-146">Задает массив указателей на нестандартные матрицы.</span><span class="sxs-lookup"><span data-stu-id="be6ed-146">Sets an array of pointers to non-transposed matrices.</span></span><br/>            |
| [<span data-ttu-id="be6ed-147">**сетматрикстранспосе**</span><span class="sxs-lookup"><span data-stu-id="be6ed-147">**SetMatrixTranspose**</span></span>](id3dxtextureshader--setmatrixtranspose.md)                         | <span data-ttu-id="be6ed-148">Задает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="be6ed-148">Sets a transposed matrix.</span></span><br/>                                        |
| [<span data-ttu-id="be6ed-149">**сетматрикстранспосеаррай**</span><span class="sxs-lookup"><span data-stu-id="be6ed-149">**SetMatrixTransposeArray**</span></span>](id3dxtextureshader--setmatrixtransposearray.md)               | <span data-ttu-id="be6ed-150">Задает массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="be6ed-150">Sets an array of transposed matrices.</span></span><br/>                            |
| [<span data-ttu-id="be6ed-151">**сетматрикстранспосепоинтераррай**</span><span class="sxs-lookup"><span data-stu-id="be6ed-151">**SetMatrixTransposePointerArray**</span></span>](id3dxtextureshader--setmatrixtransposepointerarray.md) | <span data-ttu-id="be6ed-152">Задает массив указателей на перекладываемые матрицы.</span><span class="sxs-lookup"><span data-stu-id="be6ed-152">Sets an array of pointers to transposed matrices.</span></span><br/>                |
| [<span data-ttu-id="be6ed-153">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="be6ed-153">**SetValue**</span></span>](id3dxtextureshader--setvalue.md)                                             | <span data-ttu-id="be6ed-154">Задает таблицу констант с данными в буфере.</span><span class="sxs-lookup"><span data-stu-id="be6ed-154">Sets the constant table with the data in the buffer.</span></span><br/>             |
| [<span data-ttu-id="be6ed-155">**сетвектор**</span><span class="sxs-lookup"><span data-stu-id="be6ed-155">**SetVector**</span></span>](id3dxtextureshader--setvector.md)                                           | <span data-ttu-id="be6ed-156">Задает вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="be6ed-156">Sets a 4D vector.</span></span><br/>                                                |
| [<span data-ttu-id="be6ed-157">**сетвектораррай**</span><span class="sxs-lookup"><span data-stu-id="be6ed-157">**SetVectorArray**</span></span>](id3dxtextureshader--setvectorarray.md)                                 | <span data-ttu-id="be6ed-158">Задает массив векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="be6ed-158">Sets an array of 4D vectors.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="be6ed-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be6ed-159">Remarks</span></span>

<span data-ttu-id="be6ed-160">Интерфейс **ID3DXTextureShader** получается путем вызова функции [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="be6ed-160">The **ID3DXTextureShader** interface is obtained by calling the [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) function.</span></span>

<span data-ttu-id="be6ed-161">Интерфейс **ID3DXTextureShader** , как и все COM-интерфейсы, наследует интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="be6ed-161">The **ID3DXTextureShader** interface, like all COM interfaces, inherits the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

<span data-ttu-id="be6ed-162">Тип LPD3DXTEXTURESHADER определяется как указатель на интерфейс **ID3DXTextureShader** .</span><span class="sxs-lookup"><span data-stu-id="be6ed-162">The LPD3DXTEXTURESHADER type is defined as a pointer to the **ID3DXTextureShader** interface.</span></span>


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a><span data-ttu-id="be6ed-163">Требования</span><span class="sxs-lookup"><span data-stu-id="be6ed-163">Requirements</span></span>



| <span data-ttu-id="be6ed-164">Требование</span><span class="sxs-lookup"><span data-stu-id="be6ed-164">Requirement</span></span> | <span data-ttu-id="be6ed-165">Значение</span><span class="sxs-lookup"><span data-stu-id="be6ed-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be6ed-166">Header</span><span class="sxs-lookup"><span data-stu-id="be6ed-166">Header</span></span><br/>  | <dl> <span data-ttu-id="be6ed-167"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="be6ed-167"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="be6ed-168">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be6ed-168">Library</span></span><br/> | <dl> <span data-ttu-id="be6ed-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be6ed-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="be6ed-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be6ed-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6ed-171">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="be6ed-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
