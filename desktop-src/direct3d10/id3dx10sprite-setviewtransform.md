---
description: Задайте преобразование представления, которое применяется ко всем спрайтам.
ms.assetid: 0420b141-46c7-4409-a0c4-67d1e8e02cd4
title: 'Метод ID3DX10Sprite:: Сетвиевтрансформ (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62ec2129d441acaa0719d2e64c02b4cc57370c8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704031"
---
# <a name="id3dx10spritesetviewtransform-method"></a><span data-ttu-id="15a72-103">Метод ID3DX10Sprite:: Сетвиевтрансформ</span><span class="sxs-lookup"><span data-stu-id="15a72-103">ID3DX10Sprite::SetViewTransform method</span></span>

<span data-ttu-id="15a72-104">Задайте преобразование представления, которое применяется ко всем спрайтам.</span><span class="sxs-lookup"><span data-stu-id="15a72-104">Set the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a72-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15a72-105">Syntax</span></span>


```C++
HRESULT SetViewTransform(
  [in] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="15a72-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15a72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a72-107">*пвиевтрансформ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15a72-107">*pViewTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a72-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="15a72-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="15a72-109">Указатель на D3DXMATRIX, содержащий преобразование спрайта из исходного мира.</span><span class="sxs-lookup"><span data-stu-id="15a72-109">Pointer to a D3DXMATRIX that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="15a72-110">Используйте это преобразование для масштабирования, вращения или преобразования спрайта.</span><span class="sxs-lookup"><span data-stu-id="15a72-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a72-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15a72-111">Return value</span></span>

<span data-ttu-id="15a72-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15a72-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15a72-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="15a72-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="15a72-114">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="15a72-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="15a72-115">Требования</span><span class="sxs-lookup"><span data-stu-id="15a72-115">Requirements</span></span>



| <span data-ttu-id="15a72-116">Требование</span><span class="sxs-lookup"><span data-stu-id="15a72-116">Requirement</span></span> | <span data-ttu-id="15a72-117">Значение</span><span class="sxs-lookup"><span data-stu-id="15a72-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15a72-118">Header</span><span class="sxs-lookup"><span data-stu-id="15a72-118">Header</span></span><br/>  | <dl> <span data-ttu-id="15a72-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="15a72-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="15a72-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="15a72-120">Library</span></span><br/> | <dl> <span data-ttu-id="15a72-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15a72-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a72-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15a72-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a72-123">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="15a72-123">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="15a72-124">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="15a72-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
