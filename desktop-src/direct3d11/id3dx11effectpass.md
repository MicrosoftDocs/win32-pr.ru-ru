---
title: Интерфейс ID3DX11EffectPass (D3dx11effect. h)
description: Интерфейс ID3DX11EffectPass инкапсулирует назначения состояний в рамках метода. Время существования объекта ID3DX11EffectPass равно времени существования родительского объекта ID3DX11Effect.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Интерфейс ID3DX11EffectPass Direct3D 11
- Интерфейс ID3DX11EffectPass Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273912"
---
# <a name="id3dx11effectpass-interface"></a><span data-ttu-id="bef17-105">Интерфейс ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="bef17-105">ID3DX11EffectPass interface</span></span>

<span data-ttu-id="bef17-106">Интерфейс **ID3DX11EffectPass** инкапсулирует назначения состояний в рамках метода.</span><span class="sxs-lookup"><span data-stu-id="bef17-106">An **ID3DX11EffectPass** interface encapsulates state assignments within a technique.</span></span>

<span data-ttu-id="bef17-107">Время существования объекта **ID3DX11EffectPass** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .</span><span class="sxs-lookup"><span data-stu-id="bef17-107">The lifetime of an **ID3DX11EffectPass** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="bef17-108">Методы</span><span class="sxs-lookup"><span data-stu-id="bef17-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bef17-109">Методы</span><span class="sxs-lookup"><span data-stu-id="bef17-109">Methods</span></span>

<span data-ttu-id="bef17-110">Интерфейс **ID3DX11EffectPass** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bef17-110">The **ID3DX11EffectPass** interface has these methods.</span></span>



