---
description: Сдвигает вектор влево на заданное число 32-разрядных элементов, заполняя освобождаемые элементы элементами из второго вектора.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Шаблон Ксмвекторшифтлефт (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648806"
---
# <a name="xmvectorshiftleft-template"></a><span data-ttu-id="bc20c-103">Шаблон Ксмвекторшифтлефт</span><span class="sxs-lookup"><span data-stu-id="bc20c-103">XMVectorShiftLeft template</span></span>

<span data-ttu-id="bc20c-104">Сдвигает вектор влево на заданное число 32-разрядных элементов, заполняя освобождаемые элементы элементами из второго вектора.</span><span class="sxs-lookup"><span data-stu-id="bc20c-104">Shifts a vector left by a given number of 32-bit elements, filling the vacated elements with elements from a second vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc20c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc20c-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="bc20c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc20c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc20c-107"><span id="V1"></span><span id="v1"></span>*ADO.NET*</span><span class="sxs-lookup"><span data-stu-id="bc20c-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="bc20c-108">\[\]для сдвига влево в векторе.</span><span class="sxs-lookup"><span data-stu-id="bc20c-108">\[in\] Vector to shift left.</span></span>

</dd> <dt>

<span data-ttu-id="bc20c-109"><span id="V2"></span><span id="v2"></span>*Шаблон*</span><span class="sxs-lookup"><span data-stu-id="bc20c-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="bc20c-110">\[\]вектор, используемый для заполнения освобожденных компонентов v1 после сдвига влево.</span><span class="sxs-lookup"><span data-stu-id="bc20c-110">\[in\] Vector used to fill in the vacated components of V1 after it is shifted left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc20c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc20c-111">Return Value</span></span>

<span data-ttu-id="bc20c-112">Возвращает перемещенный и заполненный [**ксмвектор**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="bc20c-112">Returns the shifted and filled in [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bc20c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc20c-113">Remarks</span></span>

<span data-ttu-id="bc20c-114">Эта функция является версией шаблона [**ксмвекторшифтлефт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) , в которой аргумент *Elements* является значением шаблона.</span><span class="sxs-lookup"><span data-stu-id="bc20c-114">This function is a template version of [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="bc20c-115">`XMVectorShiftLeft`Шаблон является новым для директксмас и недоступен для кснамас 2. x.</span><span class="sxs-lookup"><span data-stu-id="bc20c-115">The `XMVectorShiftLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="bc20c-116">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="bc20c-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="bc20c-117">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="bc20c-117">Platform Requirements</span></span>

<span data-ttu-id="bc20c-118">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bc20c-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="bc20c-119">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="bc20c-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc20c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="bc20c-120">Requirements</span></span>



| <span data-ttu-id="bc20c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="bc20c-121">Requirement</span></span> | <span data-ttu-id="bc20c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="bc20c-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc20c-123">Header</span><span class="sxs-lookup"><span data-stu-id="bc20c-123">Header</span></span><br/> | <dl> <span data-ttu-id="bc20c-124"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc20c-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc20c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc20c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc20c-126">Функции шаблона библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="bc20c-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="bc20c-127">**ксмвекторпермуте**</span><span class="sxs-lookup"><span data-stu-id="bc20c-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="bc20c-128">**ксмвекторротателефт**</span><span class="sxs-lookup"><span data-stu-id="bc20c-128">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="bc20c-129">**ксмвекторротатеригхт**</span><span class="sxs-lookup"><span data-stu-id="bc20c-129">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> </dl>

 

 
