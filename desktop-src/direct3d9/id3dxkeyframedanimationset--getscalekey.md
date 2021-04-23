---
description: Получение сведений о масштабе для определенного ключевого кадра в наборе анимации.
ms.assetid: 7f4a0bf3-2922-4fd7-bb85-b387d3e983a7
title: 'Метод ID3DXKeyframedAnimationSet:: Жетскалекэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58cbd432404fcd511140a7368999161f5e44f77f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355723"
---
# <a name="id3dxkeyframedanimationsetgetscalekey-method"></a><span data-ttu-id="cf504-103">Метод ID3DXKeyframedAnimationSet:: Жетскалекэй</span><span class="sxs-lookup"><span data-stu-id="cf504-103">ID3DXKeyframedAnimationSet::GetScaleKey method</span></span>

<span data-ttu-id="cf504-104">Получение сведений о масштабе для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="cf504-104">Get scale information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf504-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf504-105">Syntax</span></span>


```C++
HRESULT GetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="cf504-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf504-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf504-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf504-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf504-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf504-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf504-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="cf504-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="cf504-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf504-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf504-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf504-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf504-112">Ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="cf504-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="cf504-113">*пскалекэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf504-113">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf504-114">Тип: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="cf504-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="cf504-115">Указатель на данные шкалы.</span><span class="sxs-lookup"><span data-stu-id="cf504-115">Pointer to the scale data.</span></span> <span data-ttu-id="cf504-116">См. раздел [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="cf504-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf504-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf504-117">Return value</span></span>

<span data-ttu-id="cf504-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cf504-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cf504-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="cf504-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cf504-120">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="cf504-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf504-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cf504-121">Requirements</span></span>



| <span data-ttu-id="cf504-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cf504-122">Requirement</span></span> | <span data-ttu-id="cf504-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cf504-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf504-124">Header</span><span class="sxs-lookup"><span data-stu-id="cf504-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cf504-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf504-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="cf504-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cf504-126">Library</span></span><br/> | <dl> <span data-ttu-id="cf504-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf504-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf504-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf504-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf504-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="cf504-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
