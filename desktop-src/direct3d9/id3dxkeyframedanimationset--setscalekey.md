---
description: Установка сведений о масштабе для определенного ключевого кадра в наборе анимации.
ms.assetid: b606e5d3-11c9-4997-ad3c-d3ae21c32e10
title: 'Метод ID3DXKeyframedAnimationSet:: Сетскалекэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12ac4d46a2719e452d44d2da67f178e6146b799b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713941"
---
# <a name="id3dxkeyframedanimationsetsetscalekey-method"></a><span data-ttu-id="4da1a-103">Метод ID3DXKeyframedAnimationSet:: Сетскалекэй</span><span class="sxs-lookup"><span data-stu-id="4da1a-103">ID3DXKeyframedAnimationSet::SetScaleKey method</span></span>

<span data-ttu-id="4da1a-104">Установка сведений о масштабе для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="4da1a-104">Set scale information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4da1a-105">Syntax</span></span>


```C++
HRESULT SetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="4da1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4da1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da1a-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4da1a-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4da1a-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4da1a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4da1a-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="4da1a-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="4da1a-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4da1a-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4da1a-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4da1a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4da1a-112">Ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="4da1a-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="4da1a-113">*пскалекэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4da1a-113">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4da1a-114">Тип: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="4da1a-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="4da1a-115">Указатель на данные шкалы.</span><span class="sxs-lookup"><span data-stu-id="4da1a-115">Pointer to the scale data.</span></span> <span data-ttu-id="4da1a-116">См. раздел [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="4da1a-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da1a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4da1a-117">Return value</span></span>

<span data-ttu-id="4da1a-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4da1a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4da1a-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="4da1a-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4da1a-120">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="4da1a-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da1a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4da1a-121">Requirements</span></span>



| <span data-ttu-id="4da1a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4da1a-122">Requirement</span></span> | <span data-ttu-id="4da1a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4da1a-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4da1a-124">Header</span><span class="sxs-lookup"><span data-stu-id="4da1a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4da1a-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4da1a-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4da1a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4da1a-126">Library</span></span><br/> | <dl> <span data-ttu-id="4da1a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4da1a-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4da1a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4da1a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da1a-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="4da1a-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
