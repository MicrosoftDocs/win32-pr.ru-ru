---
title: Интерфейс ID3DX11EffectVectorVariable (D3dx11effect. h)
description: Интерфейс векторной переменной обращается к вектору из четырех компонентов.
ms.assetid: 191d373b-0562-4d7b-ac3f-cd24abf259bc
keywords:
- Интерфейс ID3DX11EffectVectorVariable Direct3D 11
- Интерфейс ID3DX11EffectVectorVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9235a4047617dd2e5ff9f14925908ae7a0dc1060
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998294"
---
# <a name="id3dx11effectvectorvariable-interface"></a><span data-ttu-id="73252-105">Интерфейс ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="73252-105">ID3DX11EffectVectorVariable interface</span></span>

<span data-ttu-id="73252-106">Интерфейс векторной переменной обращается к вектору из четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="73252-106">A vector-variable interface accesses a four-component vector.</span></span>

## <a name="members"></a><span data-ttu-id="73252-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="73252-107">Members</span></span>

<span data-ttu-id="73252-108">Интерфейс **ID3DX11EffectVectorVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="73252-108">The **ID3DX11EffectVectorVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="73252-109">**ID3DX11EffectVectorVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="73252-109">**ID3DX11EffectVectorVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="73252-110">Методы</span><span class="sxs-lookup"><span data-stu-id="73252-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="73252-111">Методы</span><span class="sxs-lookup"><span data-stu-id="73252-111">Methods</span></span>

<span data-ttu-id="73252-112">Интерфейс **ID3DX11EffectVectorVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="73252-112">The **ID3DX11EffectVectorVariable** interface has these methods.</span></span>



