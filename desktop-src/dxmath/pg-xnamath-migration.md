---
description: В этом обзоре описываются изменения, необходимые для переноса существующего кода с помощью библиотеки XNA Math в библиотеку Директксмас.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Перенос кода из библиотеки XNA Math
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c446165d3d0b6b7303424959f96ddf48bc75b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544079"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="6fc15-103">Перенос кода из библиотеки XNA Math</span><span class="sxs-lookup"><span data-stu-id="6fc15-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="6fc15-104">В этом обзоре описываются изменения, необходимые для переноса существующего кода с помощью библиотеки XNA Math в библиотеку Директксмас.</span><span class="sxs-lookup"><span data-stu-id="6fc15-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

-   [<span data-ttu-id="6fc15-105">Изменения заголовка</span><span class="sxs-lookup"><span data-stu-id="6fc15-105">Header Changes</span></span>](#header-changes)
-   [<span data-ttu-id="6fc15-106">Постоянные изменения</span><span class="sxs-lookup"><span data-stu-id="6fc15-106">Constant Changes</span></span>](#constant-changes)
-   [<span data-ttu-id="6fc15-107">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="6fc15-107">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="6fc15-108">Частичные загрузки</span><span class="sxs-lookup"><span data-stu-id="6fc15-108">Partial Loads</span></span>](#partial-loads)
-   [<span data-ttu-id="6fc15-109">Удаление специальных типов для Xbox 360</span><span class="sxs-lookup"><span data-stu-id="6fc15-109">Removal of Xbox 360 Specific Types</span></span>](#removal-of-xbox-360-specific-types)
-   [<span data-ttu-id="6fc15-110">Встроенные функции ARM-NEON</span><span class="sxs-lookup"><span data-stu-id="6fc15-110">ARM-NEON Intrinsics</span></span>](#arm-neon-intrinsics)
-   [<span data-ttu-id="6fc15-111">Переставляют</span><span class="sxs-lookup"><span data-stu-id="6fc15-111">Permute</span></span>](#permute)
-   [<span data-ttu-id="6fc15-112">Формы шаблонов</span><span class="sxs-lookup"><span data-stu-id="6fc15-112">Template Forms</span></span>](#template-forms)
-   [<span data-ttu-id="6fc15-113">Исключенные функции</span><span class="sxs-lookup"><span data-stu-id="6fc15-113">Eliminated Functions</span></span>](#eliminated-functions)
-   [<span data-ttu-id="6fc15-114">См. также</span><span class="sxs-lookup"><span data-stu-id="6fc15-114">Related topics</span></span>](#related-topics)

## <a name="header-changes"></a><span data-ttu-id="6fc15-115">Изменения заголовка</span><span class="sxs-lookup"><span data-stu-id="6fc15-115">Header Changes</span></span>

<span data-ttu-id="6fc15-116">Библиотека Директксмас использует новый набор заголовков.</span><span class="sxs-lookup"><span data-stu-id="6fc15-116">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="6fc15-117">Замените заголовок кснамас. h на Директксмас. h и добавьте Директкспаккедвектор. h для типов "GPU Pack".</span><span class="sxs-lookup"><span data-stu-id="6fc15-117">Replace the xnamath.h header with DirectXMath.h and add DirectXPackedVector.h for the “GPU packed” types.</span></span>

<span data-ttu-id="6fc15-118">Ограничивающие типы из примера конфликта DirectX SDK в кснаколлисион. h теперь входят в библиотеку Директксмас в Директксколлисион. h.</span><span class="sxs-lookup"><span data-stu-id="6fc15-118">The bounding types from the DirectX SDK Collision sample in xnacollision.h is now part of the DirectXMath library in DirectXCollision.h.</span></span> <span data-ttu-id="6fc15-119">Они были изменены для использования классов C++, а не API-интерфейсов в стиле языка C.</span><span class="sxs-lookup"><span data-stu-id="6fc15-119">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="6fc15-120">Постоянные изменения</span><span class="sxs-lookup"><span data-stu-id="6fc15-120">Constant Changes</span></span>

<span data-ttu-id="6fc15-121">\_Версия кснамас (200, 201, 202, 203, 204 и т. д.) заменена диреккстмас \_ версией (300, 301, 302, 303 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="6fc15-121">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!Note]  
> <span data-ttu-id="6fc15-122">Директксмас 3,00 и 3,02 поставляются с предварительными версиями Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6fc15-122">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="6fc15-123">Директксмас 3,03 в финальной версии пакета SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6fc15-123">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

 

## <a name="namespaces"></a><span data-ttu-id="6fc15-124">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="6fc15-124">Namespaces</span></span>

<span data-ttu-id="6fc15-125">Библиотека Директксмас использует пространства имен C++ для организации типов.</span><span class="sxs-lookup"><span data-stu-id="6fc15-125">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="6fc15-126">XNA Math использовал только глобальное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="6fc15-126">XNA Math used only the global namespace.</span></span> <span data-ttu-id="6fc15-127">Типы Директксмас, общие с XNA Math, находятся в пространстве имен DirectX или DirectX::P Аккедвектор.</span><span class="sxs-lookup"><span data-stu-id="6fc15-127">The DirectXMath types in common with XNA Math are in the “DirectX” or the “DirectX::PackedVector” namespace.</span></span>

<span data-ttu-id="6fc15-128">В исходных файлах C++ простое решение заключается в добавлении операторов using:</span><span class="sxs-lookup"><span data-stu-id="6fc15-128">In C++ source files, a simple solution is to add ‘using’ statements:</span></span>


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



<span data-ttu-id="6fc15-129">Для заголовков не считается рекомендациями по добавлению операторов using.</span><span class="sxs-lookup"><span data-stu-id="6fc15-129">For headers, it is not considered ‘best practice’ to add using statements.</span></span> <span data-ttu-id="6fc15-130">Вместо этого добавьте полные пространства имен:</span><span class="sxs-lookup"><span data-stu-id="6fc15-130">Instead, add fully qualified namespaces:</span></span>


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a><span data-ttu-id="6fc15-131">Частичные загрузки</span><span class="sxs-lookup"><span data-stu-id="6fc15-131">Partial Loads</span></span>

<span data-ttu-id="6fc15-132">Для различных функций, которые загружают менее 4 элементов КСМВЕКТОР, в библиотеке XNA Math не определены дополнительные элементы.</span><span class="sxs-lookup"><span data-stu-id="6fc15-132">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="6fc15-133">Директксмас всегда будет заполнять эти дополнительные элементы 0.</span><span class="sxs-lookup"><span data-stu-id="6fc15-133">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="6fc15-134">Удаление специальных типов для Xbox 360</span><span class="sxs-lookup"><span data-stu-id="6fc15-134">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="6fc15-135">Следующие типы, функции и константы XNA Math Library недоступны в Директксмас.</span><span class="sxs-lookup"><span data-stu-id="6fc15-135">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="6fc15-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="6fc15-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="6fc15-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="6fc15-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="6fc15-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="6fc15-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="6fc15-139">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ ксмадддхен, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="6fc15-139">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="6fc15-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="6fc15-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="6fc15-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="6fc15-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="6fc15-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="6fc15-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="6fc15-143">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="6fc15-143">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="6fc15-144">\_\_vector4i является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="6fc15-144">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="6fc15-145">Вместо этого используйте [**XMVECTORI32**](xmvectori32-data-type.md) или [**XMVECTORU32**](xmvectoru32-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="6fc15-145">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="6fc15-146">Следующие функции и типы являются устаревшими, так как они являются только Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="6fc15-146">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="6fc15-147">Встроенные функции ARM-NEON</span><span class="sxs-lookup"><span data-stu-id="6fc15-147">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="6fc15-148">Объявление векторной константы с этим кодом будет компилироваться для XNA Math для SSE и без встроенных функций, но не будет выполняться для Директксмас с помощью ARM-NEON.</span><span class="sxs-lookup"><span data-stu-id="6fc15-148">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



<span data-ttu-id="6fc15-149">Как правило, не рекомендуется использовать этот метод инициализации [**ксмвектор**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="6fc15-149">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="6fc15-150">Однако, если требуется константа Vector, класс [**XMVECTORF32**](xmvectorf32-data-type.md) поддерживает этот стиль инициализации и возвращает тип **ксмвектор** автоматически, чтобы можно было использовать **XMVECTORF32** в большинстве тех же контекстов.</span><span class="sxs-lookup"><span data-stu-id="6fc15-150">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="6fc15-151">Для выполнения любых операций записи в класс **XMVECTORF32** требуется явная ссылка на элемент **ксмвектор** . v.</span><span class="sxs-lookup"><span data-stu-id="6fc15-151">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="6fc15-152">Переставляют</span><span class="sxs-lookup"><span data-stu-id="6fc15-152">Permute</span></span>

<span data-ttu-id="6fc15-153">Библиотека XNA Math имела следующую форму для общих векторных переставляют:</span><span class="sxs-lookup"><span data-stu-id="6fc15-153">The XNA Math library had the following form for general vector permute:</span></span>


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



<span data-ttu-id="6fc15-154">Для Директксмас было устранено **ксмвекторпермутеконтрол** , а XM \_ переставляют \_ 0x.</span><span class="sxs-lookup"><span data-stu-id="6fc15-154">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="6fc15-155">\_ \_ Константы 1Z переставляют XM были переопределены, чтобы они были простыми индексами 0-7.</span><span class="sxs-lookup"><span data-stu-id="6fc15-155">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="6fc15-156">Вот новая сигнатура для [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span><span class="sxs-lookup"><span data-stu-id="6fc15-156">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



<span data-ttu-id="6fc15-157">Вместо управляющего слова эта функция непосредственно принимает 4 индекса в качестве параметров, что также делает ее аналогом функции [**ксмвекторсвиззле**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) , используя новый XM \_ свиззле \_ X.</span><span class="sxs-lookup"><span data-stu-id="6fc15-157">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="6fc15-158">\_ \_ Константы XM свиззле W определены как простые индексы 0-3.</span><span class="sxs-lookup"><span data-stu-id="6fc15-158">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> <span data-ttu-id="6fc15-159">Для постоянных значений существует гораздо более эффективный способ реализации переставляют.</span><span class="sxs-lookup"><span data-stu-id="6fc15-159">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="6fc15-160">Вместо использования формы функции [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)используйте форму **шаблона** :</span><span class="sxs-lookup"><span data-stu-id="6fc15-160">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="template-forms"></a><span data-ttu-id="6fc15-161">Формы шаблонов</span><span class="sxs-lookup"><span data-stu-id="6fc15-161">Template Forms</span></span>
>
> <span data-ttu-id="6fc15-162">Как правило, использование формы шаблона в форме функции следующих функций значительно более эффективно и позволяет библиотеке выполнять оптимизацию для конкретной платформы с помощью специализации шаблонов.</span><span class="sxs-lookup"><span data-stu-id="6fc15-162">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
>     XMVECTOR XMVectorSwizzle(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateLeft(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateRight(FXMVECTOR V)
>
> template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
>     XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="eliminated-functions"></a><span data-ttu-id="6fc15-163">Исключенные функции</span><span class="sxs-lookup"><span data-stu-id="6fc15-163">Eliminated Functions</span></span>
>
> 
>
> | <span data-ttu-id="6fc15-164">Функция исключена</span><span class="sxs-lookup"><span data-stu-id="6fc15-164">Eliminated Function</span></span>        | <span data-ttu-id="6fc15-165">Замена</span><span class="sxs-lookup"><span data-stu-id="6fc15-165">Replacement</span></span>                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | <span data-ttu-id="6fc15-166">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="6fc15-166">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="6fc15-167">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="6fc15-167">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | <span data-ttu-id="6fc15-168">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="6fc15-168">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="6fc15-169">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="6fc15-169">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | <span data-ttu-id="6fc15-170">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="6fc15-170">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="6fc15-171">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="6fc15-171">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | <span data-ttu-id="6fc15-172">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="6fc15-172">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="6fc15-173">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="6fc15-173">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | <span data-ttu-id="6fc15-174">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="6fc15-174">XMStoreInt4NC</span></span>              | [<span data-ttu-id="6fc15-175">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="6fc15-175">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | <span data-ttu-id="6fc15-176">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="6fc15-176">XMVector2InBoundsR</span></span>         | <span data-ttu-id="6fc15-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="6fc15-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="6fc15-178">[XM \_ КРМАСК \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="6fc15-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="6fc15-179">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="6fc15-179">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="6fc15-180">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="6fc15-180">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | <span data-ttu-id="6fc15-181">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="6fc15-181">XMVector3InBoundsR</span></span>         | <span data-ttu-id="6fc15-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="6fc15-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="6fc15-183">[XM \_ КРМАСК \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="6fc15-183">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="6fc15-184">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="6fc15-184">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="6fc15-185">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="6fc15-185">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | <span data-ttu-id="6fc15-186">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="6fc15-186">XMVector4InBoundsR</span></span>         | <span data-ttu-id="6fc15-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="6fc15-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="6fc15-188">[XM \_ КРМАСК \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="6fc15-188">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="6fc15-189">ксмвекторкошест</span><span class="sxs-lookup"><span data-stu-id="6fc15-189">XMVectorCosHEst</span></span>            | [<span data-ttu-id="6fc15-190">**ксмвекторкош**</span><span class="sxs-lookup"><span data-stu-id="6fc15-190">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | <span data-ttu-id="6fc15-191">ксмвекторекспест</span><span class="sxs-lookup"><span data-stu-id="6fc15-191">XMVectorExpEst</span></span>             | [<span data-ttu-id="6fc15-192">**ксмвекторексп**</span><span class="sxs-lookup"><span data-stu-id="6fc15-192">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | <span data-ttu-id="6fc15-193">ксмвекторложест</span><span class="sxs-lookup"><span data-stu-id="6fc15-193">XMVectorLogEst</span></span>             | [<span data-ttu-id="6fc15-194">**ксмвекторлог**</span><span class="sxs-lookup"><span data-stu-id="6fc15-194">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | <span data-ttu-id="6fc15-195">ксмвекторповест</span><span class="sxs-lookup"><span data-stu-id="6fc15-195">XMVectorPowEst</span></span>             | [<span data-ttu-id="6fc15-196">**ксмвекторпов**</span><span class="sxs-lookup"><span data-stu-id="6fc15-196">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | <span data-ttu-id="6fc15-197">ксмвекторсинхест</span><span class="sxs-lookup"><span data-stu-id="6fc15-197">XMVectorSinHEst</span></span>            | [<span data-ttu-id="6fc15-198">**ксмвекторсинх**</span><span class="sxs-lookup"><span data-stu-id="6fc15-198">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | <span data-ttu-id="6fc15-199">ксмвектортанхест</span><span class="sxs-lookup"><span data-stu-id="6fc15-199">XMVectorTanHEst</span></span>            | [<span data-ttu-id="6fc15-200">**ксмвектортанх**</span><span class="sxs-lookup"><span data-stu-id="6fc15-200">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a><span data-ttu-id="6fc15-201">См. также</span><span class="sxs-lookup"><span data-stu-id="6fc15-201">Related topics</span></span>
>
> <dl> <dt>

[<span data-ttu-id="6fc15-202">Директксмас по программированию</span><span class="sxs-lookup"><span data-stu-id="6fc15-202">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
