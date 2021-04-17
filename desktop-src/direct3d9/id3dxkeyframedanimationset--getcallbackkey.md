---
description: Возвращает сведения о конкретном обратном вызове в наборе анимации.
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: 'Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95a3f5a97b84862a66d18b60a3776e183df36444
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703983"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a><span data-ttu-id="096f9-103">Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэй</span><span class="sxs-lookup"><span data-stu-id="096f9-103">ID3DXKeyframedAnimationSet::GetCallbackKey method</span></span>

<span data-ttu-id="096f9-104">Возвращает сведения о конкретном обратном вызове в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="096f9-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="096f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="096f9-105">Syntax</span></span>


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="096f9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="096f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="096f9-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="096f9-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="096f9-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="096f9-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="096f9-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="096f9-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="096f9-110">*пкаллбакккэйс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="096f9-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="096f9-111">Тип: **[ **\_ обратный вызов LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="096f9-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="096f9-112">Указатель на [**функцию обратного вызова**](d3dxkey-callback.md).</span><span class="sxs-lookup"><span data-stu-id="096f9-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="096f9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="096f9-113">Return value</span></span>

<span data-ttu-id="096f9-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="096f9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="096f9-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="096f9-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="096f9-116">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="096f9-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="096f9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="096f9-117">Requirements</span></span>



| <span data-ttu-id="096f9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="096f9-118">Requirement</span></span> | <span data-ttu-id="096f9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="096f9-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="096f9-120">Header</span><span class="sxs-lookup"><span data-stu-id="096f9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="096f9-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="096f9-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="096f9-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="096f9-122">Library</span></span><br/> | <dl> <span data-ttu-id="096f9-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="096f9-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="096f9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="096f9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="096f9-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="096f9-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
