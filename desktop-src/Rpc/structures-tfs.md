---
title: Структуры (RPC)
description: Описание различных типов структур в удаленном вызове процедур (RPC).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070349"
---
# <a name="structures-rpc"></a><span data-ttu-id="f7cb5-103">Структуры (RPC)</span><span class="sxs-lookup"><span data-stu-id="f7cb5-103">Structures (RPC)</span></span>

<span data-ttu-id="f7cb5-104">Существует несколько категорий структур, которые постепенно более сложны в отношении действий, необходимых для маршалирования.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-104">There are several categories of structures, progressively more complicated in terms of actions required for marshaling.</span></span> <span data-ttu-id="f7cb5-105">Они начинаются с простой структуры, которую можно блокировать, копировать в целом и продолжать до сложной структуры, которая должна обслуживаться полем по полю.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-105">They begin with a simple structure that can be block-copied as a whole, and continue to a complex structure that has to be serviced field by field.</span></span>

-   [<span data-ttu-id="f7cb5-106">Простая структура</span><span class="sxs-lookup"><span data-stu-id="f7cb5-106">Simple Structure</span></span>](#simple-structure)
-   [<span data-ttu-id="f7cb5-107">Простая структура с указателями</span><span class="sxs-lookup"><span data-stu-id="f7cb5-107">Simple Structure with Pointers</span></span>](#simple-structure-with-pointers)
-   [<span data-ttu-id="f7cb5-108">Согласованная структура</span><span class="sxs-lookup"><span data-stu-id="f7cb5-108">Conformant Structure</span></span>](#conformant-structure)
-   [<span data-ttu-id="f7cb5-109">Согласованная структура с указателями</span><span class="sxs-lookup"><span data-stu-id="f7cb5-109">Conformant Structure with Pointers</span></span>](#conformant-structure-with-pointers)
-   [<span data-ttu-id="f7cb5-110">Согласованная структура (с указателями или без них)</span><span class="sxs-lookup"><span data-stu-id="f7cb5-110">Conformant Varying Structure (with or without Pointers)</span></span>](#conformant-varying-structure-with-or-without-pointers)
-   [<span data-ttu-id="f7cb5-111">Жесткая структура</span><span class="sxs-lookup"><span data-stu-id="f7cb5-111">Hard Structure</span></span>](#hard-structure)
-   [<span data-ttu-id="f7cb5-112">Сложная структура</span><span class="sxs-lookup"><span data-stu-id="f7cb5-112">Complex Structure</span></span>](#complex-structure)
-   [<span data-ttu-id="f7cb5-113">Описание макета элемента структуры</span><span class="sxs-lookup"><span data-stu-id="f7cb5-113">Structure Member Layout Description</span></span>](#structure-member-layout-description)

> [!Note]  
> <span data-ttu-id="f7cb5-114">По сравнению с категориями массива становится ясно, что можно описать только структуры размером до 64 КБ (размер для плоской части структуры), то есть не имеет эквивалента массивов SM и LG.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-114">When compared to array categories, it becomes clear that only structures up to 64k in size can be described (the size is for the flat part of the structure), that is there is no equivalent of SM and LG arrays.</span></span>

 

<span data-ttu-id="f7cb5-115">**Элементы, общие для структур**</span><span class="sxs-lookup"><span data-stu-id="f7cb5-115">**Members Common to Structures**</span></span>

-   <span data-ttu-id="f7cb5-116">**Выравнивание**</span><span class="sxs-lookup"><span data-stu-id="f7cb5-116">**alignment**</span></span>

    <span data-ttu-id="f7cb5-117">Необходимое выравнивание буфера перед деупаковкой структуры.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-117">The necessary alignment of the buffer before unmarshaling the structure.</span></span> <span data-ttu-id="f7cb5-118">Допустимые значения: 0, 1, 3 и 7 (фактическое выравнивание минус 1).</span><span class="sxs-lookup"><span data-stu-id="f7cb5-118">Valid values are 0, 1, 3, and 7 (the actual alignment minus 1).</span></span>

-   <span data-ttu-id="f7cb5-119">**\_объем памяти**</span><span class="sxs-lookup"><span data-stu-id="f7cb5-119">**memory\_size**</span></span>

    <span data-ttu-id="f7cb5-120">Размер структуры в памяти в байтах; для согласованных структур этот размер не включает размер массива.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-120">Size of the structure in memory in bytes; for conformant structures this size does not include the array's size.</span></span>

-   <span data-ttu-id="f7cb5-121">**смещение \_ к \_ \_ описанию массива**</span><span class="sxs-lookup"><span data-stu-id="f7cb5-121">**offset\_to\_array\_description**</span></span>

    <span data-ttu-id="f7cb5-122">Смещение от текущего указателя строки формата к описанию согласованного массива, содержащегося в структуре.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-122">Offset from the current format string pointer to the description of the conformant array contained in a structure.</span></span>

-   <span data-ttu-id="f7cb5-123">**\_макет элемента**</span><span class="sxs-lookup"><span data-stu-id="f7cb5-123">**member\_layout**</span></span>

    <span data-ttu-id="f7cb5-124">Описание каждого элемента структуры.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-124">Description of each element of the structure.</span></span> <span data-ttu-id="f7cb5-125">Подпрограммы NDR должны проверять эту часть строки формата типа, если требуется преобразование с обратным порядком байтов или если тип является сложной структурой.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-125">The NDR routines only need to examine this portion of a type's format string if endian transformation is needed or if the type is a complex structure.</span></span>

-   <span data-ttu-id="f7cb5-126">**\_Макет указателя**</span><span class="sxs-lookup"><span data-stu-id="f7cb5-126">**pointer\_layout**</span></span>

    <span data-ttu-id="f7cb5-127">См. раздел [Макет указателя](pointer-layout-tfs.md) .</span><span class="sxs-lookup"><span data-stu-id="f7cb5-127">See the [Pointer Layout](pointer-layout-tfs.md) section.</span></span>

## <a name="simple-structure"></a><span data-ttu-id="f7cb5-128">Простая структура</span><span class="sxs-lookup"><span data-stu-id="f7cb5-128">Simple Structure</span></span>

<span data-ttu-id="f7cb5-129">Простая структура содержит только базовые типы, фиксированные массивы и другие простые структуры.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-129">A simple structure contains only base types, fixed arrays, and other simple structures.</span></span> <span data-ttu-id="f7cb5-130">Основная функция простой структуры заключается в том, что ее можно блокировать и копировать в целом.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-130">The main feature of the simple structure is that it can be block-copied as a whole.</span></span>

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a><span data-ttu-id="f7cb5-131">Простая структура с указателями</span><span class="sxs-lookup"><span data-stu-id="f7cb5-131">Simple Structure with Pointers</span></span>

<span data-ttu-id="f7cb5-132">Простая структура с указателями содержит только базовые типы, указатели, фиксированные массивы, простые структуры и другие простые структуры с указателями.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-132">A simple structure with pointers contains only base types, pointers, fixed arrays, simple structures, and other simple structures with pointers.</span></span> <span data-ttu-id="f7cb5-133">Так как при преобразовании архитектуре необходимо только посещение<> макета, оно помещается в конец описания.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-133">Because the layout<> will only have to be visited when doing an endianess conversion, it is placed at the end of the description.</span></span>

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a><span data-ttu-id="f7cb5-134">Согласованная структура</span><span class="sxs-lookup"><span data-stu-id="f7cb5-134">Conformant Structure</span></span>

<span data-ttu-id="f7cb5-135">Согласованная структура содержит только базовые типы, фиксированные массивы и простые структуры и должна содержать либо согласованную строку, либо согласованный массив.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-135">A conformant structure contains only base types, fixed arrays, and simple structures, and must contain either a conformant string or a conformant array.</span></span> <span data-ttu-id="f7cb5-136">Этот массив фактически может содержаться в другой согласованной структуре или в согласованной структуре с указателями, внедренными в эту структуру.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-136">This array could actually be contained in another conformant structure or conformant structure with pointers which is embedded in this structure.</span></span>

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a><span data-ttu-id="f7cb5-137">Согласованная структура с указателями</span><span class="sxs-lookup"><span data-stu-id="f7cb5-137">Conformant Structure with Pointers</span></span>

<span data-ttu-id="f7cb5-138">Согласованная структура с указателями содержит только базовые типы, указатели, фиксированные массивы, простые структуры и простые структуры с указателями. Согласованная структура должна содержать согласованный массив.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-138">A conformant structure with pointers contains only base types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant structure must contain a conformant array.</span></span> <span data-ttu-id="f7cb5-139">Этот массив фактически может содержаться в другой согласованной структуре или в согласованной структуре с указателями, внедренными в эту структуру.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-139">This array could actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a><span data-ttu-id="f7cb5-140">Согласованная структура (с указателями или без них)</span><span class="sxs-lookup"><span data-stu-id="f7cb5-140">Conformant Varying Structure (with or without Pointers)</span></span>

<span data-ttu-id="f7cb5-141">В согласованной различной структуре содержатся только простые типы, указатели, фиксированные массивы, простые структуры и простые структуры с указателями. Согласованная структура должна содержать либо согласованную строку, либо согласованный, изменяющихся массив.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-141">A conformant varying structure contains only simple types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant varying structure must contain either a conformant string or a conformant-varying array.</span></span> <span data-ttu-id="f7cb5-142">Согласованная строка или массив фактически могут содержаться в другой согласованной структуре или согласованной структуре с указателями, внедренными в эту структуру.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-142">The conformant string or array can actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a><span data-ttu-id="f7cb5-143">Жесткая структура</span><span class="sxs-lookup"><span data-stu-id="f7cb5-143">Hard Structure</span></span>

<span data-ttu-id="f7cb5-144">Жесткая структура была концепцией, направленной на устранение тяжелых потерь, связанных с обработкой сложных структур.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-144">The hard structure was a concept aimed at eliminating steep penalties related to processing complex structures.</span></span> <span data-ttu-id="f7cb5-145">Он является производным от наблюдения за тем, что сложная структура обычно имеет только одно или два условия, предотвращающие копирование блоков и, следовательно, вредно его производительность по сравнению с простой структурой.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-145">It is derived from an observation that a complex structure typically has only one or two conditions that prevent block-copying, and therefore spoil its performance compared to a simple structure.</span></span> <span data-ttu-id="f7cb5-146">Эти причины обычно являются объединениями или полями перечисления.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-146">The culprits are usually unions or enumeration fields.</span></span>

<span data-ttu-id="f7cb5-147">Жесткая структура — это структура с enum16, заполнением в памяти или объединением в качестве последнего элемента.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-147">A hard structure is a structure that has an enum16, end-padding in memory, or a union as the last member.</span></span> <span data-ttu-id="f7cb5-148">Эти три элемента препятствуют переходу структуры в одну из предыдущих категорий структуры, что повлияет на небольшие издержки на интерпретацию и максимальную оптимизацию, но не следует применять их к категории очень дорогостоящей сложной структуры.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-148">These three elements prevent the structure from falling into one of the previous structure categories, which enjoy small interpretation overhead and maximum optimization potential, but do not force it into the very costly complex structure category.</span></span>

<span data-ttu-id="f7cb5-149">Enum16 не должен приводить к разным размерам памяти и сети в структуре.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-149">The enum16 must not cause the memory and wire sizes of the structure to differ.</span></span> <span data-ttu-id="f7cb5-150">Структура не может иметь ни одного согласованного массива или ни одного указателя (если только часть объединения); единственными допустимыми членами являются базовые типы, фиксированные массивы и простые структуры.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-150">The structure cannot have any conformant array, nor any pointers (unless part of the union); the only other members allowed are base types, fixed arrays, and simple structures.</span></span>

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

<span data-ttu-id="f7cb5-151">Смещение Enum \_<2> предоставляет смещение от начала структуры в памяти до enum16, если оно содержит единицу. в противном случае \_ смещение enum<2> поле равно – 1.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-151">The enum\_offset<2> field provides the offset from the beginning of the structure in memory to an enum16 if it contains one; otherwise the enum\_offset<2> field is –1.</span></span>

<span data-ttu-id="f7cb5-152">\_Поле размер копии<2> предоставляет общее число байтов в структуре, которые могут быть заблокированы в буфере или скопированы в него.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-152">The copy\_size<2> field provides the total number of bytes in the structure, which may be block-copied into/from the buffer.</span></span> <span data-ttu-id="f7cb5-153">Этот итог не включает в себя все замыкающие объединения и заполнение в памяти.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-153">This total does not include any trailing union nor any end-padding in memory.</span></span> <span data-ttu-id="f7cb5-154">Это значение также представляет собой величину, с которой указатель буфера должен увеличиваться после копирования.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-154">This value is also the amount the buffer pointer should be incremented following the copy.</span></span>

<span data-ttu-id="f7cb5-155">Поле MEM \_ Copy \_ incr<2> — это количество байтов, которое должен увеличить указатель памяти после блока-Copy перед обработкой любого замыкающего объединения.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-155">The mem\_copy\_incr<2> field is the number of bytes the memory pointer should be incremented following the block-copy before handling any trailing union.</span></span> <span data-ttu-id="f7cb5-156">Приращение в этом объеме (не по \_ размеру копии<2> байтах) приводит к правильному указателю на память для любого замыкающего объединения.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-156">Incrementing by this amount (not by copy\_size<2> bytes) yields a proper memory pointer to any trailing union.</span></span>

## <a name="complex-structure"></a><span data-ttu-id="f7cb5-157">Сложная структура</span><span class="sxs-lookup"><span data-stu-id="f7cb5-157">Complex Structure</span></span>

<span data-ttu-id="f7cb5-158">Сложная структура — это любая структура, содержащая одно или несколько полей, которые либо препятствуют копированию в блок, либо, для которой должна быть выполнена дополнительная проверка во время маршалирования или распаковки (например, связанные проверки перечисления).</span><span class="sxs-lookup"><span data-stu-id="f7cb5-158">A complex structure is any structure containing one or more fields that either prevent the structure from being block-copied, or for which additional checking must be performed during marshaling or unmarshaling (for example, bound checks on an enumeration).</span></span> <span data-ttu-id="f7cb5-159">Следующие типы NDR относятся к этой категории:</span><span class="sxs-lookup"><span data-stu-id="f7cb5-159">The following NDR types fall in this category:</span></span>

-   <span data-ttu-id="f7cb5-160">[простые типы](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (только на 64-разрядных платформах), интеграл с \[ [ **диапазоном**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="f7cb5-160">[simple types](simple-types-tfs.md): ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="f7cb5-161">Выравнивание отступа в конце структуры</span><span class="sxs-lookup"><span data-stu-id="f7cb5-161">alignment padding at the end of the structure</span></span>
-   <span data-ttu-id="f7cb5-162">указатели интерфейса (они используют внедренный сложный)</span><span class="sxs-lookup"><span data-stu-id="f7cb5-162">interface pointers (they go using an embedded complex)</span></span>
-   <span data-ttu-id="f7cb5-163">Игнорируемые указатели (которые связаны с \[ [](/windows/desktop/Midl/ignore) \] атрибутом Ignore и \_ маркером игнорирования токена FC)</span><span class="sxs-lookup"><span data-stu-id="f7cb5-163">ignored pointers (that is related to \[[**ignore**](/windows/desktop/Midl/ignore)\] attribute and FC\_IGNORE token)</span></span>
-   <span data-ttu-id="f7cb5-164">сложные массивы, различные массивы, массивы строк</span><span class="sxs-lookup"><span data-stu-id="f7cb5-164">complex arrays, varying arrays, string arrays</span></span>
-   <span data-ttu-id="f7cb5-165">многомерные массивы, имеющие по меньшей мере одно нефиксированное измерение</span><span class="sxs-lookup"><span data-stu-id="f7cb5-165">multidimensional conformant arrays with at least one nonfixed dimension</span></span>
-   <span data-ttu-id="f7cb5-166">объединения</span><span class="sxs-lookup"><span data-stu-id="f7cb5-166">unions</span></span>
-   <span data-ttu-id="f7cb5-167">элементы, определенные с помощью \[ [**передачи \_ as**](/windows/desktop/Midl/transmit-as) \] , \[ [**представляются \_ как**](/windows/desktop/Midl/represent-as) \] , \[ [**проводная \_ Упаковка**](/windows/desktop/Midl/wire-marshal) \] , \[ [**\_ маршалирование пользователя**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="f7cb5-167">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**represent\_as**](/windows/desktop/Midl/represent-as)\], \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="f7cb5-168">внедренные сложные структуры</span><span class="sxs-lookup"><span data-stu-id="f7cb5-168">embedded complex structures</span></span>
-   <span data-ttu-id="f7cb5-169">заполнение в конце структуры</span><span class="sxs-lookup"><span data-stu-id="f7cb5-169">padding at the end of the structure</span></span>

<span data-ttu-id="f7cb5-170">Сложная структура имеет следующее описание формата:</span><span class="sxs-lookup"><span data-stu-id="f7cb5-170">A complex structure has the following format description:</span></span>

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

<span data-ttu-id="f7cb5-171">Размер памяти \_<2> поле — это размер структуры в памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-171">The memory\_size<2> field is the size of the structure in memory, in bytes.</span></span>

<span data-ttu-id="f7cb5-172">Если структура содержит согласованный массив, то смещение \_ в \_ \_ описании соответствия массиву \_<2> поле предоставляет смещение к описанию согласованного массива, в противном случае — ноль.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-172">If the structure contains a conformant array, the offset\_to\_conformant\_array\_description<2> field provides the offset to the conformant array's description, otherwise it is zero.</span></span>

<span data-ttu-id="f7cb5-173">Если структура имеет указатели, то смещение \_ в \_ \_ макете указателя<2> поле предоставляет смещение после макета структуры указателем, в противном случае это поле равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-173">If the structure has pointers, the offset\_to\_pointer\_layout<2> field provides the offset past the structure's layout to the pointer layout, otherwise this field is zero.</span></span>

<span data-ttu-id="f7cb5-174">Макет указателя \_<> поле сложной структуры обрабатывается несколько иначе, чем для других структур.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-174">The pointer\_layout<> field of a complex structure is handled somewhat differently than for other structures.</span></span> <span data-ttu-id="f7cb5-175">Макет указателя \_<> поле сложной структуры содержит только описания фактических полей указателя в самой структуре.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-175">The pointer\_layout<> field of a complex structure only contains descriptions of actual pointer fields in the structure itself.</span></span> <span data-ttu-id="f7cb5-176">Любые указатели, содержащиеся в любых внедренных массивах, объединениях или структурах, не описываются в макете указателя сложной структуры \_<> поле.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-176">Any pointers contained within any embedded arrays, unions, or structures are not described in the complex structure's pointer\_layout<> field.</span></span>

> [!Note]  
> <span data-ttu-id="f7cb5-177">Это отличается от других структур, которые дублируют описание всех указателей, содержащихся во внедренных массивах или структурах, в их собственном \_ макете указателя<> поле.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-177">This is in contrast to other structures, which duplicate the description of any pointers contained in embedded arrays or structures in their own pointer \_layout<> field as well.</span></span>

 

<span data-ttu-id="f7cb5-178">Формат макета с указателем сложной структуры также имеет коренные отличия.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-178">The format of a complex structure's pointer layout is also radically different.</span></span> <span data-ttu-id="f7cb5-179">Так как он содержит только описания фактических элементов указателя, а сложная структура упакована и неупакована по одному полю за раз, \_ Макет указателя<> поле просто содержит описание указателя всех членов указателя.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-179">Because it only contains descriptions of actual pointer members and because a complex structure is marshaled and unmarshaled one field at a time, the pointer\_layout<> field simply contains the pointer description of all pointer members.</span></span> <span data-ttu-id="f7cb5-180">PP FC не существует \_ , и ни один из обычных макетов указателей не \_<> информации.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-180">There is no beginning FC\_PP, and none of the usual pointer\_layout<> information.</span></span>

## <a name="structure-member-layout-description"></a><span data-ttu-id="f7cb5-181">Описание макета элемента структуры</span><span class="sxs-lookup"><span data-stu-id="f7cb5-181">Structure Member Layout Description</span></span>

<span data-ttu-id="f7cb5-182">Описание макета структуры содержит один или несколько следующих символов формата:</span><span class="sxs-lookup"><span data-stu-id="f7cb5-182">A structure's layout description contains one or more of the following format characters:</span></span>

-   <span data-ttu-id="f7cb5-183">Любой из символов базового типа, например FC \_ char и т. д.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-183">Any of the base type characters, like FC\_CHAR, and so on</span></span>
-   <span data-ttu-id="f7cb5-184">Директивы выравнивания.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-184">Alignment directives.</span></span> <span data-ttu-id="f7cb5-185">Существует три символа формата, определяющие выравнивание указателя памяти: FC \_ ALIGNM2, FC \_ ALIGNM4 и FC \_ ALIGNM8.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-185">There are three format characters specifying alignment of the memory pointer: FC\_ALIGNM2, FC\_ALIGNM4, and FC\_ALIGNM8.</span></span>
    > [!Note]  
    > <span data-ttu-id="f7cb5-186">Существуют также маркеры выравнивания буфера, FC \_ ALIGNB2 через FC \_ ALIGNM8; они не используются.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-186">There are also buffer alignment tokens, FC\_ALIGNB2 through FC\_ALIGNM8; these are not used.</span></span>

     

-   <span data-ttu-id="f7cb5-187">Заполнение памяти.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-187">Memory padding.</span></span> <span data-ttu-id="f7cb5-188">Они происходят только в конце описания структуры и обозначают число байтов заполнения в памяти перед согласованным массивом в структуре: FC \_ структпадн, где n — число байтов заполнения.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-188">These occur only at the end of a structure's description and denote the number of bytes of padding in memory before the conformant array in the structure: FC\_STRUCTPADn, where n is the number of bytes of padding.</span></span>
-   <span data-ttu-id="f7cb5-189">Любой внедренный небазовый тип (Обратите внимание, что согласованный массив никогда не происходит в макете структуры).</span><span class="sxs-lookup"><span data-stu-id="f7cb5-189">Any embedded nonbase type (note, however, that a conformant array never occurs in the structure layout).</span></span> <span data-ttu-id="f7cb5-190">Это 4-байтное описание:</span><span class="sxs-lookup"><span data-stu-id="f7cb5-190">This has a 4-byte description:</span></span>

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    <span data-ttu-id="f7cb5-191">где смещение не гарантируется в 2 байта.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-191">where the offset is not guaranteed to be 2-byte aligned.</span></span>

    <span data-ttu-id="f7cb5-192">\_панель памяти<1> — это дополнение, необходимое в памяти перед сложным полем.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-192">memory\_pad<1> is a padding needed in memory before the complex field.</span></span>

    <span data-ttu-id="f7cb5-193">смещение \_ к \_ описанию<2> — это относительное смещение типа к внедренному типу.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-193">offset\_to\_description<2> is a relative type offset to the embedded type.</span></span>

<span data-ttu-id="f7cb5-194">Кроме того \_ , при необходимости можно использовать клавиатуру FC перед завершающим \_ ЗАВЕРШЕНИЕм FC, чтобы обеспечить выравнивание строки формата по 2-байтовой границе после \_ конца FC.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-194">There may also be an FC\_PAD before the terminating FC\_END if needed to ensure that the format string will be aligned at a 2-byte boundary following the FC\_END.</span></span>

 

 