---
description: В этом обзоре описываются изменения, необходимые для переноса существующего кода с помощью библиотеки XNA Math в библиотеку Директксмас.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Перенос кода из библиотеки XNA Math
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc7a48d30711a870c28b677e458a4f72c3b3c40
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549966"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="b35f3-103">Перенос кода из библиотеки XNA Math</span><span class="sxs-lookup"><span data-stu-id="b35f3-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="b35f3-104">В этом обзоре описываются изменения, необходимые для переноса существующего кода с помощью библиотеки XNA Math в библиотеку Директксмас.</span><span class="sxs-lookup"><span data-stu-id="b35f3-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

## <a name="header-changes"></a><span data-ttu-id="b35f3-105">Изменения заголовка</span><span class="sxs-lookup"><span data-stu-id="b35f3-105">Header Changes</span></span>

<span data-ttu-id="b35f3-106">Библиотека Директксмас использует новый набор заголовков.</span><span class="sxs-lookup"><span data-stu-id="b35f3-106">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="b35f3-107">Замените `xnamath.h` заголовок на `DirectXMath.h` и добавьте `DirectXPackedVector.h` для *упакованных типов GPU* .</span><span class="sxs-lookup"><span data-stu-id="b35f3-107">Replace the `xnamath.h` header with `DirectXMath.h`, and add `DirectXPackedVector.h` for the *GPU packed* types.</span></span>

<span data-ttu-id="b35f3-108">Ограничивающие типы из примера конфликта DirectX SDK в `xnacollision.h` теперь входят в библиотеку директксмас в `DirectXCollision.h` .</span><span class="sxs-lookup"><span data-stu-id="b35f3-108">The bounding types from the DirectX SDK Collision sample in `xnacollision.h` is now part of the DirectXMath library in `DirectXCollision.h`.</span></span> <span data-ttu-id="b35f3-109">Они были изменены для использования классов C++, а не API-интерфейсов в стиле языка C.</span><span class="sxs-lookup"><span data-stu-id="b35f3-109">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="b35f3-110">Постоянные изменения</span><span class="sxs-lookup"><span data-stu-id="b35f3-110">Constant Changes</span></span>

