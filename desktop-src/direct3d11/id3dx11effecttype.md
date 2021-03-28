---
title: Интерфейс ID3DX11EffectType (D3dx11effect. h)
description: Интерфейс ID3DX11EffectType обращается к переменным эффектов по типу. Время существования объекта ID3DX11EffectType равно времени существования родительского объекта ID3DX11Effect.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- Интерфейс ID3DX11EffectType Direct3D 11
- Интерфейс ID3DX11EffectType Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820997"
---
# <a name="id3dx11effecttype-interface"></a><span data-ttu-id="2ef3d-105">Интерфейс ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="2ef3d-105">ID3DX11EffectType interface</span></span>

<span data-ttu-id="2ef3d-106">Интерфейс **ID3DX11EffectType** обращается к переменным эффектов по типу.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-106">The **ID3DX11EffectType** interface accesses effect variables by type.</span></span>

<span data-ttu-id="2ef3d-107">Время существования объекта **ID3DX11EffectType** равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .</span><span class="sxs-lookup"><span data-stu-id="2ef3d-107">The lifetime of an **ID3DX11EffectType** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="2ef3d-108">Методы</span><span class="sxs-lookup"><span data-stu-id="2ef3d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2ef3d-109">Методы</span><span class="sxs-lookup"><span data-stu-id="2ef3d-109">Methods</span></span>

<span data-ttu-id="2ef3d-110">Интерфейс **ID3DX11EffectType** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-110">The **ID3DX11EffectType** interface has these methods.</span></span>



| <span data-ttu-id="2ef3d-111">Метод</span><span class="sxs-lookup"><span data-stu-id="2ef3d-111">Method</span></span>                                                                       | <span data-ttu-id="2ef3d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2ef3d-112">Description</span></span>                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="2ef3d-113">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="2ef3d-113">**GetDesc**</span></span>](id3dx11effecttype-getdesc.md)                                 | <span data-ttu-id="2ef3d-114">Получите описание типа Effect.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-114">Get an effect-type description.</span></span><br/>        |
| [<span data-ttu-id="2ef3d-115">**жетмембернаме**</span><span class="sxs-lookup"><span data-stu-id="2ef3d-115">**GetMemberName**</span></span>](id3dx11effecttype-getmembername.md)                     | <span data-ttu-id="2ef3d-116">Возвращает имя элемента.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-116">Get the name of a member.</span></span><br/>              |
| [<span data-ttu-id="2ef3d-117">**жетмемберсемантик**</span><span class="sxs-lookup"><span data-stu-id="2ef3d-117">**GetMemberSemantic**</span></span>](id3dx11effecttype-getmembersemantic.md)             | <span data-ttu-id="2ef3d-118">Возвращает семантическую присоединение к элементу.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-118">Get the semantic attached to a member.</span></span><br/> |
| [<span data-ttu-id="2ef3d-119">**GetMemberTypeByIndex**</span><span class="sxs-lookup"><span data-stu-id="2ef3d-119">**GetMemberTypeByIndex**</span></span>](id3dx11effecttype-getmembertypebyindex.md)       | <span data-ttu-id="2ef3d-120">Получение типа элемента по индексу.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-120">Get a member type by index.</span></span><br/>            |
| [<span data-ttu-id="2ef3d-121">**GetMemberTypeByName**</span><span class="sxs-lookup"><span data-stu-id="2ef3d-121">**GetMemberTypeByName**</span></span>](id3dx11effecttype-getmembertypebyname.md)         | <span data-ttu-id="2ef3d-122">Получение типа элемента по имени.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-122">Get an member type by name.</span></span><br/>            |
| [<span data-ttu-id="2ef3d-123">**жетмембертипебисемантик**</span><span class="sxs-lookup"><span data-stu-id="2ef3d-123">**GetMemberTypeBySemantic**</span></span>](id3dx11effecttype-getmembertypebysemantic.md) | <span data-ttu-id="2ef3d-124">Получение типа члена по семантике.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-124">Get a member type by semantic.</span></span><br/>         |
| [<span data-ttu-id="2ef3d-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="2ef3d-125">**IsValid**</span></span>](id3dx11effecttype-isvalid.md)                                 | <span data-ttu-id="2ef3d-126">Проверяет допустимость типа воздействия.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-126">Tests that the effect type is valid.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="2ef3d-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ef3d-127">Remarks</span></span>

<span data-ttu-id="2ef3d-128">Чтобы получить сведения о типе эффектов из переменной Effect, вызовите метод [**ID3DX11EffectVariable:: GetType**](id3dx11effectvariable-gettype.md).</span><span class="sxs-lookup"><span data-stu-id="2ef3d-128">To get information about an effect type from an effect variable, call [**ID3DX11EffectVariable::GetType**](id3dx11effectvariable-gettype.md).</span></span>

> [!Note]  
> <span data-ttu-id="2ef3d-129">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-129">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2ef3d-130">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="2ef3d-130">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2ef3d-131">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2ef3d-131">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2ef3d-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2ef3d-132">Requirements</span></span>



| <span data-ttu-id="2ef3d-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2ef3d-133">Requirement</span></span> | <span data-ttu-id="2ef3d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2ef3d-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef3d-135">Header</span><span class="sxs-lookup"><span data-stu-id="2ef3d-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2ef3d-136"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ef3d-136"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2ef3d-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ef3d-137">Library</span></span><br/> | <dl> <span data-ttu-id="2ef3d-138"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="2ef3d-138"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ef3d-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ef3d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef3d-140">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="2ef3d-140">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2ef3d-141">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="2ef3d-141">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





