---
description: Свиззлес вектор.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Шаблон Ксмвекторсвиззле (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708590"
---
# <a name="xmvectorswizzle-template"></a><span data-ttu-id="204f5-103">Шаблон Ксмвекторсвиззле</span><span class="sxs-lookup"><span data-stu-id="204f5-103">XMVectorSwizzle template</span></span>

<span data-ttu-id="204f5-104">Свиззлес вектор.</span><span class="sxs-lookup"><span data-stu-id="204f5-104">Swizzles a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="204f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="204f5-105">Syntax</span></span>

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="204f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="204f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="204f5-107"><span id="V"></span><span id="v"></span>*3,3*</span><span class="sxs-lookup"><span data-stu-id="204f5-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="204f5-108">\[в \] vector to свиззле.</span><span class="sxs-lookup"><span data-stu-id="204f5-108">\[in\] Vector to swizzle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="204f5-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="204f5-109">Return Value</span></span>

<span data-ttu-id="204f5-110">Возвращает свиззлед [**ксмвектор**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="204f5-110">Returns the swizzled [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="204f5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="204f5-111">Remarks</span></span>

<span data-ttu-id="204f5-112">Эта функция является версией шаблона [**ксмвекторсвиззле**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) , где аргументы *свиззле \** являются значениями шаблона.</span><span class="sxs-lookup"><span data-stu-id="204f5-112">This function is a template version of [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) where the *Swizzle\** arguments are template values.</span></span>

<span data-ttu-id="204f5-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` и `XM_SWIZZLE_W` — константы, которые возвращают 0, 1, 2 и 3 соответственно для использования с `XMVectorSwizzle` .</span><span class="sxs-lookup"><span data-stu-id="204f5-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y`, `XM_SWIZZLE_Z`, and `XM_SWIZZLE_W` are constants which evaluate to 0, 1, 2, and 3 respectively for use with `XMVectorSwizzle`.</span></span> <span data-ttu-id="204f5-114">Это идентично `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , `XM_PERMUTE_0Z` и `XM_PERMUTE_0W` .</span><span class="sxs-lookup"><span data-stu-id="204f5-114">This is identical to `XM_PERMUTE_0X`, `XM_PERMUTE_0Y`, `XM_PERMUTE_0Z`, and `XM_PERMUTE_0W`.</span></span>

> [!Note]  
> <span data-ttu-id="204f5-115">`XMVectorSwizzle`Шаблон является новым для директксмас и недоступен для кснамас 2. x.</span><span class="sxs-lookup"><span data-stu-id="204f5-115">The `XMVectorSwizzle` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="204f5-116">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="204f5-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="204f5-117">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="204f5-117">Platform Requirements</span></span>

<span data-ttu-id="204f5-118">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="204f5-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="204f5-119">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="204f5-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="204f5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="204f5-120">Requirements</span></span>



| <span data-ttu-id="204f5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="204f5-121">Requirement</span></span> | <span data-ttu-id="204f5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="204f5-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="204f5-123">Header</span><span class="sxs-lookup"><span data-stu-id="204f5-123">Header</span></span><br/> | <dl> <span data-ttu-id="204f5-124"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="204f5-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="204f5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="204f5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="204f5-126">Функции шаблона библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="204f5-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="204f5-127">**ксмвекторпермуте**</span><span class="sxs-lookup"><span data-stu-id="204f5-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> </dl>

 

 
