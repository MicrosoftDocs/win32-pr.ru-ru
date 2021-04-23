---
description: Зарегистрируйте данные опорного кадра шкалы, вращения и перевода (SRT) для анимации.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'Метод ID3DXKeyframedAnimationSet:: Регистераниматионсрткэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713943"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a><span data-ttu-id="9a922-103">Метод ID3DXKeyframedAnimationSet:: Регистераниматионсрткэйс</span><span class="sxs-lookup"><span data-stu-id="9a922-103">ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys method</span></span>

<span data-ttu-id="9a922-104">Зарегистрируйте данные опорного кадра шкалы, вращения и перевода (SRT) для анимации.</span><span class="sxs-lookup"><span data-stu-id="9a922-104">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a922-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a922-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a><span data-ttu-id="9a922-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a922-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a922-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a922-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a922-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a922-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a922-109">Указатель на имя анимации.</span><span class="sxs-lookup"><span data-stu-id="9a922-109">Pointer to the animation name.</span></span>

</dd> <dt>

<span data-ttu-id="9a922-110">*Нумскалекэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a922-110">*NumScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a922-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a922-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a922-112">Количество ключей масштабирования.</span><span class="sxs-lookup"><span data-stu-id="9a922-112">Number of scale keys.</span></span>

</dd> <dt>

<span data-ttu-id="9a922-113">*Нумротатионкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a922-113">*NumRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a922-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a922-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a922-115">Число ключей вращения.</span><span class="sxs-lookup"><span data-stu-id="9a922-115">Number of rotation keys.</span></span>

</dd> <dt>

<span data-ttu-id="9a922-116">*Нумтранслатионкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a922-116">*NumTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a922-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a922-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a922-118">Число ключей перевода.</span><span class="sxs-lookup"><span data-stu-id="9a922-118">Number of translation keys.</span></span>

</dd> <dt>

<span data-ttu-id="9a922-119">*пскалекэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a922-119">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a922-120">Тип: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9a922-120">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="9a922-121">Адрес указателя на выделенный пользователем массив векторов [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) , который метод заполняет данными масштабирования.</span><span class="sxs-lookup"><span data-stu-id="9a922-121">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with scale data.</span></span>

</dd> <dt>

<span data-ttu-id="9a922-122">*протатионкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a922-122">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a922-123">Тип: **const [**LPD3DXKEY \_ кватернион**](d3dxkey-quaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="9a922-123">Type: **const [**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)\***</span></span>

<span data-ttu-id="9a922-124">Адрес указателя на выделенный пользователем массив [**D3DXKEY \_ кватернион**](d3dxkey-quaternion.md) , который заполняется методом данными вращения.</span><span class="sxs-lookup"><span data-stu-id="9a922-124">Address of a pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method fills with rotation data.</span></span>

</dd> <dt>

<span data-ttu-id="9a922-125">*птранслатионкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a922-125">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a922-126">Тип: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9a922-126">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="9a922-127">Адрес указателя на выделенный пользователем массив [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) векторов, который заполняется методом данными перевода.</span><span class="sxs-lookup"><span data-stu-id="9a922-127">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with translation data.</span></span>

</dd> <dt>

<span data-ttu-id="9a922-128">*паниматиониндекс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9a922-128">*pAnimationIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a922-129">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a922-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9a922-130">Возвращает индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="9a922-130">Returns the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a922-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a922-131">Return value</span></span>

<span data-ttu-id="9a922-132">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a922-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a922-133">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="9a922-133">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9a922-134">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="9a922-134">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="9a922-135">Требования</span><span class="sxs-lookup"><span data-stu-id="9a922-135">Requirements</span></span>



| <span data-ttu-id="9a922-136">Требование</span><span class="sxs-lookup"><span data-stu-id="9a922-136">Requirement</span></span> | <span data-ttu-id="9a922-137">Значение</span><span class="sxs-lookup"><span data-stu-id="9a922-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a922-138">Header</span><span class="sxs-lookup"><span data-stu-id="9a922-138">Header</span></span><br/>  | <dl> <span data-ttu-id="9a922-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a922-139"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9a922-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9a922-140">Library</span></span><br/> | <dl> <span data-ttu-id="9a922-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a922-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9a922-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a922-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a922-143">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="9a922-143">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="9a922-144">**ID3DXKeyframedAnimationSet:: Жетнумскалекэйс**</span><span class="sxs-lookup"><span data-stu-id="9a922-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[<span data-ttu-id="9a922-145">**ID3DXKeyframedAnimationSet:: Жетнумротатионкэйс**</span><span class="sxs-lookup"><span data-stu-id="9a922-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[<span data-ttu-id="9a922-146">**ID3DXKeyframedAnimationSet:: Жетнумтранслатионкэйс**</span><span class="sxs-lookup"><span data-stu-id="9a922-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
