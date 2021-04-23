---
description: Интерфейс ID3DXConstantTable используется для доступа к таблице констант. Эта таблица содержит переменные, используемые в высокоуровневой шейдере и эффектах языка.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Интерфейс ID3DXConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713725"
---
# <a name="id3dxconstanttable-interface"></a><span data-ttu-id="d9058-104">Интерфейс ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="d9058-104">ID3DXConstantTable interface</span></span>

<span data-ttu-id="d9058-105">Интерфейс ID3DXConstantTable используется для доступа к таблице констант.</span><span class="sxs-lookup"><span data-stu-id="d9058-105">The ID3DXConstantTable interface is used to access the constant table.</span></span> <span data-ttu-id="d9058-106">Эта таблица содержит переменные, используемые в высокоуровневой шейдере и эффектах языка.</span><span class="sxs-lookup"><span data-stu-id="d9058-106">This table contains the variables that are used by high-level language shaders and effects.</span></span>

## <a name="members"></a><span data-ttu-id="d9058-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="d9058-107">Members</span></span>

<span data-ttu-id="d9058-108">Интерфейс **ID3DXConstantTable** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d9058-108">The **ID3DXConstantTable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d9058-109">**ID3DXConstantTable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d9058-109">**ID3DXConstantTable** also has these types of members:</span></span>

