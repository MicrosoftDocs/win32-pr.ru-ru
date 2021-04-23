---
title: Метод ID3DX11Effect Жетвариаблебиндекс (D3dx11effect. h)
description: Возвращает переменную по индексу.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Метод Жетвариаблебиндекс Direct3D 11
- Метод Жетвариаблебиндекс Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетвариаблебиндекс
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998615"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a><span data-ttu-id="c4335-106">Метод ID3DX11Effect:: Жетвариаблебиндекс</span><span class="sxs-lookup"><span data-stu-id="c4335-106">ID3DX11Effect::GetVariableByIndex method</span></span>

<span data-ttu-id="c4335-107">Возвращает переменную по индексу.</span><span class="sxs-lookup"><span data-stu-id="c4335-107">Get a variable by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4335-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4335-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="c4335-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4335-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4335-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c4335-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c4335-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c4335-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c4335-112">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="c4335-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4335-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4335-113">Return value</span></span>

<span data-ttu-id="c4335-114">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4335-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="c4335-115">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="c4335-115">A pointer to a [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4335-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4335-116">Remarks</span></span>

<span data-ttu-id="c4335-117">Результат может содержать одну или несколько переменных.</span><span class="sxs-lookup"><span data-stu-id="c4335-117">An effect may contain one or more variables.</span></span> <span data-ttu-id="c4335-118">Переменные за пределами метода считаются глобальными для всех эффектов, а те, которые находятся внутри метода, являются локальными для этого метода.</span><span class="sxs-lookup"><span data-stu-id="c4335-118">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="c4335-119">Можно получить доступ к любой локальной переменной с нестатическим действием, используя ее имя или индекс.</span><span class="sxs-lookup"><span data-stu-id="c4335-119">You can access any local non-static effect variable using its name or with an index.</span></span>

<span data-ttu-id="c4335-120">Метод возвращает указатель на [**интерфейс переменной влияния**](id3dx11effectvariable.md) , если переменная не найдена. можно вызвать [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) , чтобы проверить, существует ли индекс.</span><span class="sxs-lookup"><span data-stu-id="c4335-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the index exists.</span></span>

> [!Note]  
> <span data-ttu-id="c4335-121">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="c4335-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c4335-122">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="c4335-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c4335-123">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c4335-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4335-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c4335-124">Requirements</span></span>



| <span data-ttu-id="c4335-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c4335-125">Requirement</span></span> | <span data-ttu-id="c4335-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c4335-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4335-127">Header</span><span class="sxs-lookup"><span data-stu-id="c4335-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c4335-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4335-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c4335-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c4335-129">Library</span></span><br/> | <dl> <span data-ttu-id="c4335-130"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="c4335-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4335-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4335-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4335-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="c4335-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

