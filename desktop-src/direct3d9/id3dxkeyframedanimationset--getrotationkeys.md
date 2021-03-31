---
description: Заполняет массив данными ротации ключей, используемыми для анимации ключевых кадров.
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'Метод ID3DXKeyframedAnimationSet:: Жетротатионкэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821436"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a><span data-ttu-id="e1cc4-103">Метод ID3DXKeyframedAnimationSet:: Жетротатионкэйс</span><span class="sxs-lookup"><span data-stu-id="e1cc4-103">ID3DXKeyframedAnimationSet::GetRotationKeys method</span></span>

<span data-ttu-id="e1cc4-104">Заполняет массив данными ротации ключей, используемыми для анимации ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="e1cc4-104">Fills an array with rotational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1cc4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1cc4-105">Syntax</span></span>


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="e1cc4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1cc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1cc4-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1cc4-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1cc4-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1cc4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1cc4-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="e1cc4-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="e1cc4-110">*протатионкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1cc4-110">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1cc4-111">Тип: **[ **LPD3DXKEY \_ кватернион**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="e1cc4-111">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="e1cc4-112">Указатель на выделенный пользователем массив [**D3DXKEY \_ кватернион**](d3dxkey-quaternion.md) кватернион, который метод заполнит заливкой данными вращения анимации.</span><span class="sxs-lookup"><span data-stu-id="e1cc4-112">Pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method is to fill with animation rotation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1cc4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1cc4-113">Return value</span></span>

<span data-ttu-id="e1cc4-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1cc4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1cc4-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="e1cc4-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e1cc4-116">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e1cc4-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1cc4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e1cc4-117">Requirements</span></span>



| <span data-ttu-id="e1cc4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e1cc4-118">Requirement</span></span> | <span data-ttu-id="e1cc4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e1cc4-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cc4-120">Header</span><span class="sxs-lookup"><span data-stu-id="e1cc4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e1cc4-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1cc4-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e1cc4-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e1cc4-122">Library</span></span><br/> | <dl> <span data-ttu-id="e1cc4-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1cc4-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e1cc4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1cc4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1cc4-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="e1cc4-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="e1cc4-126">**ID3DXKeyframedAnimationSet:: Жетнумротатионкэйс**</span><span class="sxs-lookup"><span data-stu-id="e1cc4-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 
