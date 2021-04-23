---
title: Метод ID3DX11Effect Жеттечникуебинаме (D3dx11effect. h)
description: Получите метод по имени. | Метод ID3DX11Effect Жеттечникуебинаме (D3dx11effect. h)
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- Метод Жеттечникуебинаме Direct3D 11
- Метод Жеттечникуебинаме Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жеттечникуебинаме
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26b6067352d4ca898cc1fc970524040d407bda1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987092"
---
# <a name="id3dx11effectgettechniquebyname-method"></a><span data-ttu-id="587e6-107">Метод ID3DX11Effect:: Жеттечникуебинаме</span><span class="sxs-lookup"><span data-stu-id="587e6-107">ID3DX11Effect::GetTechniqueByName method</span></span>

<span data-ttu-id="587e6-108">Получите метод по имени.</span><span class="sxs-lookup"><span data-stu-id="587e6-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="587e6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="587e6-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="587e6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="587e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="587e6-111">*имя*;</span><span class="sxs-lookup"><span data-stu-id="587e6-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="587e6-112">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="587e6-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="587e6-113">Имя метода.</span><span class="sxs-lookup"><span data-stu-id="587e6-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="587e6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="587e6-114">Return value</span></span>

<span data-ttu-id="587e6-115">Тип: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="587e6-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="587e6-116">Указатель на [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="587e6-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span> <span data-ttu-id="587e6-117">Если метод с соответствующим именем не найден, возвращается недопустимый метод.</span><span class="sxs-lookup"><span data-stu-id="587e6-117">If a technique with the appropriate name is not found an invalid technique is returned.</span></span> <span data-ttu-id="587e6-118">[**ID3DX11EffectTechnique:: IsValid**](id3dx11effecttechnique-isvalid.md) должен вызываться для возвращаемого метода, чтобы определить, является ли он допустимым.</span><span class="sxs-lookup"><span data-stu-id="587e6-118">[**ID3DX11EffectTechnique::IsValid**](id3dx11effecttechnique-isvalid.md) should be called on the returned technique to determine whether it is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="587e6-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="587e6-119">Remarks</span></span>

<span data-ttu-id="587e6-120">Результат содержит один или несколько методов. Каждый прием содержит один или несколько проходов.</span><span class="sxs-lookup"><span data-stu-id="587e6-120">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="587e6-121">Можно получить доступ к методу, используя его имя или индекс.</span><span class="sxs-lookup"><span data-stu-id="587e6-121">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="587e6-122">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="587e6-122">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="587e6-123">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="587e6-123">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="587e6-124">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="587e6-124">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="587e6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="587e6-125">Requirements</span></span>



| <span data-ttu-id="587e6-126">Требование</span><span class="sxs-lookup"><span data-stu-id="587e6-126">Requirement</span></span> | <span data-ttu-id="587e6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="587e6-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="587e6-128">Header</span><span class="sxs-lookup"><span data-stu-id="587e6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="587e6-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="587e6-129"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="587e6-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="587e6-130">Library</span></span><br/> | <dl> <span data-ttu-id="587e6-131"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="587e6-131"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="587e6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="587e6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="587e6-133">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="587e6-133">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

