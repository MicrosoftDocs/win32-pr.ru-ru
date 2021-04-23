---
description: Заполняет массив данными ключа шкалы, используемыми для анимации ключевых кадров.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'Метод ID3DXKeyframedAnimationSet:: Жетскалекэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88c907bc9b45b1203917b092f565096be3ed1fb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713949"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a><span data-ttu-id="5d626-103">Метод ID3DXKeyframedAnimationSet:: Жетскалекэйс</span><span class="sxs-lookup"><span data-stu-id="5d626-103">ID3DXKeyframedAnimationSet::GetScaleKeys method</span></span>

<span data-ttu-id="5d626-104">Заполняет массив данными ключа шкалы, используемыми для анимации ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="5d626-104">Fills an array with scale key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d626-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d626-105">Syntax</span></span>


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="5d626-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d626-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d626-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d626-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d626-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d626-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d626-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="5d626-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="5d626-110">*пскалекэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d626-110">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d626-111">Тип: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="5d626-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="5d626-112">Указатель на выделенный пользователем массив векторов [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) , который метод должен заполнять данными шкалы анимации.</span><span class="sxs-lookup"><span data-stu-id="5d626-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation scale data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d626-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d626-113">Return value</span></span>

<span data-ttu-id="5d626-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d626-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d626-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="5d626-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5d626-116">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="5d626-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d626-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5d626-117">Requirements</span></span>



| <span data-ttu-id="5d626-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5d626-118">Requirement</span></span> | <span data-ttu-id="5d626-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5d626-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d626-120">Header</span><span class="sxs-lookup"><span data-stu-id="5d626-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5d626-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d626-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5d626-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d626-122">Library</span></span><br/> | <dl> <span data-ttu-id="5d626-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d626-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d626-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d626-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d626-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5d626-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="5d626-126">**ID3DXKeyframedAnimationSet:: Жетнумскалекэйс**</span><span class="sxs-lookup"><span data-stu-id="5d626-126">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