<span data-ttu-id="b35f3-111">\_Версия кснамас (200, 201, 202, 203, 204 и т. д.) заменена диреккстмас \_ версией (300, 301, 302, 303 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b35f3-111">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!NOTE]  
> <span data-ttu-id="b35f3-112">Директксмас 3,00 и 3,02 поставляются с предварительными версиями Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b35f3-112">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="b35f3-113">Директксмас 3,03 в финальной версии пакета SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b35f3-113">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

## <a name="namespaces"></a><span data-ttu-id="b35f3-114">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="b35f3-114">Namespaces</span></span>

<span data-ttu-id="b35f3-115">Библиотека Директксмас использует пространства имен C++ для организации типов.</span><span class="sxs-lookup"><span data-stu-id="b35f3-115">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="b35f3-116">XNA Math использовал только глобальное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="b35f3-116">XNA Math used only the global namespace.</span></span> <span data-ttu-id="b35f3-117">Типы Директксмас, общие с XNA Math, находятся в **DirectX** или в пространстве имен **DirectX::P аккедвектор** .</span><span class="sxs-lookup"><span data-stu-id="b35f3-117">The DirectXMath types in common with XNA Math are in the **DirectX** or the **DirectX::PackedVector** namespace.</span></span>

<span data-ttu-id="b35f3-118">В исходных файлах C++ простое решение заключается в добавлении `using` инструкций.</span><span class="sxs-lookup"><span data-stu-id="b35f3-118">In C++ source files, a simple solution is to add `using` statements.</span></span>

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

<span data-ttu-id="b35f3-119">Для заголовков не рекомендуется добавлять операторы using.</span><span class="sxs-lookup"><span data-stu-id="b35f3-119">For headers, it is not considered best practice to add using statements.</span></span> <span data-ttu-id="b35f3-120">Вместо этого добавьте полные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="b35f3-120">Instead, add fully-qualified namespaces.</span></span>

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a><span data-ttu-id="b35f3-121">Частичные загрузки</span><span class="sxs-lookup"><span data-stu-id="b35f3-121">Partial Loads</span></span>

<span data-ttu-id="b35f3-122">Для различных функций, которые загружают менее 4 элементов КСМВЕКТОР, в библиотеке XNA Math не определены дополнительные элементы.</span><span class="sxs-lookup"><span data-stu-id="b35f3-122">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="b35f3-123">Директксмас всегда будет заполнять эти дополнительные элементы 0.</span><span class="sxs-lookup"><span data-stu-id="b35f3-123">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="b35f3-124">Удаление специальных типов для Xbox 360</span><span class="sxs-lookup"><span data-stu-id="b35f3-124">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="b35f3-125">Следующие типы, функции и константы XNA Math Library недоступны в Директксмас.</span><span class="sxs-lookup"><span data-stu-id="b35f3-125">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="b35f3-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="b35f3-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="b35f3-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="b35f3-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="b35f3-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="b35f3-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="b35f3-129">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ ксмадддхен, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="b35f3-129">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="b35f3-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="b35f3-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="b35f3-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="b35f3-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="b35f3-132">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="b35f3-132">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="b35f3-133">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="b35f3-133">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="b35f3-134">\_\_vector4i является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="b35f3-134">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="b35f3-135">Вместо этого используйте [**XMVECTORI32**](xmvectori32-data-type.md) или [**XMVECTORU32**](xmvectoru32-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="b35f3-135">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="b35f3-136">Следующие функции и типы являются устаревшими, так как они являются только Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="b35f3-136">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="b35f3-137">Встроенные функции ARM-NEON</span><span class="sxs-lookup"><span data-stu-id="b35f3-137">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="b35f3-138">Объявление векторной константы с этим кодом будет компилироваться для XNA Math для SSE и без встроенных функций, но не будет выполняться для Директксмас с помощью ARM-NEON.</span><span class="sxs-lookup"><span data-stu-id="b35f3-138">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

<span data-ttu-id="b35f3-139">Как правило, не рекомендуется использовать этот метод инициализации [**ксмвектор**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="b35f3-139">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="b35f3-140">Однако, если требуется константа Vector, класс [**XMVECTORF32**](xmvectorf32-data-type.md) поддерживает этот стиль инициализации и возвращает тип **ксмвектор** автоматически, чтобы можно было использовать **XMVECTORF32** в большинстве тех же контекстов.</span><span class="sxs-lookup"><span data-stu-id="b35f3-140">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="b35f3-141">Для выполнения любых операций записи в класс **XMVECTORF32** требуется явная ссылка на элемент **ксмвектор** . v.</span><span class="sxs-lookup"><span data-stu-id="b35f3-141">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="b35f3-142">Переставляют</span><span class="sxs-lookup"><span data-stu-id="b35f3-142">Permute</span></span>

<span data-ttu-id="b35f3-143">Библиотека XNA Math имела следующую форму для общих векторных переставляют:</span><span class="sxs-lookup"><span data-stu-id="b35f3-143">The XNA Math library had the following form for general vector permute:</span></span>

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

<span data-ttu-id="b35f3-144">Для Директксмас было устранено **ксмвекторпермутеконтрол** , а XM \_ переставляют \_ 0x.</span><span class="sxs-lookup"><span data-stu-id="b35f3-144">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="b35f3-145">\_ \_ Константы 1Z переставляют XM были переопределены, чтобы они были простыми индексами 0-7.</span><span class="sxs-lookup"><span data-stu-id="b35f3-145">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="b35f3-146">Вот новая сигнатура для [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span><span class="sxs-lookup"><span data-stu-id="b35f3-146">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

<span data-ttu-id="b35f3-147">Вместо управляющего слова эта функция непосредственно принимает 4 индекса в качестве параметров, что также делает ее аналогом функции [**ксмвекторсвиззле**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) , используя новый XM \_ свиззле \_ X.</span><span class="sxs-lookup"><span data-stu-id="b35f3-147">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="b35f3-148">\_ \_ Константы XM свиззле W определены как простые индексы 0-3.</span><span class="sxs-lookup"><span data-stu-id="b35f3-148">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> <span data-ttu-id="b35f3-149">Для постоянных значений существует гораздо более эффективный способ реализации переставляют.</span><span class="sxs-lookup"><span data-stu-id="b35f3-149">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="b35f3-150">Вместо использования формы функции [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)используйте форму **шаблона** :</span><span class="sxs-lookup"><span data-stu-id="b35f3-150">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a><span data-ttu-id="b35f3-151">Формы шаблонов</span><span class="sxs-lookup"><span data-stu-id="b35f3-151">Template Forms</span></span>

<span data-ttu-id="b35f3-152">Как правило, использование формы шаблона в форме функции следующих функций значительно более эффективно и позволяет библиотеке выполнять оптимизацию для конкретной платформы с помощью специализации шаблонов.</span><span class="sxs-lookup"><span data-stu-id="b35f3-152">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateLeft(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateRight(FXMVECTOR V)

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
```

## <a name="eliminated-functions"></a><span data-ttu-id="b35f3-153">Исключенные функции</span><span class="sxs-lookup"><span data-stu-id="b35f3-153">Eliminated Functions</span></span>

| <span data-ttu-id="b35f3-154">Функция исключена</span><span class="sxs-lookup"><span data-stu-id="b35f3-154">Eliminated Function</span></span>        | <span data-ttu-id="b35f3-155">Замена</span><span class="sxs-lookup"><span data-stu-id="b35f3-155">Replacement</span></span>                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35f3-156">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="b35f3-156">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="b35f3-157">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="b35f3-157">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| <span data-ttu-id="b35f3-158">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="b35f3-158">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="b35f3-159">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="b35f3-159">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| <span data-ttu-id="b35f3-160">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="b35f3-160">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="b35f3-161">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="b35f3-161">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| <span data-ttu-id="b35f3-162">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="b35f3-162">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="b35f3-163">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="b35f3-163">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| <span data-ttu-id="b35f3-164">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="b35f3-164">XMStoreInt4NC</span></span>              | [<span data-ttu-id="b35f3-165">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="b35f3-165">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| <span data-ttu-id="b35f3-166">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="b35f3-166">XMVector2InBoundsR</span></span>         | <span data-ttu-id="b35f3-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="b35f3-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="b35f3-168">[XM \_ КРМАСК \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="b35f3-168">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="b35f3-169">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="b35f3-169">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="b35f3-170">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="b35f3-170">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| <span data-ttu-id="b35f3-171">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="b35f3-171">XMVector3InBoundsR</span></span>         | <span data-ttu-id="b35f3-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="b35f3-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="b35f3-173">[XM \_ КРМАСК \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="b35f3-173">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="b35f3-174">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="b35f3-174">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="b35f3-175">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="b35f3-175">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| <span data-ttu-id="b35f3-176">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="b35f3-176">XMVector4InBoundsR</span></span>         | <span data-ttu-id="b35f3-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="b35f3-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="b35f3-178">[XM \_ КРМАСК \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="b35f3-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="b35f3-179">ксмвекторкошест</span><span class="sxs-lookup"><span data-stu-id="b35f3-179">XMVectorCosHEst</span></span>            | [<span data-ttu-id="b35f3-180">**ксмвекторкош**</span><span class="sxs-lookup"><span data-stu-id="b35f3-180">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| <span data-ttu-id="b35f3-181">ксмвекторекспест</span><span class="sxs-lookup"><span data-stu-id="b35f3-181">XMVectorExpEst</span></span>             | [<span data-ttu-id="b35f3-182">**ксмвекторексп**</span><span class="sxs-lookup"><span data-stu-id="b35f3-182">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| <span data-ttu-id="b35f3-183">ксмвекторложест</span><span class="sxs-lookup"><span data-stu-id="b35f3-183">XMVectorLogEst</span></span>             | [<span data-ttu-id="b35f3-184">**ксмвекторлог**</span><span class="sxs-lookup"><span data-stu-id="b35f3-184">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| <span data-ttu-id="b35f3-185">ксмвекторповест</span><span class="sxs-lookup"><span data-stu-id="b35f3-185">XMVectorPowEst</span></span>             | [<span data-ttu-id="b35f3-186">**ксмвекторпов**</span><span class="sxs-lookup"><span data-stu-id="b35f3-186">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| <span data-ttu-id="b35f3-187">ксмвекторсинхест</span><span class="sxs-lookup"><span data-stu-id="b35f3-187">XMVectorSinHEst</span></span>            | [<span data-ttu-id="b35f3-188">**ксмвекторсинх**</span><span class="sxs-lookup"><span data-stu-id="b35f3-188">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| <span data-ttu-id="b35f3-189">ксмвектортанхест</span><span class="sxs-lookup"><span data-stu-id="b35f3-189">XMVectorTanHEst</span></span>            | [<span data-ttu-id="b35f3-190">**ксмвектортанх**</span><span class="sxs-lookup"><span data-stu-id="b35f3-190">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a><span data-ttu-id="b35f3-191">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b35f3-191">Related topics</span></span>

[<span data-ttu-id="b35f3-192">Директксмас по программированию</span><span class="sxs-lookup"><span data-stu-id="b35f3-192">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
