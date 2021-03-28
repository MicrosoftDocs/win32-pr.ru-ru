---
title: Метод ID3DX11Effect-desc (D3dx11effect. h)
description: Получение описания воздействия.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- Метод DESC Direct3D 11
- Метод DESC Direct3D 11, интерфейс ID3DX11Effect
- ID3DX11Effect интерфейс Direct3D 11, метод DESC
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587cde43ec2d9136bab5884691c99321d1492835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998633"
---
# <a name="id3dx11effectgetdesc-method"></a><span data-ttu-id="59fb3-106">Метод ID3DX11Effect:: DESC</span><span class="sxs-lookup"><span data-stu-id="59fb3-106">ID3DX11Effect::GetDesc method</span></span>

<span data-ttu-id="59fb3-107">Получение описания воздействия.</span><span class="sxs-lookup"><span data-stu-id="59fb3-107">Get an effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="59fb3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59fb3-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="59fb3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="59fb3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59fb3-110">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="59fb3-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="59fb3-111">Тип: **[ **D3DX11 \_ Effect, \_ DESC**](d3dx11-effect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="59fb3-111">Type: **[**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)\***</span></span>

<span data-ttu-id="59fb3-112">Указатель на описание действия (см. [**D3DX11 \_ Effect \_ DESC**](d3dx11-effect-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="59fb3-112">A pointer to an effect description (see [**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59fb3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59fb3-113">Return value</span></span>

<span data-ttu-id="59fb3-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59fb3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59fb3-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="59fb3-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="59fb3-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="59fb3-116">Remarks</span></span>

<span data-ttu-id="59fb3-117">Описание действия содержит основные сведения о таких последствиях, как содержащиеся в нем методы и ресурсы постоянного буфера.</span><span class="sxs-lookup"><span data-stu-id="59fb3-117">An effect description contains basic information about an effect such as the techniques it contains and the constant buffer resources it requires.</span></span>

> [!Note]  
> <span data-ttu-id="59fb3-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="59fb3-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="59fb3-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="59fb3-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="59fb3-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="59fb3-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="59fb3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="59fb3-121">Requirements</span></span>



| <span data-ttu-id="59fb3-122">Требование</span><span class="sxs-lookup"><span data-stu-id="59fb3-122">Requirement</span></span> | <span data-ttu-id="59fb3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="59fb3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59fb3-124">Header</span><span class="sxs-lookup"><span data-stu-id="59fb3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="59fb3-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="59fb3-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="59fb3-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59fb3-126">Library</span></span><br/> | <dl> <span data-ttu-id="59fb3-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="59fb3-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59fb3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59fb3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59fb3-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="59fb3-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





