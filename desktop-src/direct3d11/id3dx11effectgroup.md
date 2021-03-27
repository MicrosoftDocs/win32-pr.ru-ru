---
title: Интерфейс ID3DX11EffectGroup (D3dx11effect. h)
description: Интерфейс ID3DX11EffectGroup обращается к группе эффектов. Время существования объекта ID3DX11EffectGroup равно времени существования родительского объекта ID3DX11Effect.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Интерфейс ID3DX11EffectGroup Direct3D 11
- Интерфейс ID3DX11EffectGroup Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986954"
---
# <a name="id3dx11effectgroup-interface"></a><span data-ttu-id="e21d6-105">Интерфейс ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="e21d6-105">ID3DX11EffectGroup interface</span></span>

<span data-ttu-id="e21d6-106">Интерфейс **ID3DX11EffectGroup** обращается к группе эффектов.</span><span class="sxs-lookup"><span data-stu-id="e21d6-106">The **ID3DX11EffectGroup** interface accesses an Effect group.</span></span>

<span data-ttu-id="e21d6-107">Время существования объекта **ID3DX11EffectGroup** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .</span><span class="sxs-lookup"><span data-stu-id="e21d6-107">The lifetime of an **ID3DX11EffectGroup** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="e21d6-108">Методы</span><span class="sxs-lookup"><span data-stu-id="e21d6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e21d6-109">Методы</span><span class="sxs-lookup"><span data-stu-id="e21d6-109">Methods</span></span>

<span data-ttu-id="e21d6-110">Интерфейс **ID3DX11EffectGroup** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e21d6-110">The **ID3DX11EffectGroup** interface has these methods.</span></span>



| <span data-ttu-id="e21d6-111">Метод</span><span class="sxs-lookup"><span data-stu-id="e21d6-111">Method</span></span>                                                                  | <span data-ttu-id="e21d6-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e21d6-112">Description</span></span>                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="e21d6-113">**жетаннотатионбиндекс**</span><span class="sxs-lookup"><span data-stu-id="e21d6-113">**GetAnnotationByIndex**</span></span>](id3dx11effectgroup-getannotationbyindex.md) | <span data-ttu-id="e21d6-114">Получение заметки по индексу.</span><span class="sxs-lookup"><span data-stu-id="e21d6-114">Get an annotation by index.</span></span><br/>                        |
| [<span data-ttu-id="e21d6-115">**жетаннотатионбинаме**</span><span class="sxs-lookup"><span data-stu-id="e21d6-115">**GetAnnotationByName**</span></span>](id3dx11effectgroup-getannotationbyname.md)   | <span data-ttu-id="e21d6-116">Получение заметки по имени.</span><span class="sxs-lookup"><span data-stu-id="e21d6-116">Get an annotation by name.</span></span><br/>                         |
| [<span data-ttu-id="e21d6-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="e21d6-117">**GetDesc**</span></span>](id3dx11effectgroup-getdesc.md)                           | <span data-ttu-id="e21d6-118">Возвращает описание группы.</span><span class="sxs-lookup"><span data-stu-id="e21d6-118">Gets a group description.</span></span><br/>                          |
| [<span data-ttu-id="e21d6-119">**жеттечникуебиндекс**</span><span class="sxs-lookup"><span data-stu-id="e21d6-119">**GetTechniqueByIndex**</span></span>](id3dx11effectgroup-gettechniquebyindex.md)   | <span data-ttu-id="e21d6-120">Получение методики по индексу.</span><span class="sxs-lookup"><span data-stu-id="e21d6-120">Get a technique by index.</span></span><br/>                          |
| [<span data-ttu-id="e21d6-121">**жеттечникуебинаме**</span><span class="sxs-lookup"><span data-stu-id="e21d6-121">**GetTechniqueByName**</span></span>](id3dx11effectgroup-gettechniquebyname.md)     | <span data-ttu-id="e21d6-122">Получите метод по имени.</span><span class="sxs-lookup"><span data-stu-id="e21d6-122">Get a technique by name.</span></span><br/>                           |
| [<span data-ttu-id="e21d6-123">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="e21d6-123">**IsValid**</span></span>](id3dx11effectgroup-isvalid.md)                           | <span data-ttu-id="e21d6-124">Протестируйте результат, чтобы проверить, содержит ли он допустимый синтаксис.</span><span class="sxs-lookup"><span data-stu-id="e21d6-124">Test an effect to see if it contains valid syntax.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e21d6-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="e21d6-125">Remarks</span></span>

<span data-ttu-id="e21d6-126">Чтобы получить интерфейс **ID3DX11EffectGroup** , вызовите метод, например [**ID3DX11Effect:: жетграупбинаме**](id3dx11effect-getgroupbyname.md).</span><span class="sxs-lookup"><span data-stu-id="e21d6-126">To get an **ID3DX11EffectGroup** interface, call a method like [**ID3DX11Effect::GetGroupByName**](id3dx11effect-getgroupbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="e21d6-127">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="e21d6-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e21d6-128">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="e21d6-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e21d6-129">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e21d6-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e21d6-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e21d6-130">Requirements</span></span>



| <span data-ttu-id="e21d6-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e21d6-131">Requirement</span></span> | <span data-ttu-id="e21d6-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e21d6-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e21d6-133">Header</span><span class="sxs-lookup"><span data-stu-id="e21d6-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e21d6-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e21d6-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e21d6-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e21d6-135">Library</span></span><br/> | <dl> <span data-ttu-id="e21d6-136"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="e21d6-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e21d6-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e21d6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e21d6-138">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="e21d6-138">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e21d6-139">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="e21d6-139">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





