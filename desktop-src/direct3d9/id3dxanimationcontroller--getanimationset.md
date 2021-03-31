---
description: Возвращает набор анимации.
ms.assetid: 61785f60-82c1-4ddc-b4cd-2e7f665cfe8c
title: 'Метод ID3DXAnimationController:: Animation (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c21f073b74d1ab7dac09ddd8bfb3d6be543e122a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157211"
---
# <a name="id3dxanimationcontrollergetanimationset-method"></a><span data-ttu-id="35127-103">Метод ID3DXAnimationController:: Animation</span><span class="sxs-lookup"><span data-stu-id="35127-103">ID3DXAnimationController::GetAnimationSet method</span></span>

<span data-ttu-id="35127-104">Возвращает набор анимации.</span><span class="sxs-lookup"><span data-stu-id="35127-104">Gets an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="35127-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35127-105">Syntax</span></span>


```C++
HRESULT GetAnimationSet(
  [in]  UINT               Index,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="35127-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="35127-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35127-107">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35127-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35127-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35127-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35127-109">Индекс набора анимации.</span><span class="sxs-lookup"><span data-stu-id="35127-109">Index of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="35127-110">*ппанимсет* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="35127-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35127-111">Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="35127-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="35127-112">Указатель на набор эффектов анимации [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="35127-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35127-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35127-113">Return value</span></span>

<span data-ttu-id="35127-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35127-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35127-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="35127-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="35127-116">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="35127-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="35127-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35127-117">Remarks</span></span>

<span data-ttu-id="35127-118">Контроллер анимации содержит массив наборов анимации.</span><span class="sxs-lookup"><span data-stu-id="35127-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="35127-119">Этот метод возвращает один из них по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="35127-119">This method returns one of them at the given index.</span></span>

## <a name="requirements"></a><span data-ttu-id="35127-120">Требования</span><span class="sxs-lookup"><span data-stu-id="35127-120">Requirements</span></span>



| <span data-ttu-id="35127-121">Требование</span><span class="sxs-lookup"><span data-stu-id="35127-121">Requirement</span></span> | <span data-ttu-id="35127-122">Значение</span><span class="sxs-lookup"><span data-stu-id="35127-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35127-123">Header</span><span class="sxs-lookup"><span data-stu-id="35127-123">Header</span></span><br/>  | <dl> <span data-ttu-id="35127-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="35127-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="35127-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="35127-125">Library</span></span><br/> | <dl> <span data-ttu-id="35127-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35127-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35127-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35127-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35127-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="35127-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
