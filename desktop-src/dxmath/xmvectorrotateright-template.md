---
description: Поворачивает вектор вправо на заданное число 32-разрядных элементов.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Шаблон Ксмвекторротатеригхт (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2c4e623a75015e8051a5a9ccf32f4715016b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649093"
---
# <a name="xmvectorrotateright-template"></a><span data-ttu-id="d124d-103">Шаблон Ксмвекторротатеригхт</span><span class="sxs-lookup"><span data-stu-id="d124d-103">XMVectorRotateRight template</span></span>

<span data-ttu-id="d124d-104">Поворачивает вектор вправо на заданное число 32-разрядных элементов.</span><span class="sxs-lookup"><span data-stu-id="d124d-104">Rotates the vector right by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="d124d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d124d-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="d124d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d124d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d124d-107"><span id="V"></span><span id="v"></span>*3,3*</span><span class="sxs-lookup"><span data-stu-id="d124d-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="d124d-108">\[\]для поворота в векторе вправо.</span><span class="sxs-lookup"><span data-stu-id="d124d-108">\[in\] Vector to rotate right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d124d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d124d-109">Return Value</span></span>

<span data-ttu-id="d124d-110">Возвращает повернутое [**ксмвектор**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d124d-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d124d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d124d-111">Remarks</span></span>

<span data-ttu-id="d124d-112">Эта функция является версией шаблона [**ксмвекторротатеригхт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) , в которой аргумент *Elements* является значением шаблона.</span><span class="sxs-lookup"><span data-stu-id="d124d-112">This function is a template version of [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="d124d-113">`XMVectorRotateRight`Шаблон является новым для директксмас и недоступен для кснамас 2. x.</span><span class="sxs-lookup"><span data-stu-id="d124d-113">The `XMVectorRotateRight` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="d124d-114">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="d124d-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="d124d-115">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="d124d-115">Platform Requirements</span></span>

<span data-ttu-id="d124d-116">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d124d-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="d124d-117">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="d124d-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="d124d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d124d-118">Requirements</span></span>



| <span data-ttu-id="d124d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d124d-119">Requirement</span></span> | <span data-ttu-id="d124d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d124d-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d124d-121">Header</span><span class="sxs-lookup"><span data-stu-id="d124d-121">Header</span></span><br/> | <dl> <span data-ttu-id="d124d-122"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="d124d-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d124d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d124d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d124d-124">Функции шаблона библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="d124d-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="d124d-125">**ксмвекторпермуте**</span><span class="sxs-lookup"><span data-stu-id="d124d-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="d124d-126">**ксмвекторротателефт**</span><span class="sxs-lookup"><span data-stu-id="d124d-126">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="d124d-127">**ксмвекторшифтлефт**</span><span class="sxs-lookup"><span data-stu-id="d124d-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
