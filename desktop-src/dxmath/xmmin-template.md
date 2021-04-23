---
description: Сравнивает два экземпляра типа числовых данных или два экземпляра объекта, которые поддерживают перегрузку <, и возвращает меньше одного из двух экземпляров. Тип данных аргументов и возвращаемое значение одинаковы.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Шаблон Ксммин (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550fd93c9776ad8547502b50817446e64f9bdd64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704051"
---
# <a name="xmmin-template"></a><span data-ttu-id="1baa9-104">Шаблон Ксммин</span><span class="sxs-lookup"><span data-stu-id="1baa9-104">XMMin template</span></span>

<span data-ttu-id="1baa9-105">Сравнивает два экземпляра типа числовых данных или два экземпляра объекта, которые поддерживают перегрузку <, и возвращает меньше одного из двух экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1baa9-105">Compares two numeric data type instances, or two instances of an object which supports an overload of <, and returns the smaller one of the two instances.</span></span> <span data-ttu-id="1baa9-106">Тип данных аргументов и возвращаемое значение одинаковы.</span><span class="sxs-lookup"><span data-stu-id="1baa9-106">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="1baa9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1baa9-107">Syntax</span></span>

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a><span data-ttu-id="1baa9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1baa9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1baa9-109"><span id="a"></span><span id="A"></span>*конкретного*</span><span class="sxs-lookup"><span data-stu-id="1baa9-109"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="1baa9-110">\[в \] задает первый из двух объектов.</span><span class="sxs-lookup"><span data-stu-id="1baa9-110">\[in\] Specifies the first of two objects.</span></span>

</dd> <dt>

<span data-ttu-id="1baa9-111"><span id="b"></span><span id="B"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="1baa9-111"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="1baa9-112">\[в \] задает два из двух объектов.</span><span class="sxs-lookup"><span data-stu-id="1baa9-112">\[in\] Specifies the two of two objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1baa9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1baa9-113">Return Value</span></span>

<span data-ttu-id="1baa9-114">Возвращает меньшее из двух входных объектов.</span><span class="sxs-lookup"><span data-stu-id="1baa9-114">Returns the smaller of the two input objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="1baa9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1baa9-115">Remarks</span></span>

<span data-ttu-id="1baa9-116">`XMMin` является шаблоном, а тип T указывается при создании экземпляра шаблона.</span><span class="sxs-lookup"><span data-stu-id="1baa9-116">`XMMin` is a template and the T type is specified when the template is instantiated.</span></span>

> [!Note]  
> <span data-ttu-id="1baa9-117">`XMMin`Шаблон является новым для директксмас и недоступен для кснамас 2. x.</span><span class="sxs-lookup"><span data-stu-id="1baa9-117">The `XMMin` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span> <span data-ttu-id="1baa9-118">`XMMin` доступен в виде макроса в Кснамас 2. x.</span><span class="sxs-lookup"><span data-stu-id="1baa9-118">`XMMin` is available as a macro in XNAMath 2.x.</span></span>

 

> [!Note]  
> <span data-ttu-id="1baa9-119">В идеале используйте std:: min вместо `XMMin` .</span><span class="sxs-lookup"><span data-stu-id="1baa9-119">Ideally use std::min instead of `XMMin`.</span></span> <span data-ttu-id="1baa9-120">Чтобы избежать конфликтов с заголовками Windows с std:: min, необходимо \# определить номинмакс перед включением заголовков Windows.</span><span class="sxs-lookup"><span data-stu-id="1baa9-120">To avoid conflicts with Windows headers with std::min, you need to \#define NOMINMAX before you include Windows headers.</span></span>

 

<span data-ttu-id="1baa9-121">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="1baa9-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="1baa9-122">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="1baa9-122">Platform Requirements</span></span>

<span data-ttu-id="1baa9-123">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1baa9-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="1baa9-124">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="1baa9-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="1baa9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1baa9-125">Requirements</span></span>



| <span data-ttu-id="1baa9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1baa9-126">Requirement</span></span> | <span data-ttu-id="1baa9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1baa9-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1baa9-128">Header</span><span class="sxs-lookup"><span data-stu-id="1baa9-128">Header</span></span><br/> | <dl> <span data-ttu-id="1baa9-129"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="1baa9-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1baa9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1baa9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1baa9-131">Функции шаблона библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="1baa9-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="1baa9-132">**ксммакс**</span><span class="sxs-lookup"><span data-stu-id="1baa9-132">**XMMax**</span></span>](xmmax-template.md)
</dt> </dl>

 

 




