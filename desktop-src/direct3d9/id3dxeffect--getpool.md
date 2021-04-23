---
description: Возвращает указатель на пул общих параметров.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: Метод ID3DXEffect::-Pool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 18a35e9bc0a596cb88da6d4c1faf10941fbce8a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000324"
---
# <a name="id3dxeffectgetpool-method"></a><span data-ttu-id="487f2-103">Метод ID3DXEffect:: pool</span><span class="sxs-lookup"><span data-stu-id="487f2-103">ID3DXEffect::GetPool method</span></span>

<span data-ttu-id="487f2-104">Возвращает указатель на пул общих параметров.</span><span class="sxs-lookup"><span data-stu-id="487f2-104">Gets a pointer to the pool of shared parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="487f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="487f2-105">Syntax</span></span>


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="487f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="487f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="487f2-107">*пппул* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="487f2-107">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="487f2-108">Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="487f2-108">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="487f2-109">Указатель на объект [**ID3DXEffectPool**](id3dxeffectpool.md) .</span><span class="sxs-lookup"><span data-stu-id="487f2-109">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="487f2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="487f2-110">Return value</span></span>

<span data-ttu-id="487f2-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="487f2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="487f2-112">Этот метод всегда возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="487f2-112">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="487f2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="487f2-113">Remarks</span></span>

<span data-ttu-id="487f2-114">Пулы содержат общие параметры между различными эффектами.</span><span class="sxs-lookup"><span data-stu-id="487f2-114">Pools contain shared parameters between effects.</span></span> <span data-ttu-id="487f2-115">См. раздел [клонирование и совместное использование (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="487f2-115">See [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="487f2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="487f2-116">Requirements</span></span>



| <span data-ttu-id="487f2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="487f2-117">Requirement</span></span> | <span data-ttu-id="487f2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="487f2-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="487f2-119">Header</span><span class="sxs-lookup"><span data-stu-id="487f2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="487f2-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="487f2-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="487f2-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="487f2-121">Library</span></span><br/> | <dl> <span data-ttu-id="487f2-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="487f2-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="487f2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="487f2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="487f2-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="487f2-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




