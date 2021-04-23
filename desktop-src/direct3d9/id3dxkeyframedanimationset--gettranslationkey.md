---
description: Получение сведений о переводе для определенного ключевого кадра в наборе анимации.
ms.assetid: 757af408-8a9c-4294-9343-91f52d4cc1ab
title: 'Метод ID3DXKeyframedAnimationSet:: Жеттранслатионкэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f61d1caecb46477d16be4367588ab5609bfd6224
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713947"
---
# <a name="id3dxkeyframedanimationsetgettranslationkey-method"></a><span data-ttu-id="d3b69-103">Метод ID3DXKeyframedAnimationSet:: Жеттранслатионкэй</span><span class="sxs-lookup"><span data-stu-id="d3b69-103">ID3DXKeyframedAnimationSet::GetTranslationKey method</span></span>

<span data-ttu-id="d3b69-104">Получение сведений о переводе для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="d3b69-104">Get translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b69-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3b69-105">Syntax</span></span>


```C++
HRESULT GetTranslationKey(
  [in]  UINT              Animation,
  [in]  UINT              Key,
  [out] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="d3b69-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3b69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b69-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d3b69-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b69-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3b69-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3b69-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="d3b69-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="d3b69-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d3b69-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b69-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3b69-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3b69-112">Ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="d3b69-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="d3b69-113">*птранслатионкэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d3b69-113">*pTranslationKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b69-114">Тип: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="d3b69-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="d3b69-115">Указатель на сведения о повороте.</span><span class="sxs-lookup"><span data-stu-id="d3b69-115">Pointer to the rotation information.</span></span> <span data-ttu-id="d3b69-116">См. раздел [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="d3b69-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b69-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3b69-117">Return value</span></span>

<span data-ttu-id="d3b69-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3b69-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3b69-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="d3b69-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d3b69-120">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="d3b69-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b69-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d3b69-121">Requirements</span></span>



| <span data-ttu-id="d3b69-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d3b69-122">Requirement</span></span> | <span data-ttu-id="d3b69-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d3b69-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b69-124">Header</span><span class="sxs-lookup"><span data-stu-id="d3b69-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d3b69-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3b69-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d3b69-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d3b69-126">Library</span></span><br/> | <dl> <span data-ttu-id="d3b69-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3b69-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3b69-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3b69-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b69-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="d3b69-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
