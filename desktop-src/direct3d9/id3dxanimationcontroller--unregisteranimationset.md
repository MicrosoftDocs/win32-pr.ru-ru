---
description: Удаляет набор эффектов анимации из контроллера анимации.
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: 'Метод ID3DXAnimationController:: Унрегистераниматионсет (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35c70552f16daac6d2cfed5cbccf268179526ae1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694330"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a><span data-ttu-id="53bdf-103">Метод ID3DXAnimationController:: Унрегистераниматионсет</span><span class="sxs-lookup"><span data-stu-id="53bdf-103">ID3DXAnimationController::UnregisterAnimationSet method</span></span>

<span data-ttu-id="53bdf-104">Удаляет набор эффектов анимации из контроллера анимации.</span><span class="sxs-lookup"><span data-stu-id="53bdf-104">Removes an animation set from the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="53bdf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53bdf-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="53bdf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53bdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53bdf-107">*панимсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53bdf-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53bdf-108">Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="53bdf-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="53bdf-109">Указатель на удаляемый набор анимации [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="53bdf-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53bdf-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53bdf-110">Return value</span></span>

<span data-ttu-id="53bdf-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53bdf-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53bdf-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="53bdf-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="53bdf-113">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="53bdf-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="53bdf-114">Требования</span><span class="sxs-lookup"><span data-stu-id="53bdf-114">Requirements</span></span>



| <span data-ttu-id="53bdf-115">Требование</span><span class="sxs-lookup"><span data-stu-id="53bdf-115">Requirement</span></span> | <span data-ttu-id="53bdf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="53bdf-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53bdf-117">Header</span><span class="sxs-lookup"><span data-stu-id="53bdf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="53bdf-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="53bdf-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="53bdf-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53bdf-119">Library</span></span><br/> | <dl> <span data-ttu-id="53bdf-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53bdf-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53bdf-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53bdf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53bdf-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="53bdf-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




