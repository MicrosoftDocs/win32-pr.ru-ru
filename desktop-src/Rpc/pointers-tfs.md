---
title: Указатели (RPC)
description: Сведения об общем указателе RPC, который определен как все, кроме указателей интерфейса и указателей количества байтов.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e41a0b6208745b543a9efe2fe22ab090046778
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406597"
---
# <a name="pointers-rpc"></a><span data-ttu-id="28fd5-103">Указатели (RPC)</span><span class="sxs-lookup"><span data-stu-id="28fd5-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="28fd5-104">Общие указатели</span><span class="sxs-lookup"><span data-stu-id="28fd5-104">Common Pointers</span></span>

<span data-ttu-id="28fd5-105">Общий указатель определяется так же, как и все указатели интерфейса и числа байтов.</span><span class="sxs-lookup"><span data-stu-id="28fd5-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="28fd5-106">Существует два возможных макета для описания:</span><span class="sxs-lookup"><span data-stu-id="28fd5-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="28fd5-107">–или–</span><span class="sxs-lookup"><span data-stu-id="28fd5-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="28fd5-108">Первый формат используется, если указатель является указателем на простой тип или неизмененный указатель на строку.</span><span class="sxs-lookup"><span data-stu-id="28fd5-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="28fd5-109">Второй формат используется для указателей на все остальные типы.</span><span class="sxs-lookup"><span data-stu-id="28fd5-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="28fd5-110">Атрибуты указателя указывают, какой макет описания имеет \_ флаг простого указателя FC \_ .</span><span class="sxs-lookup"><span data-stu-id="28fd5-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="28fd5-111">\_тип указателя<1> является одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="28fd5-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="28fd5-112">Символ формата</span><span class="sxs-lookup"><span data-stu-id="28fd5-112">Format character</span></span> | <span data-ttu-id="28fd5-113">Описание</span><span class="sxs-lookup"><span data-stu-id="28fd5-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="28fd5-114">FC \_ RP</span><span class="sxs-lookup"><span data-stu-id="28fd5-114">FC\_RP</span></span>           | <span data-ttu-id="28fd5-115">Указатель ссылки.</span><span class="sxs-lookup"><span data-stu-id="28fd5-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="28fd5-116">FC \_</span><span class="sxs-lookup"><span data-stu-id="28fd5-116">FC\_UP</span></span>           | <span data-ttu-id="28fd5-117">Уникальный указатель.</span><span class="sxs-lookup"><span data-stu-id="28fd5-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="28fd5-118">FC \_ FP</span><span class="sxs-lookup"><span data-stu-id="28fd5-118">FC\_FP</span></span>           | <span data-ttu-id="28fd5-119">Полный указатель.</span><span class="sxs-lookup"><span data-stu-id="28fd5-119">A full pointer.</span></span>                          |
| <span data-ttu-id="28fd5-120">FC \_ Op</span><span class="sxs-lookup"><span data-stu-id="28fd5-120">FC\_OP</span></span>           | <span data-ttu-id="28fd5-121">Уникальный указатель в интерфейсе объекта.</span><span class="sxs-lookup"><span data-stu-id="28fd5-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="28fd5-122">Основанием для различения операций FC \_ -операций является семантика: в объектных интерфейсах \[ \] перед деупаковкой нового объекта и присваиванием нового значения указателя следует освободить указатель in.</span><span class="sxs-lookup"><span data-stu-id="28fd5-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="28fd5-123">\_Атрибуты указателя<1> могут иметь любой из флагов, показанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="28fd5-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="28fd5-124">Flag</span><span class="sxs-lookup"><span data-stu-id="28fd5-124">Flag</span></span> | <span data-ttu-id="28fd5-125">Описание</span><span class="sxs-lookup"><span data-stu-id="28fd5-125">Description</span></span>              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28fd5-126">01</span><span class="sxs-lookup"><span data-stu-id="28fd5-126">01</span></span>   | <span data-ttu-id="28fd5-127">FC \_ выделяет \_ все \_ узлы</span><span class="sxs-lookup"><span data-stu-id="28fd5-127">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="28fd5-128">Указатель является частью \_ схемы выделения размещения (все узлы).</span><span class="sxs-lookup"><span data-stu-id="28fd5-128">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="28fd5-129">02</span><span class="sxs-lookup"><span data-stu-id="28fd5-129">02</span></span>   | <span data-ttu-id="28fd5-130">FC \_ не \_ бесплатно</span><span class="sxs-lookup"><span data-stu-id="28fd5-130">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="28fd5-131">Указатель выделения (не \_ свободен).</span><span class="sxs-lookup"><span data-stu-id="28fd5-131">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="28fd5-132">04</span><span class="sxs-lookup"><span data-stu-id="28fd5-132">04</span></span>   | <span data-ttu-id="28fd5-133">FC, \_ выделено \_ в \_ стеке</span><span class="sxs-lookup"><span data-stu-id="28fd5-133">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="28fd5-134">Указатель, референт которого выделяется в стеке заглушки.</span><span class="sxs-lookup"><span data-stu-id="28fd5-134">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="28fd5-135">08</span><span class="sxs-lookup"><span data-stu-id="28fd5-135">08</span></span>   | <span data-ttu-id="28fd5-136">\_простой \_ указатель FC</span><span class="sxs-lookup"><span data-stu-id="28fd5-136">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="28fd5-137">Указатель на простой тип или неизмененную строку соответствия.</span><span class="sxs-lookup"><span data-stu-id="28fd5-137">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="28fd5-138">Этот флаг задает расположение описания указателя как простой макет указателя, описанный выше, в противном случае указывается формат дескриптора с смещением.</span><span class="sxs-lookup"><span data-stu-id="28fd5-138">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="28fd5-139">10</span><span class="sxs-lookup"><span data-stu-id="28fd5-139">10</span></span>   | <span data-ttu-id="28fd5-140">FC, \_ указатель \_ DEREF</span><span class="sxs-lookup"><span data-stu-id="28fd5-140">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="28fd5-141">Указатель, который должен быть разыменован перед обработкой референт указателя.</span><span class="sxs-lookup"><span data-stu-id="28fd5-141">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="28fd5-142">Указатели, имеющие размер \_ , — (), \_ Функция Max имеет значение (), Length \_ — (), Last \_ — (), а/или First \_ — (). к ним применяются описания строк формата, идентичные указателю на массив соответствующего типа (например, соответствует массиву, если применяется параметр size \_ (), \_ и применяется длина, соответствующий различным массивам \_ .</span><span class="sxs-lookup"><span data-stu-id="28fd5-142">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="28fd5-143">Указатели интерфейса</span><span class="sxs-lookup"><span data-stu-id="28fd5-143">Interface Pointers</span></span>

<span data-ttu-id="28fd5-144">Строка формата указателя на интерфейс объекта имеет один из двух форматов в зависимости от того, известен ли компилятору соответствующий идентификатор IID.</span><span class="sxs-lookup"><span data-stu-id="28fd5-144">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="28fd5-145">Указатель интерфейса с постоянным IID имеет следующее описание:</span><span class="sxs-lookup"><span data-stu-id="28fd5-145">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="28fd5-146">IID<16> является фактическим IID для указателя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="28fd5-146">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="28fd5-147">IID записывается в строку формата в формате, идентичном структуре данных GUID: длинная, короткая, короткая, символьная \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="28fd5-147">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="28fd5-148">К нему применено описание указателя интерфейса с IID \_ ():</span><span class="sxs-lookup"><span data-stu-id="28fd5-148">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="28fd5-149">Описание IID \_<> является дескриптором корреляции и имеет 4 или 6 байт в зависимости от того, используется ли [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="28fd5-149">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="28fd5-150">Значение, вычисленное функцией **ндркомпутеконформанце** , является указателем IID.</span><span class="sxs-lookup"><span data-stu-id="28fd5-150">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="28fd5-151">Указатели числа байтов</span><span class="sxs-lookup"><span data-stu-id="28fd5-151">Byte Count Pointers</span></span>

<span data-ttu-id="28fd5-152">Указатели счетчика байтов относятся к Специальному атрибуту оптимизации, который называется \[ **\_ числом байтов** \] .</span><span class="sxs-lookup"><span data-stu-id="28fd5-152">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="28fd5-153">Используются следующие форматы:</span><span class="sxs-lookup"><span data-stu-id="28fd5-153">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="28fd5-154">перетаскивани</span><span class="sxs-lookup"><span data-stu-id="28fd5-154">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="28fd5-155">\_Описание счетчика байтов \_<> является дескриптором корреляции и имеет 4 или 6 байт в зависимости от того, используется ли [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="28fd5-155">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="28fd5-156">В \_ описании<> является описание типа Point.</span><span class="sxs-lookup"><span data-stu-id="28fd5-156">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