| <span data-ttu-id="73252-113">Метод</span><span class="sxs-lookup"><span data-stu-id="73252-113">Method</span></span>                                                                         | <span data-ttu-id="73252-114">Описание</span><span class="sxs-lookup"><span data-stu-id="73252-114">Description</span></span>                                                                         |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="73252-115">**жетбулвектор**</span><span class="sxs-lookup"><span data-stu-id="73252-115">**GetBoolVector**</span></span>](id3dx11effectvectorvariable-getboolvector.md)             | <span data-ttu-id="73252-116">Получение вектора из четырех компонентов, содержащего логические данные.</span><span class="sxs-lookup"><span data-stu-id="73252-116">Get a four-component vector that contains boolean data.</span></span><br/>                  |
| [<span data-ttu-id="73252-117">**жетбулвектораррай**</span><span class="sxs-lookup"><span data-stu-id="73252-117">**GetBoolVectorArray**</span></span>](id3dx11effectvectorvariable-getboolvectorarray.md)   | <span data-ttu-id="73252-118">Получение массива векторов из четырех компонентов, содержащих логические данные.</span><span class="sxs-lookup"><span data-stu-id="73252-118">Get an array of four-component vectors that contain boolean data.</span></span><br/>        |
| [<span data-ttu-id="73252-119">**жетфлоатвектор**</span><span class="sxs-lookup"><span data-stu-id="73252-119">**GetFloatVector**</span></span>](id3dx11effectvectorvariable-getfloatvector.md)           | <span data-ttu-id="73252-120">Получение вектора из четырех компонентов, содержащего данные с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="73252-120">Get a four-component vector that contains floating-point data.</span></span><br/>           |
| [<span data-ttu-id="73252-121">**жетфлоатвектораррай**</span><span class="sxs-lookup"><span data-stu-id="73252-121">**GetFloatVectorArray**</span></span>](id3dx11effectvectorvariable-getfloatvectorarray.md) | <span data-ttu-id="73252-122">Получите массив векторов из четырех компонентов, содержащих данные с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="73252-122">Get an array of four-component vectors that contain floating-point data.</span></span><br/> |
| [<span data-ttu-id="73252-123">**жетинтвектор**</span><span class="sxs-lookup"><span data-stu-id="73252-123">**GetIntVector**</span></span>](id3dx11effectvectorvariable-getintvector.md)               | <span data-ttu-id="73252-124">Получение вектора из четырех компонентов, содержащего целочисленные данные.</span><span class="sxs-lookup"><span data-stu-id="73252-124">Get a four-component vector that contains integer data.</span></span><br/>                  |
| [<span data-ttu-id="73252-125">**жетинтвектораррай**</span><span class="sxs-lookup"><span data-stu-id="73252-125">**GetIntVectorArray**</span></span>](id3dx11effectvectorvariable-getintvectorarray.md)     | <span data-ttu-id="73252-126">Получение массива векторов из четырех компонентов, содержащих целочисленные данные.</span><span class="sxs-lookup"><span data-stu-id="73252-126">Get an array of four-component vectors that contain integer data.</span></span><br/>        |
| [<span data-ttu-id="73252-127">**сетбулвектор**</span><span class="sxs-lookup"><span data-stu-id="73252-127">**SetBoolVector**</span></span>](id3dx11effectvectorvariable-setboolvector.md)             | <span data-ttu-id="73252-128">Установите вектор с четырьмя компонентами, содержащий логические данные.</span><span class="sxs-lookup"><span data-stu-id="73252-128">Set a four-component vector that contains boolean data.</span></span><br/>                  |
| [<span data-ttu-id="73252-129">**сетбулвектораррай**</span><span class="sxs-lookup"><span data-stu-id="73252-129">**SetBoolVectorArray**</span></span>](id3dx11effectvectorvariable-setboolvectorarray.md)   | <span data-ttu-id="73252-130">Установите массив векторов из четырех компонентов, содержащих логические данные.</span><span class="sxs-lookup"><span data-stu-id="73252-130">Set an array of four-component vectors that contain boolean data.</span></span><br/>        |
| [<span data-ttu-id="73252-131">**сетфлоатвектор**</span><span class="sxs-lookup"><span data-stu-id="73252-131">**SetFloatVector**</span></span>](id3dx11effectvectorvariable-setfloatvector.md)           | <span data-ttu-id="73252-132">Установите вектор с четырьмя компонентами, содержащий данные с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="73252-132">Set a four-component vector that contains floating-point data.</span></span><br/>           |
| [<span data-ttu-id="73252-133">**сетфлоатвектораррай**</span><span class="sxs-lookup"><span data-stu-id="73252-133">**SetFloatVectorArray**</span></span>](id3dx11effectvectorvariable-setfloatvectorarray.md) | <span data-ttu-id="73252-134">Установите массив векторов из четырех компонентов, содержащих данные с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="73252-134">Set an array of four-component vectors that contain floating-point data.</span></span><br/> |
| [<span data-ttu-id="73252-135">**сетинтвектор**</span><span class="sxs-lookup"><span data-stu-id="73252-135">**SetIntVector**</span></span>](id3dx11effectvectorvariable-setintvector.md)               | <span data-ttu-id="73252-136">Установите вектор с четырьмя компонентами, который содержит целочисленные данные.</span><span class="sxs-lookup"><span data-stu-id="73252-136">Set a four-component vector that contains integer data.</span></span><br/>                  |
| [<span data-ttu-id="73252-137">**сетинтвектораррай**</span><span class="sxs-lookup"><span data-stu-id="73252-137">**SetIntVectorArray**</span></span>](id3dx11effectvectorvariable-setintvectorarray.md)     | <span data-ttu-id="73252-138">Установите массив векторов из четырех компонентов, содержащих целочисленные данные.</span><span class="sxs-lookup"><span data-stu-id="73252-138">Set an array of four-component vectors that contain integer data.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="73252-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="73252-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="73252-140">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="73252-140">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="73252-141">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="73252-141">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="73252-142">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="73252-142">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73252-143">Требования</span><span class="sxs-lookup"><span data-stu-id="73252-143">Requirements</span></span>



| <span data-ttu-id="73252-144">Требование</span><span class="sxs-lookup"><span data-stu-id="73252-144">Requirement</span></span> | <span data-ttu-id="73252-145">Значение</span><span class="sxs-lookup"><span data-stu-id="73252-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73252-146">Header</span><span class="sxs-lookup"><span data-stu-id="73252-146">Header</span></span><br/>  | <dl> <span data-ttu-id="73252-147"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="73252-147"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="73252-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73252-148">Library</span></span><br/> | <dl> <span data-ttu-id="73252-149"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="73252-149"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73252-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73252-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73252-151">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="73252-151">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="73252-152">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="73252-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="73252-153">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="73252-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





