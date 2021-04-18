---
description: Возвращает значения масштаба, вращения и перевода набора анимации.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'Метод ID3DXAnimationSet:: Жетсрт (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b70243dd9aa2f304d80eaff2e2cc7695dad43379
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714001"
---
# <a name="id3dxanimationsetgetsrt-method"></a><span data-ttu-id="71aea-103">Метод ID3DXAnimationSet:: Жетсрт</span><span class="sxs-lookup"><span data-stu-id="71aea-103">ID3DXAnimationSet::GetSRT method</span></span>

<span data-ttu-id="71aea-104">Возвращает значения масштаба, вращения и перевода набора анимации.</span><span class="sxs-lookup"><span data-stu-id="71aea-104">Gets the scale, rotation, and translation values of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="71aea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71aea-105">Syntax</span></span>


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="71aea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71aea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71aea-107">*Периодикпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71aea-107">*PeriodicPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71aea-108">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71aea-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71aea-109">Расположение набора анимации.</span><span class="sxs-lookup"><span data-stu-id="71aea-109">Position of the animation set.</span></span> <span data-ttu-id="71aea-110">Эту точку можно получить путем вызова [**ID3DXAnimationSet:: жетпериодикпоситион**](id3dxanimationset--getperiodicposition.md).</span><span class="sxs-lookup"><span data-stu-id="71aea-110">The position can be obtained by calling [**ID3DXAnimationSet::GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span></span>

</dd> <dt>

<span data-ttu-id="71aea-111">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71aea-111">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71aea-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71aea-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71aea-113">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="71aea-113">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="71aea-114">*пскале* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="71aea-114">*pScale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71aea-115">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="71aea-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="71aea-116">Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , описывающий масштаб набора анимации.</span><span class="sxs-lookup"><span data-stu-id="71aea-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="71aea-117"> \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="71aea-117">*pRotation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71aea-118">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="71aea-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="71aea-119">Указатель на кватернион [**D3DXQUATERNION**](d3dxquaternion.md) , описывающий поворот набора анимации.</span><span class="sxs-lookup"><span data-stu-id="71aea-119">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="71aea-120">*птранслатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="71aea-120">*pTranslation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71aea-121">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="71aea-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="71aea-122">Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , описывающий перевод набора анимации.</span><span class="sxs-lookup"><span data-stu-id="71aea-122">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71aea-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71aea-123">Return value</span></span>

<span data-ttu-id="71aea-124">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71aea-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71aea-125">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="71aea-125">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="71aea-126">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="71aea-126">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="71aea-127">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке из [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="71aea-127">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71aea-128">Требования</span><span class="sxs-lookup"><span data-stu-id="71aea-128">Requirements</span></span>



| <span data-ttu-id="71aea-129">Требование</span><span class="sxs-lookup"><span data-stu-id="71aea-129">Requirement</span></span> | <span data-ttu-id="71aea-130">Значение</span><span class="sxs-lookup"><span data-stu-id="71aea-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71aea-131">Header</span><span class="sxs-lookup"><span data-stu-id="71aea-131">Header</span></span><br/>  | <dl> <span data-ttu-id="71aea-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="71aea-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="71aea-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71aea-133">Library</span></span><br/> | <dl> <span data-ttu-id="71aea-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71aea-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="71aea-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71aea-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71aea-136">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="71aea-136">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
