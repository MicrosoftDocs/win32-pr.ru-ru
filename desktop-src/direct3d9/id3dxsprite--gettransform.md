---
description: Возвращает преобразование спрайта.
ms.assetid: d91f2776-ee87-42b3-998b-fccea178cee2
title: 'Метод ID3DXSprite:: Transform (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 646fa3574c3b9be788ad32ef402a7ca2051d04de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081884"
---
# <a name="id3dxspritegettransform-method"></a><span data-ttu-id="366c6-103">Метод ID3DXSprite:: Transform</span><span class="sxs-lookup"><span data-stu-id="366c6-103">ID3DXSprite::GetTransform method</span></span>

<span data-ttu-id="366c6-104">Возвращает преобразование спрайта.</span><span class="sxs-lookup"><span data-stu-id="366c6-104">Gets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="366c6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="366c6-105">Syntax</span></span>


```C++
HRESULT GetTransform(
  [in] D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="366c6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="366c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="366c6-107">*птрансформ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="366c6-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="366c6-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="366c6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="366c6-109">Указатель на [**D3DXMATRIX**](d3dxmatrix.md) , содержащий преобразование спрайта из исходного мира.</span><span class="sxs-lookup"><span data-stu-id="366c6-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="366c6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="366c6-110">Return value</span></span>

<span data-ttu-id="366c6-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="366c6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="366c6-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="366c6-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="366c6-113">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="366c6-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="366c6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="366c6-114">Requirements</span></span>



| <span data-ttu-id="366c6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="366c6-115">Requirement</span></span> | <span data-ttu-id="366c6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="366c6-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="366c6-117">Header</span><span class="sxs-lookup"><span data-stu-id="366c6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="366c6-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="366c6-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="366c6-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="366c6-119">Library</span></span><br/> | <dl> <span data-ttu-id="366c6-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="366c6-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="366c6-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="366c6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="366c6-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="366c6-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