| <span data-ttu-id="bef17-111">Метод</span><span class="sxs-lookup"><span data-stu-id="bef17-111">Method</span></span>                                                                   | <span data-ttu-id="bef17-112">Описание</span><span class="sxs-lookup"><span data-stu-id="bef17-112">Description</span></span>                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="bef17-113">**Применить**</span><span class="sxs-lookup"><span data-stu-id="bef17-113">**Apply**</span></span>](id3dx11effectpass-apply.md)                                 | <span data-ttu-id="bef17-114">Задайте состояние, которое содержится в передаче на устройство.</span><span class="sxs-lookup"><span data-stu-id="bef17-114">Set the state contained in a pass to the device.</span></span><br/>       |
| [<span data-ttu-id="bef17-115">**компутестатеблоккмаск**</span><span class="sxs-lookup"><span data-stu-id="bef17-115">**ComputeStateBlockMask**</span></span>](id3dx11effectpass-computestateblockmask.md) | <span data-ttu-id="bef17-116">Создание маски для разрешения или запрета изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="bef17-116">Generate a mask for allowing/preventing state changes.</span></span><br/> |
| [<span data-ttu-id="bef17-117">**жетаннотатионбиндекс**</span><span class="sxs-lookup"><span data-stu-id="bef17-117">**GetAnnotationByIndex**</span></span>](id3dx11effectpass-getannotationbyindex.md)   | <span data-ttu-id="bef17-118">Получение заметки по индексу.</span><span class="sxs-lookup"><span data-stu-id="bef17-118">Get an annotation by index.</span></span><br/>                            |
| [<span data-ttu-id="bef17-119">**жетаннотатионбинаме**</span><span class="sxs-lookup"><span data-stu-id="bef17-119">**GetAnnotationByName**</span></span>](id3dx11effectpass-getannotationbyname.md)     | <span data-ttu-id="bef17-120">Получение заметки по имени.</span><span class="sxs-lookup"><span data-stu-id="bef17-120">Get an annotation by name.</span></span><br/>                             |
| [<span data-ttu-id="bef17-121">**жеткомпутешадердеск**</span><span class="sxs-lookup"><span data-stu-id="bef17-121">**GetComputeShaderDesc**</span></span>](id3dx11effectpass-getcomputeshaderdesc.md)   | <span data-ttu-id="bef17-122">Получение описания вычислений для шейдера.</span><span class="sxs-lookup"><span data-stu-id="bef17-122">Get a compute-shader description.</span></span><br/>                      |
| [<span data-ttu-id="bef17-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="bef17-123">**GetDesc**</span></span>](id3dx11effectpass-getdesc.md)                             | <span data-ttu-id="bef17-124">Получите описание этапа.</span><span class="sxs-lookup"><span data-stu-id="bef17-124">Get a pass description.</span></span><br/>                                |
| [<span data-ttu-id="bef17-125">**жетдомаиншадердеск**</span><span class="sxs-lookup"><span data-stu-id="bef17-125">**GetDomainShaderDesc**</span></span>](id3dx11effectpass-getdomainshaderdesc.md)     | <span data-ttu-id="bef17-126">Получите описание шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="bef17-126">Get a domain-shader description.</span></span><br/>                       |
| [<span data-ttu-id="bef17-127">**жетжеометришадердеск**</span><span class="sxs-lookup"><span data-stu-id="bef17-127">**GetGeometryShaderDesc**</span></span>](id3dx11effectpass-getgeometryshaderdesc.md) | <span data-ttu-id="bef17-128">Получите описание геометрического шейдера.</span><span class="sxs-lookup"><span data-stu-id="bef17-128">Get a geometry-shader description.</span></span><br/>                     |
| [<span data-ttu-id="bef17-129">**жесуллшадердеск**</span><span class="sxs-lookup"><span data-stu-id="bef17-129">**GetHullShaderDesc**</span></span>](id3dx11effectpass-gethullshaderdesc.md)         | <span data-ttu-id="bef17-130">Получение описания поверхности-шейдера.</span><span class="sxs-lookup"><span data-stu-id="bef17-130">Get hull-shader description.</span></span><br/>                           |
| [<span data-ttu-id="bef17-131">**жетпикселшадердеск**</span><span class="sxs-lookup"><span data-stu-id="bef17-131">**GetPixelShaderDesc**</span></span>](id3dx11effectpass-getpixelshaderdesc.md)       | <span data-ttu-id="bef17-132">Получите описание пиксельного шейдера.</span><span class="sxs-lookup"><span data-stu-id="bef17-132">Get a pixel-shader description.</span></span><br/>                        |
| [<span data-ttu-id="bef17-133">**жетвертексшадердеск**</span><span class="sxs-lookup"><span data-stu-id="bef17-133">**GetVertexShaderDesc**</span></span>](id3dx11effectpass-getvertexshaderdesc.md)     | <span data-ttu-id="bef17-134">Получите описание вершинного шейдера.</span><span class="sxs-lookup"><span data-stu-id="bef17-134">Get a vertex-shader description.</span></span><br/>                       |
| [<span data-ttu-id="bef17-135">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="bef17-135">**IsValid**</span></span>](id3dx11effectpass-isvalid.md)                             | <span data-ttu-id="bef17-136">Протестируйте пройденный тест, чтобы увидеть, содержит ли он допустимый синтаксис.</span><span class="sxs-lookup"><span data-stu-id="bef17-136">Test a pass to see if it contains valid syntax.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="bef17-137">Примечания</span><span class="sxs-lookup"><span data-stu-id="bef17-137">Remarks</span></span>

<span data-ttu-id="bef17-138">Проход — это блок кода, который задает объекты состояния рендеринга и шейдеры.</span><span class="sxs-lookup"><span data-stu-id="bef17-138">A pass is a block of code that sets render-state objects and shaders.</span></span> <span data-ttu-id="bef17-139">В методе объявляется проход.</span><span class="sxs-lookup"><span data-stu-id="bef17-139">A pass is declared within a technique.</span></span>

<span data-ttu-id="bef17-140">Чтобы получить интерфейс передачи эффектов, вызовите метод, например [**ID3DX11EffectTechnique:: жетпассбинаме**](id3dx11effecttechnique-getpassbyname.md).</span><span class="sxs-lookup"><span data-stu-id="bef17-140">To get an effect-pass interface, call a method like [**ID3DX11EffectTechnique::GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="bef17-141">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="bef17-141">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bef17-142">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="bef17-142">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bef17-143">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bef17-143">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bef17-144">Требования</span><span class="sxs-lookup"><span data-stu-id="bef17-144">Requirements</span></span>



| <span data-ttu-id="bef17-145">Требование</span><span class="sxs-lookup"><span data-stu-id="bef17-145">Requirement</span></span> | <span data-ttu-id="bef17-146">Значение</span><span class="sxs-lookup"><span data-stu-id="bef17-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bef17-147">Header</span><span class="sxs-lookup"><span data-stu-id="bef17-147">Header</span></span><br/>  | <dl> <span data-ttu-id="bef17-148"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bef17-148"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bef17-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bef17-149">Library</span></span><br/> | <dl> <span data-ttu-id="bef17-150"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="bef17-150"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bef17-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bef17-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bef17-152">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="bef17-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="bef17-153">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="bef17-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





