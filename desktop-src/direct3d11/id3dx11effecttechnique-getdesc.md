---
title: Метод ID3DX11EffectTechnique-desc (D3dx11effect. h)
description: Получите описание метода.
ms.assetid: ed82d873-0540-4aa8-ac0f-198852b886ad
keywords:
- Метод DESC Direct3D 11
- Метод DESC Direct3D 11, интерфейс ID3DX11EffectTechnique
- ID3DX11EffectTechnique интерфейс Direct3D 11, метод DESC
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b847bd8381ec7d190931c04e5940f713676ff0b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998354"
---
# <a name="id3dx11effecttechniquegetdesc-method"></a><span data-ttu-id="2b782-106">Метод ID3DX11EffectTechnique:: DESC</span><span class="sxs-lookup"><span data-stu-id="2b782-106">ID3DX11EffectTechnique::GetDesc method</span></span>

<span data-ttu-id="2b782-107">Получите описание метода.</span><span class="sxs-lookup"><span data-stu-id="2b782-107">Get a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b782-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b782-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_TECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="2b782-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b782-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b782-110">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="2b782-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="2b782-111">Тип: **[ **D3DX11 \_ техника \_ DESC**](d3dx11-technique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b782-111">Type: **[**D3DX11\_TECHNIQUE\_DESC**](d3dx11-technique-desc.md)\***</span></span>

<span data-ttu-id="2b782-112">Указатель на описание метода (см. [**метод D3DX11 \_ \_ DESC**](d3dx11-technique-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="2b782-112">A pointer to a technique description (see [**D3DX11\_TECHNIQUE\_DESC**](d3dx11-technique-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b782-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b782-113">Return value</span></span>

<span data-ttu-id="2b782-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b782-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b782-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2b782-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2b782-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b782-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2b782-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="2b782-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2b782-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="2b782-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2b782-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2b782-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2b782-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2b782-120">Requirements</span></span>



| <span data-ttu-id="2b782-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2b782-121">Requirement</span></span> | <span data-ttu-id="2b782-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2b782-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b782-123">Header</span><span class="sxs-lookup"><span data-stu-id="2b782-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2b782-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b782-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2b782-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b782-125">Library</span></span><br/> | <dl> <span data-ttu-id="2b782-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="2b782-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b782-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b782-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b782-128">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="2b782-128">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

 





