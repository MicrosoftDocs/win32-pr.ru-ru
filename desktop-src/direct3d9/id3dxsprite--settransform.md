---
description: Задает преобразование спрайта.
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: 'Метод ID3DXSprite:: Сеттрансформ (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 316e7e2c68dfa8f25a712c2077ece03d09455050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273841"
---
# <a name="id3dxspritesettransform-method"></a><span data-ttu-id="2caab-103">Метод ID3DXSprite:: Сеттрансформ</span><span class="sxs-lookup"><span data-stu-id="2caab-103">ID3DXSprite::SetTransform method</span></span>

<span data-ttu-id="2caab-104">Задает преобразование спрайта.</span><span class="sxs-lookup"><span data-stu-id="2caab-104">Sets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="2caab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2caab-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="2caab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2caab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2caab-107">*птрансформ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2caab-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2caab-108">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2caab-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2caab-109">Указатель на [**D3DXMATRIX**](d3dxmatrix.md) , содержащий преобразование спрайта из исходного мира.</span><span class="sxs-lookup"><span data-stu-id="2caab-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="2caab-110">Используйте это преобразование для масштабирования, вращения или преобразования спрайта.</span><span class="sxs-lookup"><span data-stu-id="2caab-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2caab-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2caab-111">Return value</span></span>

<span data-ttu-id="2caab-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2caab-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2caab-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="2caab-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2caab-114">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="2caab-114">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="2caab-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2caab-115">Requirements</span></span>



| <span data-ttu-id="2caab-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2caab-116">Requirement</span></span> | <span data-ttu-id="2caab-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2caab-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2caab-118">Header</span><span class="sxs-lookup"><span data-stu-id="2caab-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2caab-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="2caab-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="2caab-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2caab-120">Library</span></span><br/> | <dl> <span data-ttu-id="2caab-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2caab-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2caab-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2caab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2caab-123">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="2caab-123">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="2caab-124">Преобразования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2caab-124">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




