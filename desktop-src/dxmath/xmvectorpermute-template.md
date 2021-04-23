---
description: Пермутес компоненты двух векторов для создания нового вектора.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Шаблон Ксмвекторпермуте (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649094"
---
# <a name="xmvectorpermute-template"></a><span data-ttu-id="149c1-103">Шаблон Ксмвекторпермуте</span><span class="sxs-lookup"><span data-stu-id="149c1-103">XMVectorPermute template</span></span>

<span data-ttu-id="149c1-104">Пермутес компоненты двух векторов для создания нового вектора.</span><span class="sxs-lookup"><span data-stu-id="149c1-104">Permutes the components of two vectors to create a new vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="149c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="149c1-105">Syntax</span></span>

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="149c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="149c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="149c1-107"><span id="V1"></span><span id="v1"></span>*ADO.NET*</span><span class="sxs-lookup"><span data-stu-id="149c1-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="149c1-108">\[в \] первом векторе.</span><span class="sxs-lookup"><span data-stu-id="149c1-108">\[in\] First vector.</span></span>

</dd> <dt>

<span data-ttu-id="149c1-109"><span id="V2"></span><span id="v2"></span>*Шаблон*</span><span class="sxs-lookup"><span data-stu-id="149c1-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="149c1-110">\[во \] втором векторе.</span><span class="sxs-lookup"><span data-stu-id="149c1-110">\[in\] Second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="149c1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="149c1-111">Return Value</span></span>

<span data-ttu-id="149c1-112">Возвращает вектор переставляются, который привел к объединению исходных векторов.</span><span class="sxs-lookup"><span data-stu-id="149c1-112">Returns the permuted vector that resulted from combining the source vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="149c1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="149c1-113">Remarks</span></span>

<span data-ttu-id="149c1-114">Если все 4 индекса ссылаются только на один вектор (т. е. все они находятся в диапазоне 0-3 или все в диапазоне 4-7), используйте [**ксмвекторсвиззле**](xmvectorswizzle-template.md) вместо этого для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="149c1-114">If all 4 indices reference only a single vector (i.e. they are all in the range 0-3 or all in the range 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) instead for better performance.</span></span>

<span data-ttu-id="149c1-115">Обратите внимание, что библиотека использует специализации шаблонов на некоторых платформах для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="149c1-115">Note the library makes use of template specializations on some platforms to improve performance.</span></span> <span data-ttu-id="149c1-116">Не все возможные зеркальные варианты реализованы в этих особых случаях, поэтому предпочтительнее пермутес, где элемент X результирующего вектора берется из параметра v1, а не параметра v2.</span><span class="sxs-lookup"><span data-stu-id="149c1-116">Not every possible mirror case is implemented for these special cases, so prefer permutes where the X element of the resulting vector comes from the V1 parameter rather than the V2 parameter.</span></span> <span data-ttu-id="149c1-117">Например, предпочтительно использовать `XMVectorPermute<0,1,4,5>(A,B);` для `XMVectorPermute(4,5,0,1)(B,A);` .</span><span class="sxs-lookup"><span data-stu-id="149c1-117">For example, prefer using `XMVectorPermute<0,1,4,5>(A,B);` to `XMVectorPermute(4,5,0,1)(B,A);`.</span></span>

<span data-ttu-id="149c1-118">Эта функция является версией шаблона [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) , где аргументы *переставляют \** являются значениями шаблона.</span><span class="sxs-lookup"><span data-stu-id="149c1-118">This function is a template version of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) where the *Permute\** arguments are template values.</span></span>

<span data-ttu-id="149c1-119">Константы [ \_ переставляют \_ XM](ovw-xnamath-reference-constants.md) предназначены для использования в качестве входных значений для *пермутекс*,*пермутэй*,*пермутез* и *пермутев*.</span><span class="sxs-lookup"><span data-stu-id="149c1-119">The [XM\_PERMUTE\_](ovw-xnamath-reference-constants.md) constants are provided to use as input values for *PermuteX*,*PermuteY*,*PermuteZ*, and *PermuteW*.</span></span>

> [!Note]  
> <span data-ttu-id="149c1-120">`XMVectorPermute`Шаблон является новым для директксмас и недоступен для кснамас 2. x.</span><span class="sxs-lookup"><span data-stu-id="149c1-120">The `XMVectorPermute` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="149c1-121">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="149c1-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="149c1-122">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="149c1-122">Platform Requirements</span></span>

<span data-ttu-id="149c1-123">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="149c1-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="149c1-124">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="149c1-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="149c1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="149c1-125">Requirements</span></span>



| <span data-ttu-id="149c1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="149c1-126">Requirement</span></span> | <span data-ttu-id="149c1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="149c1-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="149c1-128">Header</span><span class="sxs-lookup"><span data-stu-id="149c1-128">Header</span></span><br/> | <dl> <span data-ttu-id="149c1-129"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="149c1-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="149c1-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="149c1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="149c1-131">Функции шаблона библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="149c1-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="149c1-132">**ксмвекторсвиззле**</span><span class="sxs-lookup"><span data-stu-id="149c1-132">**XMVectorSwizzle**</span></span>](xmvectorswizzle-template.md)
</dt> </dl>

 

 
