---
description: Заполняет массив данными ключа обратного вызова, используемым для анимации ключевых кадров.
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
ms.openlocfilehash: d3f8dbc771fcdde6d1c07a1bf810b322b0a70a30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273721"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="ab25e-103">Метод ID3DXKeyframedAnimationSet:: Жеткаллбакккэйс</span><span class="sxs-lookup"><span data-stu-id="ab25e-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="ab25e-104">Заполняет массив данными ключа обратного вызова, используемым для анимации ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="ab25e-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab25e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab25e-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="ab25e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab25e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab25e-107">*пкаллбакккэйс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ab25e-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab25e-108">Тип: **[ **\_ обратный вызов LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="ab25e-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="ab25e-109">Указатель на выделенный пользователем массив структур [**\_ обратного вызова D3DXKEY**](d3dxkey-callback.md) , который метод должен заполнить данными обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ab25e-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab25e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab25e-110">Return value</span></span>

<span data-ttu-id="ab25e-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab25e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab25e-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ab25e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ab25e-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ab25e-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab25e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ab25e-114">Requirements</span></span>



| <span data-ttu-id="ab25e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ab25e-115">Requirement</span></span> | <span data-ttu-id="ab25e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ab25e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab25e-117">Header</span><span class="sxs-lookup"><span data-stu-id="ab25e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ab25e-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab25e-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ab25e-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ab25e-119">Library</span></span><br/> | <dl> <span data-ttu-id="ab25e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab25e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab25e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab25e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab25e-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="ab25e-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="ab25e-123">**ID3DXKeyframedAnimationSet:: Жетнумкаллбакккэйс**</span><span class="sxs-lookup"><span data-stu-id="ab25e-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




