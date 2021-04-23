---
title: Метод ID3DX11Effect Жетвариаблебинаме (D3dx11effect. h)
description: Получить переменную по имени.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Метод Жетвариаблебинаме Direct3D 11
- Метод Жетвариаблебинаме Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетвариаблебинаме
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998609"
---
# <a name="id3dx11effectgetvariablebyname-method"></a><span data-ttu-id="0c33f-106">Метод ID3DX11Effect:: Жетвариаблебинаме</span><span class="sxs-lookup"><span data-stu-id="0c33f-106">ID3DX11Effect::GetVariableByName method</span></span>

<span data-ttu-id="0c33f-107">Получить переменную по имени.</span><span class="sxs-lookup"><span data-stu-id="0c33f-107">Get a variable by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c33f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c33f-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="0c33f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c33f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c33f-110">*имя*;</span><span class="sxs-lookup"><span data-stu-id="0c33f-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="0c33f-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0c33f-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0c33f-112">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="0c33f-112">The variable name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c33f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c33f-113">Return value</span></span>

<span data-ttu-id="0c33f-114">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c33f-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="0c33f-115">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="0c33f-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="0c33f-116">Возвращает недопустимую переменную, если указанное имя не найдено.</span><span class="sxs-lookup"><span data-stu-id="0c33f-116">Returns an invalid variable if the specified name cannot be found.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c33f-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c33f-117">Remarks</span></span>

<span data-ttu-id="0c33f-118">Результат может содержать одну или несколько переменных.</span><span class="sxs-lookup"><span data-stu-id="0c33f-118">An effect may contain one or more variables.</span></span> <span data-ttu-id="0c33f-119">Переменные за пределами метода считаются глобальными для всех эффектов, а те, которые находятся внутри метода, являются локальными для этого метода.</span><span class="sxs-lookup"><span data-stu-id="0c33f-119">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="0c33f-120">Можно получить доступ к переменной Effect, используя ее имя или индекс.</span><span class="sxs-lookup"><span data-stu-id="0c33f-120">You can access an effect variable using its name or with an index.</span></span>

<span data-ttu-id="0c33f-121">Метод возвращает указатель на [**интерфейс переменной влияния**](id3dx11effectvariable.md) независимо от того, найдена ли переменная.</span><span class="sxs-lookup"><span data-stu-id="0c33f-121">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) whether or not a variable is found.</span></span> <span data-ttu-id="0c33f-122">[**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) следует вызывать, чтобы проверить, существует ли имя.</span><span class="sxs-lookup"><span data-stu-id="0c33f-122">[**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) should be called to verify whether or not the name exists.</span></span>

> [!Note]  
> <span data-ttu-id="0c33f-123">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="0c33f-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0c33f-124">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="0c33f-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0c33f-125">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0c33f-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0c33f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="0c33f-126">Requirements</span></span>



| <span data-ttu-id="0c33f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="0c33f-127">Requirement</span></span> | <span data-ttu-id="0c33f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="0c33f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c33f-129">Header</span><span class="sxs-lookup"><span data-stu-id="0c33f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0c33f-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c33f-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0c33f-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0c33f-131">Library</span></span><br/> | <dl> <span data-ttu-id="0c33f-132"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="0c33f-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c33f-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c33f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c33f-134">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="0c33f-134">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

