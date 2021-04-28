---
description: 'Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэйс — заполняет массив данными ключа обратного вызова, используемыми для анимации ключевых кадров.'
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f3bdb7049de3b5d6aad10b5ff5100d01d05e3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093722"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="5f855-103">Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэйс</span><span class="sxs-lookup"><span data-stu-id="5f855-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="5f855-104">Заполняет массив данными ключа обратного вызова, используемым для анимации ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="5f855-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f855-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f855-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="5f855-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f855-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f855-107">*пкаллбакккэйс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5f855-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f855-108">Тип: **[ **\_ обратный вызов LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="5f855-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="5f855-109">Указатель на выделенный пользователем массив структур [**\_ обратного вызова D3DXKEY**](d3dxkey-callback.md) , который метод должен заполнить данными обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="5f855-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f855-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f855-110">Return value</span></span>

<span data-ttu-id="5f855-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5f855-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5f855-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="5f855-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5f855-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="5f855-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f855-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5f855-114">Requirements</span></span>



| <span data-ttu-id="5f855-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5f855-115">Requirement</span></span> | <span data-ttu-id="5f855-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5f855-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f855-117">Header</span><span class="sxs-lookup"><span data-stu-id="5f855-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5f855-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f855-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5f855-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5f855-119">Library</span></span><br/> | <dl> <span data-ttu-id="5f855-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f855-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f855-121">См. также</span><span class="sxs-lookup"><span data-stu-id="5f855-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f855-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5f855-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="5f855-123">**ID3DXKeyframedAnimationSet:: Жетнумкаллбакккэйс**</span><span class="sxs-lookup"><span data-stu-id="5f855-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




