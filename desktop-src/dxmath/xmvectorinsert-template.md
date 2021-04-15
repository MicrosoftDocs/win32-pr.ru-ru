---
description: Поворачивает вектор влево на заданное число 32-разрядных компонентов и вставляет выбранные элементы этого результата в другой вектор.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Шаблон Ксмвекторинсерт (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648812"
---
# <a name="xmvectorinsert-template"></a><span data-ttu-id="2240b-103">Шаблон Ксмвекторинсерт</span><span class="sxs-lookup"><span data-stu-id="2240b-103">XMVectorInsert template</span></span>

<span data-ttu-id="2240b-104">Поворачивает вектор влево на заданное число 32-разрядных компонентов и вставляет выбранные элементы этого результата в другой вектор.</span><span class="sxs-lookup"><span data-stu-id="2240b-104">Rotates a vector left by a given number of 32-bit components and insert selected elements of that result into another vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="2240b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2240b-105">Syntax</span></span>

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a><span data-ttu-id="2240b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2240b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2240b-107"><span id="VD"></span><span id="vd"></span>*VD*</span><span class="sxs-lookup"><span data-stu-id="2240b-107"><span id="VD"></span><span id="vd"></span>*VD*</span></span>
</dt> <dd>

<span data-ttu-id="2240b-108">\[в \] vector для вставки в.</span><span class="sxs-lookup"><span data-stu-id="2240b-108">\[in\] Vector to insert into.</span></span>

</dd> <dt>

<span data-ttu-id="2240b-109"><span id="VS"></span><span id="vs"></span>*ЛИНЕЙЧАТ*</span><span class="sxs-lookup"><span data-stu-id="2240b-109"><span id="VS"></span><span id="vs"></span>*VS*</span></span>
</dt> <dd>

<span data-ttu-id="2240b-110">\[\]для поворота влево в векторе.</span><span class="sxs-lookup"><span data-stu-id="2240b-110">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2240b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2240b-111">Return Value</span></span>

<span data-ttu-id="2240b-112">Возвращает [**ксмвектор**](xmvector-data-type.md) , полученное в результате вращения и вставки.</span><span class="sxs-lookup"><span data-stu-id="2240b-112">Returns the [**XMVECTOR**](xmvector-data-type.md) that results from the rotation and insertion.</span></span>

## <a name="remarks"></a><span data-ttu-id="2240b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2240b-113">Remarks</span></span>

<span data-ttu-id="2240b-114">Эта функция является версией шаблона [**ксмвекторинсерт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) , в которой аргументы *SELECT \** являются значениями шаблона.</span><span class="sxs-lookup"><span data-stu-id="2240b-114">This function is a template version of [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) where the *Select\** arguments are template values.</span></span>

<span data-ttu-id="2240b-115">Для лучшей производительности результат `XMVectorInsert` должен быть назначен обратно в *VD*.</span><span class="sxs-lookup"><span data-stu-id="2240b-115">For best performance, the result of `XMVectorInsert` should be assigned back to *VD*.</span></span>

> [!Note]  
> <span data-ttu-id="2240b-116">`XMVectorInsert`Шаблон является новым для директксмас и недоступен для кснамас 2. x.</span><span class="sxs-lookup"><span data-stu-id="2240b-116">The `XMVectorInsert` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="2240b-117">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="2240b-117">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="2240b-118">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="2240b-118">Platform Requirements</span></span>

<span data-ttu-id="2240b-119">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2240b-119">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="2240b-120">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="2240b-120">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="2240b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2240b-121">Requirements</span></span>



| <span data-ttu-id="2240b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2240b-122">Requirement</span></span> | <span data-ttu-id="2240b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2240b-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2240b-124">Header</span><span class="sxs-lookup"><span data-stu-id="2240b-124">Header</span></span><br/> | <dl> <span data-ttu-id="2240b-125"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="2240b-125"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2240b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2240b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2240b-127">Функции шаблона библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="2240b-127">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="2240b-128">**ксмвекторпермуте**</span><span class="sxs-lookup"><span data-stu-id="2240b-128">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="2240b-129">**ксмвекторротателефт**</span><span class="sxs-lookup"><span data-stu-id="2240b-129">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="2240b-130">**ксмвекторротатеригхт**</span><span class="sxs-lookup"><span data-stu-id="2240b-130">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="2240b-131">**ксмвекторшифтлефт**</span><span class="sxs-lookup"><span data-stu-id="2240b-131">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
