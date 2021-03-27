---
title: Интерфейс ID3DX11EffectVariable (D3dx11effect. h)
description: Интерфейс ID3DX11EffectVariable является базовым классом для всех переменных эффектов. Время существования объекта ID3DX11EffectVariable равно времени существования родительского объекта ID3DX11Effect.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Интерфейс ID3DX11EffectVariable Direct3D 11
- Интерфейс ID3DX11EffectVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821285"
---
# <a name="id3dx11effectvariable-interface"></a><span data-ttu-id="5efa2-105">Интерфейс ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="5efa2-105">ID3DX11EffectVariable interface</span></span>

<span data-ttu-id="5efa2-106">Интерфейс **ID3DX11EffectVariable** является базовым классом для всех переменных эффектов.</span><span class="sxs-lookup"><span data-stu-id="5efa2-106">The **ID3DX11EffectVariable** interface is the base class for all effect variables.</span></span>

<span data-ttu-id="5efa2-107">Время существования объекта **ID3DX11EffectVariable** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .</span><span class="sxs-lookup"><span data-stu-id="5efa2-107">The lifetime of an **ID3DX11EffectVariable** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="5efa2-108">Методы</span><span class="sxs-lookup"><span data-stu-id="5efa2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5efa2-109">Методы</span><span class="sxs-lookup"><span data-stu-id="5efa2-109">Methods</span></span>

<span data-ttu-id="5efa2-110">Интерфейс **ID3DX11EffectVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5efa2-110">The **ID3DX11EffectVariable** interface has these methods.</span></span>



