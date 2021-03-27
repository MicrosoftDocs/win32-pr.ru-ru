---
title: Метод ID3DX11EffectGroup Жеттечникуебиндекс (D3dx11effect. h)
description: Получение методики по индексу. | Метод ID3DX11EffectGroup Жеттечникуебиндекс (D3dx11effect. h)
ms.assetid: b0962957-20d1-4ec6-9f8e-acc7a62c5f4e
keywords:
- Метод Жеттечникуебиндекс Direct3D 11
- Метод Жеттечникуебиндекс Direct3D 11, интерфейс ID3DX11EffectGroup
- Интерфейс ID3DX11EffectGroup Direct3D 11, метод Жеттечникуебиндекс
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe42d71886ae93bdaff7ac956554ff9a97fc9f8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000430"
---
# <a name="id3dx11effectgroupgettechniquebyindex-method"></a><span data-ttu-id="ea8dd-107">Метод ID3DX11EffectGroup:: Жеттечникуебиндекс</span><span class="sxs-lookup"><span data-stu-id="ea8dd-107">ID3DX11EffectGroup::GetTechniqueByIndex method</span></span>

<span data-ttu-id="ea8dd-108">Получение методики по индексу.</span><span class="sxs-lookup"><span data-stu-id="ea8dd-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8dd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea8dd-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="ea8dd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea8dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8dd-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="ea8dd-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="ea8dd-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ea8dd-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ea8dd-113">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="ea8dd-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8dd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea8dd-114">Return value</span></span>

<span data-ttu-id="ea8dd-115">Тип: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea8dd-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="ea8dd-116">Указатель на [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="ea8dd-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea8dd-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ea8dd-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea8dd-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="ea8dd-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ea8dd-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="ea8dd-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ea8dd-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ea8dd-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea8dd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ea8dd-121">Requirements</span></span>



| <span data-ttu-id="ea8dd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ea8dd-122">Requirement</span></span> | <span data-ttu-id="ea8dd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ea8dd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8dd-124">Header</span><span class="sxs-lookup"><span data-stu-id="ea8dd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ea8dd-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea8dd-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ea8dd-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ea8dd-126">Library</span></span><br/> | <dl> <span data-ttu-id="ea8dd-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="ea8dd-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea8dd-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea8dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8dd-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="ea8dd-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

