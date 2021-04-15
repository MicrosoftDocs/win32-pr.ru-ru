---
description: Поворачивает вектор влево на заданное число 32-разрядных элементов.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Шаблон Ксмвекторротателефт (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648810"
---
# <a name="xmvectorrotateleft-template"></a><span data-ttu-id="981ac-103">Шаблон Ксмвекторротателефт</span><span class="sxs-lookup"><span data-stu-id="981ac-103">XMVectorRotateLeft template</span></span>

<span data-ttu-id="981ac-104">Поворачивает вектор влево на заданное число 32-разрядных элементов.</span><span class="sxs-lookup"><span data-stu-id="981ac-104">Rotates the vector left by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="981ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="981ac-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="981ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="981ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="981ac-107"><span id="V"></span><span id="v"></span>*3,3*</span><span class="sxs-lookup"><span data-stu-id="981ac-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="981ac-108">\[\]для поворота влево в векторе.</span><span class="sxs-lookup"><span data-stu-id="981ac-108">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="981ac-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="981ac-109">Return Value</span></span>

<span data-ttu-id="981ac-110">Возвращает повернутое [**ксмвектор**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="981ac-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="981ac-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="981ac-111">Remarks</span></span>

<span data-ttu-id="981ac-112">Эта функция является версией шаблона [**ксмвекторротателефт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) , в которой аргумент *Elements* является значением шаблона.</span><span class="sxs-lookup"><span data-stu-id="981ac-112">This function is a template version of [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="981ac-113">`XMVectorRotateLeft`Шаблон является новым для директксмас и недоступен для кснамас 2. x.</span><span class="sxs-lookup"><span data-stu-id="981ac-113">The `XMVectorRotateLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="981ac-114">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="981ac-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="981ac-115">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="981ac-115">Platform Requirements</span></span>

<span data-ttu-id="981ac-116">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="981ac-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="981ac-117">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="981ac-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="981ac-118">Требования</span><span class="sxs-lookup"><span data-stu-id="981ac-118">Requirements</span></span>



| <span data-ttu-id="981ac-119">Требование</span><span class="sxs-lookup"><span data-stu-id="981ac-119">Requirement</span></span> | <span data-ttu-id="981ac-120">Значение</span><span class="sxs-lookup"><span data-stu-id="981ac-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="981ac-121">Header</span><span class="sxs-lookup"><span data-stu-id="981ac-121">Header</span></span><br/> | <dl> <span data-ttu-id="981ac-122"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="981ac-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="981ac-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="981ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="981ac-124">Функции шаблона библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="981ac-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="981ac-125">**ксмвекторпермуте**</span><span class="sxs-lookup"><span data-stu-id="981ac-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="981ac-126">**ксмвекторротатеригхт**</span><span class="sxs-lookup"><span data-stu-id="981ac-126">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="981ac-127">**ксмвекторшифтлефт**</span><span class="sxs-lookup"><span data-stu-id="981ac-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
