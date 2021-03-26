---
title: Метод ID3DX11EffectPass-desc (D3dx11effect. h)
description: Получите описание этапа.
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- Метод DESC Direct3D 11
- Метод DESC Direct3D 11, интерфейс ID3DX11EffectPass
- ID3DX11EffectPass интерфейс Direct3D 11, метод DESC
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a85a8c08faa100ecb3987a1a1421613d9c448b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355243"
---
# <a name="id3dx11effectpassgetdesc-method"></a><span data-ttu-id="a2e1b-106">Метод ID3DX11EffectPass:: DESC</span><span class="sxs-lookup"><span data-stu-id="a2e1b-106">ID3DX11EffectPass::GetDesc method</span></span>

<span data-ttu-id="a2e1b-107">Получите описание этапа.</span><span class="sxs-lookup"><span data-stu-id="a2e1b-107">Get a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2e1b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2e1b-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a2e1b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2e1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2e1b-110">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="a2e1b-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="a2e1b-111">Тип: **[ **D3DX11 \_ Pass \_ DESC**](d3dx11-pass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2e1b-111">Type: **[**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)\***</span></span>

<span data-ttu-id="a2e1b-112">Указатель на описание этапа (см. [**D3DX11 \_ Pass \_ DESC**](d3dx11-pass-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="a2e1b-112">A pointer to a pass description (see [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2e1b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2e1b-113">Return value</span></span>

<span data-ttu-id="a2e1b-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2e1b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2e1b-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a2e1b-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2e1b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a2e1b-116">Remarks</span></span>

<span data-ttu-id="a2e1b-117">Проход — это блок кода, который задает состояние визуализации и шейдеры (которые, в свою очередь, устанавливают буферы констант, пробы и текстуры).</span><span class="sxs-lookup"><span data-stu-id="a2e1b-117">A pass is a block of code that sets render state and shaders (which in turn sets constant buffers, samplers and textures).</span></span> <span data-ttu-id="a2e1b-118">Прием эффектов содержит один или несколько проходов.</span><span class="sxs-lookup"><span data-stu-id="a2e1b-118">An effect technique contains one or more passes.</span></span>

> [!Note]  
> <span data-ttu-id="a2e1b-119">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="a2e1b-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a2e1b-120">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="a2e1b-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a2e1b-121">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a2e1b-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2e1b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a2e1b-122">Requirements</span></span>



| <span data-ttu-id="a2e1b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a2e1b-123">Requirement</span></span> | <span data-ttu-id="a2e1b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a2e1b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e1b-125">Header</span><span class="sxs-lookup"><span data-stu-id="a2e1b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a2e1b-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2e1b-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a2e1b-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2e1b-127">Library</span></span><br/> | <dl> <span data-ttu-id="a2e1b-128"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="a2e1b-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2e1b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2e1b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2e1b-130">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="a2e1b-130">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





