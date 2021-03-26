---
title: Метод ID3DX11EffectSamplerVariable Жетбаккингсторе (D3dx11effect. h)
description: Возвращает указатель на переменную, содержащую состояние выборки.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Метод Жетбаккингсторе Direct3D 11
- Метод Жетбаккингсторе Direct3D 11, интерфейс ID3DX11EffectSamplerVariable
- Интерфейс ID3DX11EffectSamplerVariable Direct3D 11, метод Жетбаккингсторе
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f2d6ac3035d1dd2fd3aee8950135d7b4481862
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355363"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a><span data-ttu-id="9450a-106">Метод ID3DX11EffectSamplerVariable:: Жетбаккингсторе</span><span class="sxs-lookup"><span data-stu-id="9450a-106">ID3DX11EffectSamplerVariable::GetBackingStore method</span></span>

<span data-ttu-id="9450a-107">Возвращает указатель на переменную, содержащую состояние выборки.</span><span class="sxs-lookup"><span data-stu-id="9450a-107">Get a pointer to a variable that contains sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9450a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9450a-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="9450a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9450a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9450a-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="9450a-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="9450a-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9450a-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9450a-112">Индексировать в массив описаний образцов.</span><span class="sxs-lookup"><span data-stu-id="9450a-112">Index into an array of sampler descriptions.</span></span> <span data-ttu-id="9450a-113">Если в результате присутствует только одна переменная выборки, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="9450a-113">If there is only one sampler variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="9450a-114">*псамплердеск*</span><span class="sxs-lookup"><span data-stu-id="9450a-114">*pSamplerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="9450a-115">Тип: **[ **D3D11 \_ образец \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span><span class="sxs-lookup"><span data-stu-id="9450a-115">Type: **[**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span></span>

<span data-ttu-id="9450a-116">Указатель на описание образца (см. [**D3D11ный \_ образец \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span><span class="sxs-lookup"><span data-stu-id="9450a-116">A pointer to a sampler description (see [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9450a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9450a-117">Return value</span></span>

<span data-ttu-id="9450a-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9450a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9450a-119">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9450a-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9450a-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="9450a-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9450a-121">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="9450a-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9450a-122">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="9450a-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9450a-123">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9450a-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9450a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9450a-124">Requirements</span></span>



| <span data-ttu-id="9450a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9450a-125">Requirement</span></span> | <span data-ttu-id="9450a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9450a-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9450a-127">Header</span><span class="sxs-lookup"><span data-stu-id="9450a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9450a-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9450a-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9450a-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9450a-129">Library</span></span><br/> | <dl> <span data-ttu-id="9450a-130"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="9450a-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9450a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9450a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9450a-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="9450a-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

