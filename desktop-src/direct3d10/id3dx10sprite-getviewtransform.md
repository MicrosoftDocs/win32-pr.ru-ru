---
description: Получение преобразования представления, которое применяется ко всем спрайтам.
ms.assetid: eba45c08-64cc-4119-83d4-50351fe21bea
title: 'Метод ID3DX10Sprite:: Жетвиевтрансформ (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 699a46e48545d58058fb1f2db2955b4a4f403a53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714039"
---
# <a name="id3dx10spritegetviewtransform-method"></a><span data-ttu-id="59b3b-103">Метод ID3DX10Sprite:: Жетвиевтрансформ</span><span class="sxs-lookup"><span data-stu-id="59b3b-103">ID3DX10Sprite::GetViewTransform method</span></span>

<span data-ttu-id="59b3b-104">Получение преобразования представления, которое применяется ко всем спрайтам.</span><span class="sxs-lookup"><span data-stu-id="59b3b-104">Get the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b3b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59b3b-105">Syntax</span></span>


```C++
HRESULT GetViewTransform(
  [out] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="59b3b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59b3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b3b-107">*пвиевтрансформ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="59b3b-107">*pViewTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59b3b-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="59b3b-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="59b3b-109">Указатель на [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) , для которого будет задано преобразование спрайта из исходного мира.</span><span class="sxs-lookup"><span data-stu-id="59b3b-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b3b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59b3b-110">Return value</span></span>

<span data-ttu-id="59b3b-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59b3b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59b3b-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="59b3b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="59b3b-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="59b3b-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b3b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="59b3b-114">Requirements</span></span>



| <span data-ttu-id="59b3b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="59b3b-115">Requirement</span></span> | <span data-ttu-id="59b3b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="59b3b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59b3b-117">Header</span><span class="sxs-lookup"><span data-stu-id="59b3b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="59b3b-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="59b3b-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="59b3b-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59b3b-119">Library</span></span><br/> | <dl> <span data-ttu-id="59b3b-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59b3b-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b3b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59b3b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b3b-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="59b3b-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="59b3b-123">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="59b3b-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
