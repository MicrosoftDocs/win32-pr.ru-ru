---
description: Удалите данные анимации из набора анимации.
ms.assetid: 9821d21e-fe8f-4742-b4f3-63b2578d29ec
title: 'Метод ID3DXKeyframedAnimationSet:: Унрегистераниматион (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterAnimation
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5ee7718fb73e441daacf9fdaff38499239915e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720981"
---
# <a name="id3dxkeyframedanimationsetunregisteranimation-method"></a><span data-ttu-id="ba47d-103">Метод ID3DXKeyframedAnimationSet:: Унрегистераниматион</span><span class="sxs-lookup"><span data-stu-id="ba47d-103">ID3DXKeyframedAnimationSet::UnregisterAnimation method</span></span>

<span data-ttu-id="ba47d-104">Удалите данные анимации из набора анимации.</span><span class="sxs-lookup"><span data-stu-id="ba47d-104">Remove the animation data from the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba47d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba47d-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimation(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="ba47d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba47d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba47d-107">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba47d-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba47d-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba47d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba47d-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="ba47d-109">The animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba47d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba47d-110">Return value</span></span>

<span data-ttu-id="ba47d-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba47d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba47d-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ba47d-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ba47d-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ba47d-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba47d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ba47d-114">Requirements</span></span>



| <span data-ttu-id="ba47d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ba47d-115">Requirement</span></span> | <span data-ttu-id="ba47d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ba47d-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba47d-117">Header</span><span class="sxs-lookup"><span data-stu-id="ba47d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ba47d-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba47d-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ba47d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba47d-119">Library</span></span><br/> | <dl> <span data-ttu-id="ba47d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba47d-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ba47d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba47d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba47d-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="ba47d-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
