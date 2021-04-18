---
title: Метод ID3DX11EffectPass Компутестатеблоккмаск (D3dx11effect. h)
description: Создание маски для разрешения или запрета изменений состояния.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Метод Компутестатеблоккмаск Direct3D 11
- Метод Компутестатеблоккмаск Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Компутестатеблоккмаск
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc5cb32ce9e9644d7d5b62868bfa99f150cc94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987038"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a><span data-ttu-id="91c33-106">Метод ID3DX11EffectPass:: Компутестатеблоккмаск</span><span class="sxs-lookup"><span data-stu-id="91c33-106">ID3DX11EffectPass::ComputeStateBlockMask method</span></span>

<span data-ttu-id="91c33-107">Создание маски для разрешения или запрета изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="91c33-107">Generate a mask for allowing/preventing state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c33-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91c33-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="91c33-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="91c33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c33-110">*пстатеблоккмаск*</span><span class="sxs-lookup"><span data-stu-id="91c33-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="91c33-111">Тип: **[ **D3DX11 \_ \_ \_ Маска блока состояния**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="91c33-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="91c33-112">Указатель на маску блока State (см. раздел [**\_ \_ \_ Маска блока состояния D3DX11**](d3dx11-state-block-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="91c33-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c33-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91c33-113">Return value</span></span>

<span data-ttu-id="91c33-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91c33-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91c33-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="91c33-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91c33-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="91c33-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="91c33-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="91c33-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="91c33-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="91c33-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="91c33-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="91c33-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91c33-120">Требования</span><span class="sxs-lookup"><span data-stu-id="91c33-120">Requirements</span></span>



| <span data-ttu-id="91c33-121">Требование</span><span class="sxs-lookup"><span data-stu-id="91c33-121">Requirement</span></span> | <span data-ttu-id="91c33-122">Значение</span><span class="sxs-lookup"><span data-stu-id="91c33-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c33-123">Header</span><span class="sxs-lookup"><span data-stu-id="91c33-123">Header</span></span><br/>  | <dl> <span data-ttu-id="91c33-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="91c33-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="91c33-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="91c33-125">Library</span></span><br/> | <dl> <span data-ttu-id="91c33-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="91c33-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c33-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91c33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c33-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="91c33-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





