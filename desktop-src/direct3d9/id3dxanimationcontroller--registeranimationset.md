---
description: Добавляет набор эффектов анимации к контроллеру анимации.
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: 'Метод ID3DXAnimationController:: Регистераниматионсет (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ca70baf55a3dae19422c9026575d75f63eed4bde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713892"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a><span data-ttu-id="36f86-103">Метод ID3DXAnimationController:: Регистераниматионсет</span><span class="sxs-lookup"><span data-stu-id="36f86-103">ID3DXAnimationController::RegisterAnimationSet method</span></span>

<span data-ttu-id="36f86-104">Добавляет набор эффектов анимации к контроллеру анимации.</span><span class="sxs-lookup"><span data-stu-id="36f86-104">Adds an animation set to the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f86-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36f86-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="36f86-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36f86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36f86-107">*панимсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36f86-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36f86-108">Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="36f86-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="36f86-109">Указатель на добавляемый набор анимации [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="36f86-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36f86-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36f86-110">Return value</span></span>

<span data-ttu-id="36f86-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36f86-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36f86-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="36f86-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="36f86-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="36f86-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f86-114">Требования</span><span class="sxs-lookup"><span data-stu-id="36f86-114">Requirements</span></span>



| <span data-ttu-id="36f86-115">Требование</span><span class="sxs-lookup"><span data-stu-id="36f86-115">Requirement</span></span> | <span data-ttu-id="36f86-116">Значение</span><span class="sxs-lookup"><span data-stu-id="36f86-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36f86-117">Header</span><span class="sxs-lookup"><span data-stu-id="36f86-117">Header</span></span><br/>  | <dl> <span data-ttu-id="36f86-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="36f86-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="36f86-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36f86-119">Library</span></span><br/> | <dl> <span data-ttu-id="36f86-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36f86-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36f86-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36f86-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f86-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="36f86-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




