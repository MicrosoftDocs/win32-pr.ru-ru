---
title: Метод ID3DX11Effect Жетвариаблебисемантик (D3dx11effect. h)
description: Получить переменную по семантике.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- Метод Жетвариаблебисемантик Direct3D 11
- Метод Жетвариаблебисемантик Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетвариаблебисемантик
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273908"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a><span data-ttu-id="3cf38-106">Метод ID3DX11Effect:: Жетвариаблебисемантик</span><span class="sxs-lookup"><span data-stu-id="3cf38-106">ID3DX11Effect::GetVariableBySemantic method</span></span>

<span data-ttu-id="3cf38-107">Получить переменную по семантике.</span><span class="sxs-lookup"><span data-stu-id="3cf38-107">Get a variable by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf38-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cf38-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="3cf38-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cf38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cf38-110">*Семантическ*</span><span class="sxs-lookup"><span data-stu-id="3cf38-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="3cf38-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3cf38-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3cf38-112">Семантическое имя.</span><span class="sxs-lookup"><span data-stu-id="3cf38-112">The semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cf38-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cf38-113">Return value</span></span>

<span data-ttu-id="3cf38-114">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="3cf38-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="3cf38-115">Указатель на переменную действия, определяемую семантикой.</span><span class="sxs-lookup"><span data-stu-id="3cf38-115">A pointer to the effect variable indicated by the Semantic.</span></span> <span data-ttu-id="3cf38-116">См. [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="3cf38-116">See [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3cf38-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="3cf38-117">Remarks</span></span>

<span data-ttu-id="3cf38-118">Каждая переменная Effect может иметь семантическую присоединение, которая представляет собой строку метаданных, определяемую пользователем.</span><span class="sxs-lookup"><span data-stu-id="3cf38-118">Each effect variable can have a semantic attached, which is a user defined metadata string.</span></span> <span data-ttu-id="3cf38-119">Некоторые [семантики системных значений](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) являются зарезервированными словами, которые инициируют встроенные функции стадией конвейера.</span><span class="sxs-lookup"><span data-stu-id="3cf38-119">Some [system-value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) are reserved words that trigger built in functionality by pipeline stages.</span></span>

<span data-ttu-id="3cf38-120">Метод возвращает указатель на [**интерфейс переменной влияния**](id3dx11effectvariable.md) , если переменная не найдена. можно вызвать [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) , чтобы проверить, существует ли семантическая семантика.</span><span class="sxs-lookup"><span data-stu-id="3cf38-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the semantic exists.</span></span>

> [!Note]  
> <span data-ttu-id="3cf38-121">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="3cf38-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3cf38-122">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="3cf38-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3cf38-123">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3cf38-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3cf38-124">Требования</span><span class="sxs-lookup"><span data-stu-id="3cf38-124">Requirements</span></span>



| <span data-ttu-id="3cf38-125">Требование</span><span class="sxs-lookup"><span data-stu-id="3cf38-125">Requirement</span></span> | <span data-ttu-id="3cf38-126">Значение</span><span class="sxs-lookup"><span data-stu-id="3cf38-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf38-127">Header</span><span class="sxs-lookup"><span data-stu-id="3cf38-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3cf38-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cf38-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3cf38-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3cf38-129">Library</span></span><br/> | <dl> <span data-ttu-id="3cf38-130"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="3cf38-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cf38-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cf38-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf38-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="3cf38-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