-   [<span data-ttu-id="d9058-110">Методы</span><span class="sxs-lookup"><span data-stu-id="d9058-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d9058-111">Методы</span><span class="sxs-lookup"><span data-stu-id="d9058-111">Methods</span></span>

<span data-ttu-id="d9058-112">Интерфейс **ID3DXConstantTable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d9058-112">The **ID3DXConstantTable** interface has these methods.</span></span>



| <span data-ttu-id="d9058-113">Метод</span><span class="sxs-lookup"><span data-stu-id="d9058-113">Method</span></span>                                                                                       | <span data-ttu-id="d9058-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d9058-114">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9058-115">**жетбуфферпоинтер**</span><span class="sxs-lookup"><span data-stu-id="d9058-115">**GetBufferPointer**</span></span>](id3dxconstanttable--getbufferpointer.md)                             | <span data-ttu-id="d9058-116">Возвращает указатель на буфер, содержащий таблицу констант.</span><span class="sxs-lookup"><span data-stu-id="d9058-116">Gets a pointer to the buffer that contains the constant table.</span></span><br/>                                                          |
| [<span data-ttu-id="d9058-117">**жетбуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="d9058-117">**GetBufferSize**</span></span>](id3dxconstanttable--getbuffersize.md)                                   | <span data-ttu-id="d9058-118">Возвращает размер буфера таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="d9058-118">Gets the buffer size of the constant table.</span></span><br/>                                                                             |
| [<span data-ttu-id="d9058-119">**Константа**</span><span class="sxs-lookup"><span data-stu-id="d9058-119">**GetConstant**</span></span>](id3dxconstanttable--getconstant.md)                                       | <span data-ttu-id="d9058-120">Возвращает константу путем поиска своего индекса.</span><span class="sxs-lookup"><span data-stu-id="d9058-120">Gets a constant by looking up its index.</span></span><br/>                                                                                |
| [<span data-ttu-id="d9058-121">**жетконстантбинаме**</span><span class="sxs-lookup"><span data-stu-id="d9058-121">**GetConstantByName**</span></span>](id3dxconstanttable--getconstantbyname.md)                           | <span data-ttu-id="d9058-122">Возвращает константу путем поиска ее имени.</span><span class="sxs-lookup"><span data-stu-id="d9058-122">Gets a constant by looking up its name.</span></span><br/>                                                                                 |
| [<span data-ttu-id="d9058-123">**жетконстантдеск**</span><span class="sxs-lookup"><span data-stu-id="d9058-123">**GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)                               | <span data-ttu-id="d9058-124">Возвращает указатель на массив константных описаний в таблице констант.</span><span class="sxs-lookup"><span data-stu-id="d9058-124">Gets a pointer to an array of constant descriptions in the constant table.</span></span><br/>                                              |
| [<span data-ttu-id="d9058-125">**жетконстантелемент**</span><span class="sxs-lookup"><span data-stu-id="d9058-125">**GetConstantElement**</span></span>](id3dxconstanttable--getconstantelement.md)                         | <span data-ttu-id="d9058-126">Возвращает константу из массива констант.</span><span class="sxs-lookup"><span data-stu-id="d9058-126">Gets a constant from an array of constants.</span></span> <span data-ttu-id="d9058-127">Массив состоит из элементов.</span><span class="sxs-lookup"><span data-stu-id="d9058-127">An array is made up of elements.</span></span><br/>                                            |
| [<span data-ttu-id="d9058-128">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="d9058-128">**GetDesc**</span></span>](id3dxconstanttable--getdesc.md)                                               | <span data-ttu-id="d9058-129">Возвращает описание таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="d9058-129">Gets a description of the constant table.</span></span><br/>                                                                               |
| [<span data-ttu-id="d9058-130">**жетсамплериндекс**</span><span class="sxs-lookup"><span data-stu-id="d9058-130">**GetSamplerIndex**</span></span>](id3dxconstanttable--getsamplerindex.md)                               | <span data-ttu-id="d9058-131">Возвращает индекс образца.</span><span class="sxs-lookup"><span data-stu-id="d9058-131">Returns the sampler index.</span></span><br/>                                                                                              |
| [<span data-ttu-id="d9058-132">**сетбул**</span><span class="sxs-lookup"><span data-stu-id="d9058-132">**SetBool**</span></span>](id3dxconstanttable--setbool.md)                                               | <span data-ttu-id="d9058-133">Задает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="d9058-133">Sets a Boolean value.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="d9058-134">**сетбуларрай**</span><span class="sxs-lookup"><span data-stu-id="d9058-134">**SetBoolArray**</span></span>](id3dxconstanttable--setboolarray.md)                                     | <span data-ttu-id="d9058-135">Задает массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="d9058-135">Sets an array of Boolean values.</span></span><br/>                                                                                        |
| [<span data-ttu-id="d9058-136">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="d9058-136">**SetDefaults**</span></span>](id3dxconstanttable--setdefaults.md)                                       | <span data-ttu-id="d9058-137">Устанавливает константы в значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d9058-137">Sets the constants to their default values.</span></span> <span data-ttu-id="d9058-138">Значения по умолчанию объявляются в объявлениях переменных в шейдере.</span><span class="sxs-lookup"><span data-stu-id="d9058-138">The default values are declared in the variable declarations in the shader.</span></span><br/> |
| [<span data-ttu-id="d9058-139">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="d9058-139">**SetFloat**</span></span>](id3dxconstanttable--setfloat.md)                                             | <span data-ttu-id="d9058-140">Задает число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d9058-140">Sets a floating-point number.</span></span><br/>                                                                                           |
| [<span data-ttu-id="d9058-141">**сетфлоатаррай**</span><span class="sxs-lookup"><span data-stu-id="d9058-141">**SetFloatArray**</span></span>](id3dxconstanttable--setfloatarray.md)                                   | <span data-ttu-id="d9058-142">Задает массив чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d9058-142">Sets an array of floating-point numbers.</span></span><br/>                                                                                |
| [<span data-ttu-id="d9058-143">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="d9058-143">**SetInt**</span></span>](id3dxconstanttable--setint.md)                                                 | <span data-ttu-id="d9058-144">Задает целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="d9058-144">Sets an integer value.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="d9058-145">**сетинтаррай**</span><span class="sxs-lookup"><span data-stu-id="d9058-145">**SetIntArray**</span></span>](id3dxconstanttable--setintarray.md)                                       | <span data-ttu-id="d9058-146">Задает массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="d9058-146">Sets an array of integers.</span></span><br/>                                                                                              |
| [<span data-ttu-id="d9058-147">**сетматрикс**</span><span class="sxs-lookup"><span data-stu-id="d9058-147">**SetMatrix**</span></span>](id3dxconstanttable--setmatrix.md)                                           | <span data-ttu-id="d9058-148">Задает матрицу нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="d9058-148">Sets a nontransposed matrix.</span></span><br/>                                                                                            |
| [<span data-ttu-id="d9058-149">**сетматриксаррай**</span><span class="sxs-lookup"><span data-stu-id="d9058-149">**SetMatrixArray**</span></span>](id3dxconstanttable--setmatrixarray.md)                                 | <span data-ttu-id="d9058-150">Задает массив матриц нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="d9058-150">Sets an array of nontransposed matrices.</span></span><br/>                                                                                |
| [<span data-ttu-id="d9058-151">**сетматрикспоинтераррай**</span><span class="sxs-lookup"><span data-stu-id="d9058-151">**SetMatrixPointerArray**</span></span>](id3dxconstanttable--setmatrixpointerarray.md)                   | <span data-ttu-id="d9058-152">Задает массив указателей для нонтранспосед матриц.</span><span class="sxs-lookup"><span data-stu-id="d9058-152">Sets an array of pointers to nontransposed matrices.</span></span><br/>                                                                    |
| [<span data-ttu-id="d9058-153">**сетматрикстранспосе**</span><span class="sxs-lookup"><span data-stu-id="d9058-153">**SetMatrixTranspose**</span></span>](id3dxconstanttable--setmatrixtranspose.md)                         | <span data-ttu-id="d9058-154">Задает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="d9058-154">Sets a transposed matrix.</span></span><br/>                                                                                               |
| [<span data-ttu-id="d9058-155">**сетматрикстранспосеаррай**</span><span class="sxs-lookup"><span data-stu-id="d9058-155">**SetMatrixTransposeArray**</span></span>](id3dxconstanttable--setmatrixtransposearray.md)               | <span data-ttu-id="d9058-156">Задает массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="d9058-156">Sets an array of transposed matrices.</span></span><br/>                                                                                   |
| [<span data-ttu-id="d9058-157">**сетматрикстранспосепоинтераррай**</span><span class="sxs-lookup"><span data-stu-id="d9058-157">**SetMatrixTransposePointerArray**</span></span>](id3dxconstanttable--setmatrixtransposepointerarray.md) | <span data-ttu-id="d9058-158">Задает массив указателей на перекладываемые матрицы.</span><span class="sxs-lookup"><span data-stu-id="d9058-158">Sets an array of pointers to transposed matrices.</span></span><br/>                                                                       |
| [<span data-ttu-id="d9058-159">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="d9058-159">**SetValue**</span></span>](id3dxconstanttable--setvalue.md)                                             | <span data-ttu-id="d9058-160">Устанавливает содержимое буфера в таблицу констант.</span><span class="sxs-lookup"><span data-stu-id="d9058-160">Sets the contents of the buffer to the constant table.</span></span><br/>                                                                  |
| [<span data-ttu-id="d9058-161">**сетвектор**</span><span class="sxs-lookup"><span data-stu-id="d9058-161">**SetVector**</span></span>](id3dxconstanttable--setvector.md)                                           | <span data-ttu-id="d9058-162">Задает вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="d9058-162">Sets a 4D vector.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="d9058-163">**сетвектораррай**</span><span class="sxs-lookup"><span data-stu-id="d9058-163">**SetVectorArray**</span></span>](id3dxconstanttable--setvectorarray.md)                                 | <span data-ttu-id="d9058-164">Задает массив векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="d9058-164">Sets an array of 4D vectors.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="d9058-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9058-165">Remarks</span></span>

<span data-ttu-id="d9058-166">Тип LPD3DXCONSTANTTABLE определяется как указатель на интерфейс **ID3DXConstantTable** .</span><span class="sxs-lookup"><span data-stu-id="d9058-166">The LPD3DXCONSTANTTABLE type is defined as a pointer to the **ID3DXConstantTable** interface.</span></span>


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a><span data-ttu-id="d9058-167">Требования</span><span class="sxs-lookup"><span data-stu-id="d9058-167">Requirements</span></span>



| <span data-ttu-id="d9058-168">Требование</span><span class="sxs-lookup"><span data-stu-id="d9058-168">Requirement</span></span> | <span data-ttu-id="d9058-169">Значение</span><span class="sxs-lookup"><span data-stu-id="d9058-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9058-170">Header</span><span class="sxs-lookup"><span data-stu-id="d9058-170">Header</span></span><br/>  | <dl> <span data-ttu-id="d9058-171"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9058-171"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d9058-172">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9058-172">Library</span></span><br/> | <dl> <span data-ttu-id="d9058-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9058-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d9058-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9058-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9058-175">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="d9058-175">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
