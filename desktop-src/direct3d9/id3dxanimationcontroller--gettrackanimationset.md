---
description: Возвращает набор анимации для данной записи.
ms.assetid: d40669ac-c391-4912-82d6-28c366a0f1dc
title: 'Метод ID3DXAnimationController:: Жеттракканиматионсет (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7ba397fb876d94aa48f635785737ab0448ecef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000432"
---
# <a name="id3dxanimationcontrollergettrackanimationset-method"></a><span data-ttu-id="bf39b-103">Метод ID3DXAnimationController:: Жеттракканиматионсет</span><span class="sxs-lookup"><span data-stu-id="bf39b-103">ID3DXAnimationController::GetTrackAnimationSet method</span></span>

<span data-ttu-id="bf39b-104">Возвращает набор анимации для данной записи.</span><span class="sxs-lookup"><span data-stu-id="bf39b-104">Gets the animation set for the given track.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf39b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf39b-105">Syntax</span></span>


```C++
HRESULT GetTrackAnimationSet(
  [in]  UINT               Track,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="bf39b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf39b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf39b-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf39b-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf39b-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf39b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf39b-109">Идентификатор трассировки.</span><span class="sxs-lookup"><span data-stu-id="bf39b-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bf39b-110">*ппанимсет* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf39b-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf39b-111">Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf39b-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="bf39b-112">Указатель на набор анимации [**ID3DXAnimationSet**](id3dxanimationset.md) для данной записи.</span><span class="sxs-lookup"><span data-stu-id="bf39b-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set for the given track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf39b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf39b-113">Return value</span></span>

<span data-ttu-id="bf39b-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf39b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf39b-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="bf39b-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bf39b-116">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bf39b-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf39b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bf39b-117">Requirements</span></span>



| <span data-ttu-id="bf39b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bf39b-118">Requirement</span></span> | <span data-ttu-id="bf39b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bf39b-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf39b-120">Header</span><span class="sxs-lookup"><span data-stu-id="bf39b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bf39b-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf39b-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bf39b-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf39b-122">Library</span></span><br/> | <dl> <span data-ttu-id="bf39b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf39b-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf39b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf39b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf39b-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="bf39b-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
