---
description: Задание сведений о переводе для определенного ключевого кадра в наборе анимации.
ms.assetid: 4a926c0f-6d57-48d4-bb3b-60766fc78e40
title: 'Метод ID3DXKeyframedAnimationSet:: Сеттранслатионкэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bdfb8fb02a2b06dc797317d35cc14e75bd6f221
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713940"
---
# <a name="id3dxkeyframedanimationsetsettranslationkey-method"></a><span data-ttu-id="b90be-103">Метод ID3DXKeyframedAnimationSet:: Сеттранслатионкэй</span><span class="sxs-lookup"><span data-stu-id="b90be-103">ID3DXKeyframedAnimationSet::SetTranslationKey method</span></span>

<span data-ttu-id="b90be-104">Задание сведений о переводе для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="b90be-104">Set translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="b90be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b90be-105">Syntax</span></span>


```C++
HRESULT SetTranslationKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="b90be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b90be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b90be-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b90be-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b90be-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b90be-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b90be-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="b90be-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="b90be-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b90be-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b90be-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b90be-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b90be-112">Ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="b90be-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="b90be-113">*птранслатионкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b90be-113">*pTranslationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b90be-114">Тип: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="b90be-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="b90be-115">Указатель на данные перевода.</span><span class="sxs-lookup"><span data-stu-id="b90be-115">Pointer to the translation data.</span></span> <span data-ttu-id="b90be-116">См. раздел [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="b90be-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b90be-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b90be-117">Return value</span></span>

<span data-ttu-id="b90be-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b90be-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b90be-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="b90be-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b90be-120">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b90be-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b90be-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b90be-121">Requirements</span></span>



| <span data-ttu-id="b90be-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b90be-122">Requirement</span></span> | <span data-ttu-id="b90be-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b90be-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b90be-124">Header</span><span class="sxs-lookup"><span data-stu-id="b90be-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b90be-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b90be-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b90be-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b90be-126">Library</span></span><br/> | <dl> <span data-ttu-id="b90be-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b90be-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b90be-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b90be-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90be-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="b90be-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
