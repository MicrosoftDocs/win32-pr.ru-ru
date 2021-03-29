---
title: Интерфейс ID3DX11EffectTechnique (D3dx11effect. h)
description: Интерфейс ID3DX11EffectTechnique — это коллекция проходов. Время существования объекта ID3DX11EffectTechnique равно времени существования родительского объекта ID3DX11Effect.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Интерфейс ID3DX11EffectTechnique Direct3D 11
- Интерфейс ID3DX11EffectTechnique Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987194"
---
# <a name="id3dx11effecttechnique-interface"></a><span data-ttu-id="25447-105">Интерфейс ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="25447-105">ID3DX11EffectTechnique interface</span></span>

<span data-ttu-id="25447-106">Интерфейс **ID3DX11EffectTechnique** — это коллекция проходов.</span><span class="sxs-lookup"><span data-stu-id="25447-106">An **ID3DX11EffectTechnique** interface is a collection of passes.</span></span>

<span data-ttu-id="25447-107">Время существования объекта **ID3DX11EffectTechnique** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .</span><span class="sxs-lookup"><span data-stu-id="25447-107">The lifetime of an **ID3DX11EffectTechnique** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="25447-108">Методы</span><span class="sxs-lookup"><span data-stu-id="25447-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="25447-109">Методы</span><span class="sxs-lookup"><span data-stu-id="25447-109">Methods</span></span>

<span data-ttu-id="25447-110">Интерфейс **ID3DX11EffectTechnique** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="25447-110">The **ID3DX11EffectTechnique** interface has these methods.</span></span>



| <span data-ttu-id="25447-111">Метод</span><span class="sxs-lookup"><span data-stu-id="25447-111">Method</span></span>                                                                        | <span data-ttu-id="25447-112">Описание</span><span class="sxs-lookup"><span data-stu-id="25447-112">Description</span></span>                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="25447-113">**компутестатеблоккмаск**</span><span class="sxs-lookup"><span data-stu-id="25447-113">**ComputeStateBlockMask**</span></span>](id3dx11effecttechnique-computestateblockmask.md) | <span data-ttu-id="25447-114">Вычислите маску блока состояния, чтобы разрешить или запретить изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="25447-114">Compute a state-block mask to allow/prevent state changes.</span></span><br/> |
| [<span data-ttu-id="25447-115">**жетаннотатионбиндекс**</span><span class="sxs-lookup"><span data-stu-id="25447-115">**GetAnnotationByIndex**</span></span>](id3dx11effecttechnique-getannotationbyindex.md)   | <span data-ttu-id="25447-116">Получение заметки по индексу.</span><span class="sxs-lookup"><span data-stu-id="25447-116">Get an annotation by index.</span></span><br/>                                |
| [<span data-ttu-id="25447-117">**жетаннотатионбинаме**</span><span class="sxs-lookup"><span data-stu-id="25447-117">**GetAnnotationByName**</span></span>](id3dx11effecttechnique-getannotationbyname.md)     | <span data-ttu-id="25447-118">Получение заметки по имени.</span><span class="sxs-lookup"><span data-stu-id="25447-118">Get an annotation by name.</span></span><br/>                                 |
| [<span data-ttu-id="25447-119">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="25447-119">**GetDesc**</span></span>](id3dx11effecttechnique-getdesc.md)                             | <span data-ttu-id="25447-120">Получите описание метода.</span><span class="sxs-lookup"><span data-stu-id="25447-120">Get a technique description.</span></span><br/>                               |
| [<span data-ttu-id="25447-121">**жетпассбиндекс**</span><span class="sxs-lookup"><span data-stu-id="25447-121">**GetPassByIndex**</span></span>](id3dx11effecttechnique-getpassbyindex.md)               | <span data-ttu-id="25447-122">Получение передаваемого по индексу.</span><span class="sxs-lookup"><span data-stu-id="25447-122">Get a pass by index.</span></span><br/>                                       |
| [<span data-ttu-id="25447-123">**жетпассбинаме**</span><span class="sxs-lookup"><span data-stu-id="25447-123">**GetPassByName**</span></span>](id3dx11effecttechnique-getpassbyname.md)                 | <span data-ttu-id="25447-124">Получение передачи по имени.</span><span class="sxs-lookup"><span data-stu-id="25447-124">Get a pass by name.</span></span><br/>                                        |
| [<span data-ttu-id="25447-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="25447-125">**IsValid**</span></span>](id3dx11effecttechnique-isvalid.md)                             | <span data-ttu-id="25447-126">Протестируйте метод, чтобы проверить, содержит ли он допустимый синтаксис.</span><span class="sxs-lookup"><span data-stu-id="25447-126">Test a technique to see if it contains valid syntax.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="25447-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="25447-127">Remarks</span></span>

<span data-ttu-id="25447-128">Результат содержит один или несколько методов. Каждый прием содержит один или несколько проходов; Каждый этап содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="25447-128">An effect contains one or more techniques; each technique contains one or more passes; each pass contains state assignments.</span></span>

<span data-ttu-id="25447-129">Чтобы получить интерфейс методики влияния, вызовите метод, например [**ID3DX11Effect:: жеттечникуебинаме**](id3dx11effect-gettechniquebyname.md).</span><span class="sxs-lookup"><span data-stu-id="25447-129">To get an effect-technique interface, call a method such as [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="25447-130">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="25447-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="25447-131">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="25447-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="25447-132">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="25447-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="25447-133">Требования</span><span class="sxs-lookup"><span data-stu-id="25447-133">Requirements</span></span>



| <span data-ttu-id="25447-134">Требование</span><span class="sxs-lookup"><span data-stu-id="25447-134">Requirement</span></span> | <span data-ttu-id="25447-135">Значение</span><span class="sxs-lookup"><span data-stu-id="25447-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25447-136">Header</span><span class="sxs-lookup"><span data-stu-id="25447-136">Header</span></span><br/>  | <dl> <span data-ttu-id="25447-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="25447-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="25447-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="25447-138">Library</span></span><br/> | <dl> <span data-ttu-id="25447-139"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="25447-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25447-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25447-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25447-141">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="25447-141">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="25447-142">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="25447-142">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





