---
description: Установка сведений о повороте для определенного ключевого кадра в наборе анимации.
ms.assetid: b31edc88-0d77-49f3-b4c4-39cd866e1379
title: 'Метод ID3DXKeyframedAnimationSet:: Сетротатионкэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b03a6818a6a59904c3db5b4819775d9e58d4f8ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081932"
---
# <a name="id3dxkeyframedanimationsetsetrotationkey-method"></a><span data-ttu-id="bc22e-103">Метод ID3DXKeyframedAnimationSet:: Сетротатионкэй</span><span class="sxs-lookup"><span data-stu-id="bc22e-103">ID3DXKeyframedAnimationSet::SetRotationKey method</span></span>

<span data-ttu-id="bc22e-104">Установка сведений о повороте для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="bc22e-104">Set rotation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc22e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc22e-105">Syntax</span></span>


```C++
HRESULT SetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="bc22e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc22e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc22e-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc22e-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc22e-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc22e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc22e-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="bc22e-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="bc22e-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc22e-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc22e-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc22e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc22e-112">Ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="bc22e-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="bc22e-113">*протатионкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc22e-113">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc22e-114">Тип: **[ **LPD3DXKEY \_ кватернион**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="bc22e-114">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="bc22e-115">Указатель на данные вращения.</span><span class="sxs-lookup"><span data-stu-id="bc22e-115">Pointer to the rotation data.</span></span> <span data-ttu-id="bc22e-116">См. раздел [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="bc22e-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc22e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc22e-117">Return value</span></span>

<span data-ttu-id="bc22e-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc22e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc22e-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="bc22e-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bc22e-120">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="bc22e-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc22e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bc22e-121">Requirements</span></span>



| <span data-ttu-id="bc22e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bc22e-122">Requirement</span></span> | <span data-ttu-id="bc22e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bc22e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc22e-124">Header</span><span class="sxs-lookup"><span data-stu-id="bc22e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bc22e-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc22e-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bc22e-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bc22e-126">Library</span></span><br/> | <dl> <span data-ttu-id="bc22e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc22e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc22e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc22e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc22e-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="bc22e-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
