---
title: Интерфейс ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Интерфейс с скалярными переменными получает доступ к скалярным значениям.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d07f0d14ce37f9c84c20564189e1b8475e69887
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273710"
---
# <a name="id3dx11effectscalarvariable-interface"></a><span data-ttu-id="72f55-105">Интерфейс ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="72f55-105">ID3DX11EffectScalarVariable interface</span></span>

<span data-ttu-id="72f55-106">Интерфейс с скалярными переменными получает доступ к скалярным значениям.</span><span class="sxs-lookup"><span data-stu-id="72f55-106">An effect-scalar-variable interface accesses scalar values.</span></span>

## <a name="members"></a><span data-ttu-id="72f55-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="72f55-107">Members</span></span>

<span data-ttu-id="72f55-108">Интерфейс **ID3DX11EffectScalarVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="72f55-108">The **ID3DX11EffectScalarVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="72f55-109">**ID3DX11EffectScalarVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="72f55-109">**ID3DX11EffectScalarVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="72f55-110">Методы</span><span class="sxs-lookup"><span data-stu-id="72f55-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="72f55-111">Методы</span><span class="sxs-lookup"><span data-stu-id="72f55-111">Methods</span></span>

<span data-ttu-id="72f55-112">Интерфейс **ID3DX11EffectScalarVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="72f55-112">The **ID3DX11EffectScalarVariable** interface has these methods.</span></span>



| <span data-ttu-id="72f55-113">Метод</span><span class="sxs-lookup"><span data-stu-id="72f55-113">Method</span></span>                                                             | <span data-ttu-id="72f55-114">Описание</span><span class="sxs-lookup"><span data-stu-id="72f55-114">Description</span></span>                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="72f55-115">**Bool**</span><span class="sxs-lookup"><span data-stu-id="72f55-115">**GetBool**</span></span>](id3dx11effectscalarvariable-getbool.md)             | <span data-ttu-id="72f55-116">Получить логическую переменную.</span><span class="sxs-lookup"><span data-stu-id="72f55-116">Get a boolean variable.</span></span><br/>                   |
| [<span data-ttu-id="72f55-117">**жетбуларрай**</span><span class="sxs-lookup"><span data-stu-id="72f55-117">**GetBoolArray**</span></span>](id3dx11effectscalarvariable-getboolarray.md)   | <span data-ttu-id="72f55-118">Получение массива логических переменных.</span><span class="sxs-lookup"><span data-stu-id="72f55-118">Get an array of boolean variables.</span></span><br/>        |
| [<span data-ttu-id="72f55-119">**GetFloat**</span><span class="sxs-lookup"><span data-stu-id="72f55-119">**GetFloat**</span></span>](id3dx11effectscalarvariable-getfloat.md)           | <span data-ttu-id="72f55-120">Получение переменной с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="72f55-120">Get a floating-point variable.</span></span><br/>            |
| [<span data-ttu-id="72f55-121">**жетфлоатаррай**</span><span class="sxs-lookup"><span data-stu-id="72f55-121">**GetFloatArray**</span></span>](id3dx11effectscalarvariable-getfloatarray.md) | <span data-ttu-id="72f55-122">Получение массива переменных с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="72f55-122">Get an array of floating-point variables.</span></span><br/> |
| [<span data-ttu-id="72f55-123">**GetInt**</span><span class="sxs-lookup"><span data-stu-id="72f55-123">**GetInt**</span></span>](id3dx11effectscalarvariable-getint.md)               | <span data-ttu-id="72f55-124">Получение целочисленной переменной.</span><span class="sxs-lookup"><span data-stu-id="72f55-124">Get an integer variable.</span></span><br/>                  |
| [<span data-ttu-id="72f55-125">**жетинтаррай**</span><span class="sxs-lookup"><span data-stu-id="72f55-125">**GetIntArray**</span></span>](id3dx11effectscalarvariable-getintarray.md)     | <span data-ttu-id="72f55-126">Получение массива целочисленных переменных.</span><span class="sxs-lookup"><span data-stu-id="72f55-126">Get an array of integer variables.</span></span><br/>        |
| [<span data-ttu-id="72f55-127">**сетбул**</span><span class="sxs-lookup"><span data-stu-id="72f55-127">**SetBool**</span></span>](id3dx11effectscalarvariable-setbool.md)             | <span data-ttu-id="72f55-128">Задайте логическую переменную.</span><span class="sxs-lookup"><span data-stu-id="72f55-128">Set a boolean variable.</span></span><br/>                   |
| [<span data-ttu-id="72f55-129">**сетбуларрай**</span><span class="sxs-lookup"><span data-stu-id="72f55-129">**SetBoolArray**</span></span>](id3dx11effectscalarvariable-setboolarray.md)   | <span data-ttu-id="72f55-130">Задайте массив логических переменных.</span><span class="sxs-lookup"><span data-stu-id="72f55-130">Set an array of boolean variables.</span></span><br/>        |
| [<span data-ttu-id="72f55-131">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="72f55-131">**SetFloat**</span></span>](id3dx11effectscalarvariable-setfloat.md)           | <span data-ttu-id="72f55-132">Задайте переменную с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="72f55-132">Set a floating-point variable.</span></span><br/>            |
| [<span data-ttu-id="72f55-133">**сетфлоатаррай**</span><span class="sxs-lookup"><span data-stu-id="72f55-133">**SetFloatArray**</span></span>](id3dx11effectscalarvariable-setfloatarray.md) | <span data-ttu-id="72f55-134">Задайте массив переменных с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="72f55-134">Set an array of floating-point variables.</span></span><br/> |
| [<span data-ttu-id="72f55-135">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="72f55-135">**SetInt**</span></span>](id3dx11effectscalarvariable-setint.md)               | <span data-ttu-id="72f55-136">Задайте целочисленную переменную.</span><span class="sxs-lookup"><span data-stu-id="72f55-136">Set an integer variable.</span></span><br/>                  |
| [<span data-ttu-id="72f55-137">**сетинтаррай**</span><span class="sxs-lookup"><span data-stu-id="72f55-137">**SetIntArray**</span></span>](id3dx11effectscalarvariable-setintarray.md)     | <span data-ttu-id="72f55-138">Задайте массив целочисленных переменных.</span><span class="sxs-lookup"><span data-stu-id="72f55-138">Set an array of integer variables.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="72f55-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="72f55-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="72f55-140">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="72f55-140">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="72f55-141">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="72f55-141">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="72f55-142">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="72f55-142">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72f55-143">Требования</span><span class="sxs-lookup"><span data-stu-id="72f55-143">Requirements</span></span>



| <span data-ttu-id="72f55-144">Требование</span><span class="sxs-lookup"><span data-stu-id="72f55-144">Requirement</span></span> | <span data-ttu-id="72f55-145">Значение</span><span class="sxs-lookup"><span data-stu-id="72f55-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f55-146">Header</span><span class="sxs-lookup"><span data-stu-id="72f55-146">Header</span></span><br/>  | <dl> <span data-ttu-id="72f55-147"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f55-147"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="72f55-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72f55-148">Library</span></span><br/> | <dl> <span data-ttu-id="72f55-149"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="72f55-149"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72f55-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72f55-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f55-151">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="72f55-151">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="72f55-152">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="72f55-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="72f55-153">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="72f55-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





