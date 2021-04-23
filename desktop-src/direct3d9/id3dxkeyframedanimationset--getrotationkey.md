---
description: Получение сведений о повороте для определенного ключевого кадра в наборе анимации.
ms.assetid: d62b8d5e-328e-4227-b2e8-cb6e5ccc4b3f
title: 'Метод ID3DXKeyframedAnimationSet:: Жетротатионкэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f5bf30eaf261e4baa032ed1411b3d70bddc706c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821437"
---
# <a name="id3dxkeyframedanimationsetgetrotationkey-method"></a><span data-ttu-id="83776-103">Метод ID3DXKeyframedAnimationSet:: Жетротатионкэй</span><span class="sxs-lookup"><span data-stu-id="83776-103">ID3DXKeyframedAnimationSet::GetRotationKey method</span></span>

<span data-ttu-id="83776-104">Получение сведений о повороте для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="83776-104">Get rotation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="83776-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83776-105">Syntax</span></span>


```C++
HRESULT GetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="83776-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83776-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83776-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83776-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83776-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83776-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83776-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="83776-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="83776-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83776-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83776-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83776-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83776-112">Ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="83776-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="83776-113">*протатионкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83776-113">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83776-114">Тип: **[ **LPD3DXKEY \_ кватернион**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="83776-114">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="83776-115">Указатель на данные вращения.</span><span class="sxs-lookup"><span data-stu-id="83776-115">Pointer to the rotation data.</span></span> <span data-ttu-id="83776-116">См. [**D3DXKEY \_ кватернион**](d3dxkey-quaternion.md).</span><span class="sxs-lookup"><span data-stu-id="83776-116">See [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83776-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83776-117">Return value</span></span>

<span data-ttu-id="83776-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83776-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83776-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="83776-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="83776-120">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="83776-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="83776-121">Требования</span><span class="sxs-lookup"><span data-stu-id="83776-121">Requirements</span></span>



| <span data-ttu-id="83776-122">Требование</span><span class="sxs-lookup"><span data-stu-id="83776-122">Requirement</span></span> | <span data-ttu-id="83776-123">Значение</span><span class="sxs-lookup"><span data-stu-id="83776-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83776-124">Header</span><span class="sxs-lookup"><span data-stu-id="83776-124">Header</span></span><br/>  | <dl> <span data-ttu-id="83776-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="83776-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="83776-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83776-126">Library</span></span><br/> | <dl> <span data-ttu-id="83776-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83776-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83776-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83776-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83776-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="83776-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
