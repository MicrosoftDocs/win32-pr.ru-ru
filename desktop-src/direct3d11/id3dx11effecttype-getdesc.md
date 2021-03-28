---
title: Метод ID3DX11EffectType-desc (D3dx11effect. h)
description: Получите описание типа Effect.
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- Метод DESC Direct3D 11
- Метод DESC Direct3D 11, интерфейс ID3DX11EffectType
- ID3DX11EffectType интерфейс Direct3D 11, метод DESC
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1ee52e4c6628c00b0155e5bd3081b6c4fd8c46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998720"
---
# <a name="id3dx11effecttypegetdesc-method"></a><span data-ttu-id="e5dc5-106">Метод ID3DX11EffectType:: DESC</span><span class="sxs-lookup"><span data-stu-id="e5dc5-106">ID3DX11EffectType::GetDesc method</span></span>

<span data-ttu-id="e5dc5-107">Получите описание типа Effect.</span><span class="sxs-lookup"><span data-stu-id="e5dc5-107">Get an effect-type description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5dc5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5dc5-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="e5dc5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5dc5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5dc5-110">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="e5dc5-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="e5dc5-111">Тип: **[ **D3DX11 \_ тип влияния, \_ \_ DESC**](d3dx11-effect-type-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5dc5-111">Type: **[**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md)\***</span></span>

<span data-ttu-id="e5dc5-112">Указатель на описание типа Effect.</span><span class="sxs-lookup"><span data-stu-id="e5dc5-112">A pointer to an effect-type description.</span></span> <span data-ttu-id="e5dc5-113">См. [**D3DX11 \_ Effect \_ Type \_ DESC**](d3dx11-effect-type-desc.md).</span><span class="sxs-lookup"><span data-stu-id="e5dc5-113">See [**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5dc5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5dc5-114">Return value</span></span>

<span data-ttu-id="e5dc5-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5dc5-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5dc5-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e5dc5-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5dc5-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5dc5-117">Remarks</span></span>

<span data-ttu-id="e5dc5-118">Описание переменной Effect содержит данные о имени, аннотациях, семантическости, флагах и смещении буфера для типа эффектов.</span><span class="sxs-lookup"><span data-stu-id="e5dc5-118">The effect-variable description contains data about the name, annotations, semantic, flags and buffer offset of the effect type.</span></span>

> [!Note]  
> <span data-ttu-id="e5dc5-119">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="e5dc5-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e5dc5-120">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="e5dc5-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e5dc5-121">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e5dc5-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5dc5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e5dc5-122">Requirements</span></span>



| <span data-ttu-id="e5dc5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e5dc5-123">Requirement</span></span> | <span data-ttu-id="e5dc5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e5dc5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5dc5-125">Header</span><span class="sxs-lookup"><span data-stu-id="e5dc5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e5dc5-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5dc5-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e5dc5-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5dc5-127">Library</span></span><br/> | <dl> <span data-ttu-id="e5dc5-128"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="e5dc5-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5dc5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5dc5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5dc5-130">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="e5dc5-130">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

 





