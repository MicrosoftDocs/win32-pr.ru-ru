---
description: Переносимый тип, используемый для представления вектора 4 32-разрядных компонентов с плавающей запятой или целых чисел, каждый из которых оптимально соответствует и сопоставляется с регистром аппаратного вектора.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Тип данных КСМВЕКТОР (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704106"
---
# <a name="xmvector-data-type"></a><span data-ttu-id="92f9b-103">Тип данных КСМВЕКТОР</span><span class="sxs-lookup"><span data-stu-id="92f9b-103">XMVECTOR Data Type</span></span>

<span data-ttu-id="92f9b-104">Переносимый тип, используемый для представления вектора 4 32-разрядных компонентов с плавающей запятой или целых чисел, каждый из которых оптимально соответствует и сопоставляется с регистром аппаратного вектора.</span><span class="sxs-lookup"><span data-stu-id="92f9b-104">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span>

## <a name="remarks"></a><span data-ttu-id="92f9b-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92f9b-105">Remarks</span></span>

<span data-ttu-id="92f9b-106">Список дополнительных функций, таких как конструкторы и операторы, доступных `XMVECTOR` при использовании при программировании в C++, см. в разделе [расширения ксмвектор](ovw-xmvector-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="92f9b-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTOR` when programming in C++, see [XMVECTOR Extensions](ovw-xmvector-extensions.md).</span></span>

<span data-ttu-id="92f9b-107">В библиотеке Директксмас для полной поддержки переносимости и оптимизации `XMVECTOR` — это, по своей структуре, непрозрачный тип.</span><span class="sxs-lookup"><span data-stu-id="92f9b-107">In the DirectXMath Library, to fully support portability and optimization, `XMVECTOR` is, by design, an opaque type.</span></span> <span data-ttu-id="92f9b-108">Фактическая реализация `XMVECTOR` зависит от платформы.</span><span class="sxs-lookup"><span data-stu-id="92f9b-108">The actual implementation of `XMVECTOR` is platform dependent.</span></span>

<span data-ttu-id="92f9b-109">Как правило, код не должен полагаться на особенности любой конкретной реализации определенной платформы `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="92f9b-109">In general, code should not rely on the specifics of any given platform specific implementation of `XMVECTOR`.</span></span> <span data-ttu-id="92f9b-110">Реализации, зависящие от платформы, имеют следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="92f9b-110">Platform-specific implementations have these characteristics:</span></span>

-   <span data-ttu-id="92f9b-111">Они не являются переносимыми.</span><span class="sxs-lookup"><span data-stu-id="92f9b-111">They are not portable.</span></span>
-   <span data-ttu-id="92f9b-112">Они могут изменяться между выпусками.</span><span class="sxs-lookup"><span data-stu-id="92f9b-112">They may change between releases.</span></span>
-   <span data-ttu-id="92f9b-113">Неразумное использование сведений о реализации может быть неоптимальным.</span><span class="sxs-lookup"><span data-stu-id="92f9b-113">Injudicious use of implementation details may be suboptimal.</span></span>

<span data-ttu-id="92f9b-114">Разработчики должны использовать [методы доступа](ovw-xnamath-reference-functions-accessors.md), [загрузки](ovw-xnamath-reference-functions-load.md)и [хранения](ovw-xnamath-reference-functions-storage.md) библиотеки директксмас для получения и задания векторов, а также [функции векторных функций 4d библиотеки директксмас](ovw-xnamath-reference-functions-vector4.md) для управления ими.</span><span class="sxs-lookup"><span data-stu-id="92f9b-114">Developers should use DirectXMath Library's [accessor](ovw-xnamath-reference-functions-accessors.md), [load](ovw-xnamath-reference-functions-load.md), and [store](ovw-xnamath-reference-functions-storage.md) functions to get and set the vectors, and the [DirectXMath Library 4D Vector Functions](ovw-xnamath-reference-functions-vector4.md) to manipulate them.</span></span>

<span data-ttu-id="92f9b-115">Дополнительные сведения о проектах, требующих подробных сведений о реализации `XMVECTOR` на различных платформах, см. в разделе [Внутренняя библиотека](pg-xnamath-internals.md).</span><span class="sxs-lookup"><span data-stu-id="92f9b-115">For projects that need detailed information about how to implement `XMVECTOR` on different platforms, see [Library Internals](pg-xnamath-internals.md).</span></span>

### <a name="compiler-aliases"></a><span data-ttu-id="92f9b-116">Псевдонимы компилятора</span><span class="sxs-lookup"><span data-stu-id="92f9b-116">Compiler Aliases</span></span>

<span data-ttu-id="92f9b-117">Файл заголовка Директксмас. h использует Псевдонимы для `XMVECTOR` объекта, в частности **Кксмвектор** и **фксмвектор**.</span><span class="sxs-lookup"><span data-stu-id="92f9b-117">The DirectXMath.h header file uses aliases to the `XMVECTOR` object, specifically **CXMVECTOR** and **FXMVECTOR**.</span></span> <span data-ttu-id="92f9b-118">Заголовок использует эти псевдонимы для обеспечения соответствия оптимальным соглашениям о встроенном вызове различных компиляторов.</span><span class="sxs-lookup"><span data-stu-id="92f9b-118">The header uses these aliases to comply with the optimal in-line calling conventions of different compilers.</span></span> <span data-ttu-id="92f9b-119">Для большинства проектов, использующих Директксмас, достаточно обрабатывать эти типы как точный псевдоним для `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="92f9b-119">For most projects that use DirectXMath it is sufficient to treat these types as an exact alias to `XMVECTOR`.</span></span>

<span data-ttu-id="92f9b-120">Пример:</span><span class="sxs-lookup"><span data-stu-id="92f9b-120">For example:</span></span>


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



<span data-ttu-id="92f9b-121">Дополнительные сведения о проектах, для которых требуется подробная информация о том, как различные платформы обрабатывали свои соглашения о вызовах, см. в разделе [Внутренняя библиотека](pg-xnamath-internals.md)</span><span class="sxs-lookup"><span data-stu-id="92f9b-121">For projects that need detailed information about how different platforms handle their calling conventions, see [Library Internals](pg-xnamath-internals.md).</span></span>

<span data-ttu-id="92f9b-122">Для КСНАМАС 2. x `XMVECTOR` тип данных имеет элементы x, y,. z,. и. w, что обычно приводит к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="92f9b-122">For XNAMATH 2.x, the `XMVECTOR` data type has .x, .y, .z, .and .w element members, which generally cause poor performance.</span></span> <span data-ttu-id="92f9b-123">Использование \_ типа XM строгого \_ VECTOR4 предоставляет согласие на определение директксмас непрозрачного типа данных.</span><span class="sxs-lookup"><span data-stu-id="92f9b-123">The use of the XM\_STRICT\_VECTOR4 type provides an opt-in of the DirectXMath definition of an opaque data type.</span></span>

<span data-ttu-id="92f9b-124">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="92f9b-124">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="92f9b-125">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="92f9b-125">Platform Requirements</span></span>

<span data-ttu-id="92f9b-126">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="92f9b-126">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="92f9b-127">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="92f9b-127">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="92f9b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="92f9b-128">Requirements</span></span>



| <span data-ttu-id="92f9b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="92f9b-129">Requirement</span></span> | <span data-ttu-id="92f9b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="92f9b-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92f9b-131">Header</span><span class="sxs-lookup"><span data-stu-id="92f9b-131">Header</span></span><br/> | <dl> <span data-ttu-id="92f9b-132"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="92f9b-132"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92f9b-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92f9b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92f9b-134">Типы библиотек Директксмас</span><span class="sxs-lookup"><span data-stu-id="92f9b-134">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="92f9b-135">**Тип данных XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="92f9b-135">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="92f9b-136">**Тип данных XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="92f9b-136">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="92f9b-137">**Тип данных XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="92f9b-137">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="92f9b-138">**Тип данных XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="92f9b-138">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="92f9b-139">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="92f9b-139">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 