| <span data-ttu-id="5efa2-111">Метод</span><span class="sxs-lookup"><span data-stu-id="5efa2-111">Method</span></span>                                                                           | <span data-ttu-id="5efa2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5efa2-112">Description</span></span>                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="5efa2-113">**асбленд**</span><span class="sxs-lookup"><span data-stu-id="5efa2-113">**AsBlend**</span></span>](id3dx11effectvariable-asblend.md)                                 | <span data-ttu-id="5efa2-114">Получить переменную Effect.</span><span class="sxs-lookup"><span data-stu-id="5efa2-114">Get a effect-blend variable.</span></span><br/>                |
| [<span data-ttu-id="5efa2-115">**асклассинстанце**</span><span class="sxs-lookup"><span data-stu-id="5efa2-115">**AsClassInstance**</span></span>](id3dx11effectvariable-asclassinstance.md)                 | <span data-ttu-id="5efa2-116">Получение переменной экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="5efa2-116">Get a class-instance variable.</span></span><br/>              |
| [<span data-ttu-id="5efa2-117">**асконстантбуффер**</span><span class="sxs-lookup"><span data-stu-id="5efa2-117">**AsConstantBuffer**</span></span>](id3dx11effectvariable-asconstantbuffer.md)               | <span data-ttu-id="5efa2-118">Получение буфера константы.</span><span class="sxs-lookup"><span data-stu-id="5efa2-118">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="5efa2-119">**асдепсстенЦил**</span><span class="sxs-lookup"><span data-stu-id="5efa2-119">**AsDepthStencil**</span></span>](id3dx11effectvariable-asdepthstencil.md)                   | <span data-ttu-id="5efa2-120">Возвращает переменную с набором элементов глубины.</span><span class="sxs-lookup"><span data-stu-id="5efa2-120">Get a depth-stencil variable.</span></span><br/>               |
| [<span data-ttu-id="5efa2-121">**асдепсстенЦилвиев**</span><span class="sxs-lookup"><span data-stu-id="5efa2-121">**AsDepthStencilView**</span></span>](id3dx11effectvariable-asdepthstencilview.md)           | <span data-ttu-id="5efa2-122">Получите переменную представления с глубиной набора элементов.</span><span class="sxs-lookup"><span data-stu-id="5efa2-122">Get a depth-stencil-view variable.</span></span><br/>          |
| [<span data-ttu-id="5efa2-123">**асинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="5efa2-123">**AsInterface**</span></span>](id3dx11effectvariable-asinterface.md)                         | <span data-ttu-id="5efa2-124">Возвращает переменную интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5efa2-124">Get an interface variable.</span></span><br/>                  |
| [<span data-ttu-id="5efa2-125">**асматрикс**</span><span class="sxs-lookup"><span data-stu-id="5efa2-125">**AsMatrix**</span></span>](id3dx11effectvariable-asmatrix.md)                               | <span data-ttu-id="5efa2-126">Возвращает переменную матрицы.</span><span class="sxs-lookup"><span data-stu-id="5efa2-126">Get a matrix variable.</span></span><br/>                      |
| [<span data-ttu-id="5efa2-127">**асрастеризер**</span><span class="sxs-lookup"><span data-stu-id="5efa2-127">**AsRasterizer**</span></span>](id3dx11effectvariable-asrasterizer.md)                       | <span data-ttu-id="5efa2-128">Получение переменной средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="5efa2-128">Get a rasterizer variable.</span></span><br/>                  |
| [<span data-ttu-id="5efa2-129">**асрендертаржетвиев**</span><span class="sxs-lookup"><span data-stu-id="5efa2-129">**AsRenderTargetView**</span></span>](id3dx11effectvariable-asrendertargetview.md)           | <span data-ttu-id="5efa2-130">Получает переменную визуализации-целевого представления.</span><span class="sxs-lookup"><span data-stu-id="5efa2-130">Get a render-target-view variable.</span></span><br/>          |
| [<span data-ttu-id="5efa2-131">**ассамплер**</span><span class="sxs-lookup"><span data-stu-id="5efa2-131">**AsSampler**</span></span>](id3dx11effectvariable-assampler.md)                             | <span data-ttu-id="5efa2-132">Получить переменную образца.</span><span class="sxs-lookup"><span data-stu-id="5efa2-132">Get a sampler variable.</span></span><br/>                     |
| [<span data-ttu-id="5efa2-133">**асскалар**</span><span class="sxs-lookup"><span data-stu-id="5efa2-133">**AsScalar**</span></span>](id3dx11effectvariable-asscalar.md)                               | <span data-ttu-id="5efa2-134">Получить скалярную переменную.</span><span class="sxs-lookup"><span data-stu-id="5efa2-134">Get a scalar variable.</span></span><br/>                      |
| [<span data-ttu-id="5efa2-135">**асшадер**</span><span class="sxs-lookup"><span data-stu-id="5efa2-135">**AsShader**</span></span>](id3dx11effectvariable-asshader.md)                               | <span data-ttu-id="5efa2-136">Получение переменной шейдера.</span><span class="sxs-lookup"><span data-stu-id="5efa2-136">Get a shader variable.</span></span><br/>                      |
| [<span data-ttu-id="5efa2-137">**асшадерресаурце**</span><span class="sxs-lookup"><span data-stu-id="5efa2-137">**AsShaderResource**</span></span>](id3dx11effectvariable-asshaderresource.md)               | <span data-ttu-id="5efa2-138">Получение переменной-ресурса шейдера.</span><span class="sxs-lookup"><span data-stu-id="5efa2-138">Get a shader-resource variable.</span></span><br/>             |
| [<span data-ttu-id="5efa2-139">**AsString**</span><span class="sxs-lookup"><span data-stu-id="5efa2-139">**AsString**</span></span>](id3dx11effectvariable-asstring.md)                               | <span data-ttu-id="5efa2-140">Получение строковой переменной.</span><span class="sxs-lookup"><span data-stu-id="5efa2-140">Get a string variable.</span></span><br/>                      |
| [<span data-ttu-id="5efa2-141">**асунордередакцессвиев**</span><span class="sxs-lookup"><span data-stu-id="5efa2-141">**AsUnorderedAccessView**</span></span>](id3dx11effectvariable-asunorderedaccessview.md)     | <span data-ttu-id="5efa2-142">Возвращает неупорядоченную переменную с доступом к представлениям.</span><span class="sxs-lookup"><span data-stu-id="5efa2-142">Get an unordered-access-view variable.</span></span><br/>      |
| [<span data-ttu-id="5efa2-143">**асвектор**</span><span class="sxs-lookup"><span data-stu-id="5efa2-143">**AsVector**</span></span>](id3dx11effectvariable-asvector.md)                               | <span data-ttu-id="5efa2-144">Получение переменной Vector.</span><span class="sxs-lookup"><span data-stu-id="5efa2-144">Get a vector variable.</span></span><br/>                      |
| [<span data-ttu-id="5efa2-145">**жетаннотатионбиндекс**</span><span class="sxs-lookup"><span data-stu-id="5efa2-145">**GetAnnotationByIndex**</span></span>](id3dx11effectvariable-getannotationbyindex.md)       | <span data-ttu-id="5efa2-146">Получение заметки по индексу.</span><span class="sxs-lookup"><span data-stu-id="5efa2-146">Get an annotation by index.</span></span><br/>                 |
| [<span data-ttu-id="5efa2-147">**жетаннотатионбинаме**</span><span class="sxs-lookup"><span data-stu-id="5efa2-147">**GetAnnotationByName**</span></span>](id3dx11effectvariable-getannotationbyname.md)         | <span data-ttu-id="5efa2-148">Получение заметки по имени.</span><span class="sxs-lookup"><span data-stu-id="5efa2-148">Get an annotation by name.</span></span><br/>                  |
| [<span data-ttu-id="5efa2-149">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="5efa2-149">**GetDesc**</span></span>](id3dx11effectvariable-getdesc.md)                                 | <span data-ttu-id="5efa2-150">Получить описание.</span><span class="sxs-lookup"><span data-stu-id="5efa2-150">Get a description.</span></span><br/>                          |
| [<span data-ttu-id="5efa2-151">**GetElement**</span><span class="sxs-lookup"><span data-stu-id="5efa2-151">**GetElement**</span></span>](id3dx11effectvariable-getelement.md)                           | <span data-ttu-id="5efa2-152">Получение элемента массива.</span><span class="sxs-lookup"><span data-stu-id="5efa2-152">Get an array element.</span></span><br/>                       |
| [<span data-ttu-id="5efa2-153">**жетмембербиндекс**</span><span class="sxs-lookup"><span data-stu-id="5efa2-153">**GetMemberByIndex**</span></span>](id3dx11effectvariable-getmemberbyindex.md)               | <span data-ttu-id="5efa2-154">Получение члена структуры по индексу.</span><span class="sxs-lookup"><span data-stu-id="5efa2-154">Get a structure member by index.</span></span><br/>            |
| [<span data-ttu-id="5efa2-155">**жетмембербинаме**</span><span class="sxs-lookup"><span data-stu-id="5efa2-155">**GetMemberByName**</span></span>](id3dx11effectvariable-getmemberbyname.md)                 | <span data-ttu-id="5efa2-156">Получение члена структуры по имени.</span><span class="sxs-lookup"><span data-stu-id="5efa2-156">Get a structure member by name.</span></span><br/>             |
| [<span data-ttu-id="5efa2-157">**жетмембербисемантик**</span><span class="sxs-lookup"><span data-stu-id="5efa2-157">**GetMemberBySemantic**</span></span>](id3dx11effectvariable-getmemberbysemantic.md)         | <span data-ttu-id="5efa2-158">Получение члена структуры по семантике.</span><span class="sxs-lookup"><span data-stu-id="5efa2-158">Get a structure member by semantic.</span></span><br/>         |
| [<span data-ttu-id="5efa2-159">**жетпарентконстантбуффер**</span><span class="sxs-lookup"><span data-stu-id="5efa2-159">**GetParentConstantBuffer**</span></span>](id3dx11effectvariable-getparentconstantbuffer.md) | <span data-ttu-id="5efa2-160">Получение буфера константы.</span><span class="sxs-lookup"><span data-stu-id="5efa2-160">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="5efa2-161">**жетраввалуе**</span><span class="sxs-lookup"><span data-stu-id="5efa2-161">**GetRawValue**</span></span>](id3dx11effectvariable-getrawvalue.md)                         | <span data-ttu-id="5efa2-162">Получение данных.</span><span class="sxs-lookup"><span data-stu-id="5efa2-162">Get data.</span></span><br/>                                   |
| [<span data-ttu-id="5efa2-163">**GetType**</span><span class="sxs-lookup"><span data-stu-id="5efa2-163">**GetType**</span></span>](id3dx11effectvariable-gettype.md)                                 | <span data-ttu-id="5efa2-164">Получение сведений о типе.</span><span class="sxs-lookup"><span data-stu-id="5efa2-164">Get type information.</span></span><br/>                       |
| [<span data-ttu-id="5efa2-165">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="5efa2-165">**IsValid**</span></span>](id3dx11effectvariable-isvalid.md)                                 | <span data-ttu-id="5efa2-166">Сравните тип данных с хранимыми данными.</span><span class="sxs-lookup"><span data-stu-id="5efa2-166">Compare the data type with the data stored.</span></span><br/> |
| [<span data-ttu-id="5efa2-167">**сетраввалуе**</span><span class="sxs-lookup"><span data-stu-id="5efa2-167">**SetRawValue**</span></span>](id3dx11effectvariable-setrawvalue.md)                         | <span data-ttu-id="5efa2-168">Настройка данных.</span><span class="sxs-lookup"><span data-stu-id="5efa2-168">Set data.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="5efa2-169">Примечания</span><span class="sxs-lookup"><span data-stu-id="5efa2-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5efa2-170">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="5efa2-170">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5efa2-171">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="5efa2-171">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5efa2-172">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5efa2-172">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5efa2-173">Требования</span><span class="sxs-lookup"><span data-stu-id="5efa2-173">Requirements</span></span>



| <span data-ttu-id="5efa2-174">Требование</span><span class="sxs-lookup"><span data-stu-id="5efa2-174">Requirement</span></span> | <span data-ttu-id="5efa2-175">Значение</span><span class="sxs-lookup"><span data-stu-id="5efa2-175">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5efa2-176">Header</span><span class="sxs-lookup"><span data-stu-id="5efa2-176">Header</span></span><br/>  | <dl> <span data-ttu-id="5efa2-177"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5efa2-177"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5efa2-178">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5efa2-178">Library</span></span><br/> | <dl> <span data-ttu-id="5efa2-179"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="5efa2-179"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5efa2-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5efa2-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5efa2-181">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="5efa2-181">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="5efa2-182">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="5efa2-182">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





