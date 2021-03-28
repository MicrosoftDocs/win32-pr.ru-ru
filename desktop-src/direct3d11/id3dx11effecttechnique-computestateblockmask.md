---
title: Метод ID3DX11EffectTechnique Компутестатеблоккмаск (D3dx11effect. h)
description: Вычислите маску блока состояния, чтобы разрешить или запретить изменение состояния.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- Метод Компутестатеблоккмаск Direct3D 11
- Метод Компутестатеблоккмаск Direct3D 11, интерфейс ID3DX11EffectTechnique
- Интерфейс ID3DX11EffectTechnique Direct3D 11, метод Компутестатеблоккмаск
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d15a159c15f35d530559b4ad6d84dd815e5964a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273723"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a><span data-ttu-id="2c2de-106">Метод ID3DX11EffectTechnique:: Компутестатеблоккмаск</span><span class="sxs-lookup"><span data-stu-id="2c2de-106">ID3DX11EffectTechnique::ComputeStateBlockMask method</span></span>

<span data-ttu-id="2c2de-107">Вычислите маску блока состояния, чтобы разрешить или запретить изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="2c2de-107">Compute a state-block mask to allow/prevent state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c2de-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c2de-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="2c2de-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c2de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c2de-110">*пстатеблоккмаск*</span><span class="sxs-lookup"><span data-stu-id="2c2de-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="2c2de-111">Тип: **[ **D3DX11 \_ \_ \_ Маска блока состояния**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c2de-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="2c2de-112">Указатель на маску блока State (см. раздел [**\_ \_ \_ Маска блока состояния D3DX11**](d3dx11-state-block-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="2c2de-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c2de-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c2de-113">Return value</span></span>

<span data-ttu-id="2c2de-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c2de-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c2de-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2c2de-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c2de-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2c2de-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2c2de-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="2c2de-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2c2de-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="2c2de-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2c2de-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2c2de-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c2de-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2c2de-120">Requirements</span></span>



| <span data-ttu-id="2c2de-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2c2de-121">Requirement</span></span> | <span data-ttu-id="2c2de-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2c2de-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c2de-123">Header</span><span class="sxs-lookup"><span data-stu-id="2c2de-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2c2de-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c2de-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2c2de-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c2de-125">Library</span></span><br/> | <dl> <span data-ttu-id="2c2de-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="2c2de-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c2de-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c2de-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c2de-128">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="2c2de-128">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

 





