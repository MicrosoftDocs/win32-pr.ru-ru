---
title: Индикаторы типов
description: Фактические свойства соответствуют заданным в таблице свойствам идентификаторов свойств и пар значений свойств. Каждое свойство хранится в виде DWORD, за которым следует значение типа данных.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070365"
---
# <a name="type-indicators"></a><span data-ttu-id="82fe2-104">Индикаторы типов</span><span class="sxs-lookup"><span data-stu-id="82fe2-104">Type Indicators</span></span>

<span data-ttu-id="82fe2-105">Фактические свойства соответствуют заданным в таблице свойствам идентификаторов свойств и пар значений свойств.</span><span class="sxs-lookup"><span data-stu-id="82fe2-105">The actual properties follow the table of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="82fe2-106">Каждое свойство хранится в виде **DWORD**, за которым следует значение типа данных.</span><span class="sxs-lookup"><span data-stu-id="82fe2-106">Each property is stored as a **DWORD**, followed by the data type value.</span></span>

<span data-ttu-id="82fe2-107">Индикаторы типов и связанные с ними значения описаны в структуре [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="82fe2-107">Type indicators and their associated values are described in the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="82fe2-108">Все пары "тип-значение" должны начинаться с 32-разрядной границы.</span><span class="sxs-lookup"><span data-stu-id="82fe2-108">All Type/Value pairs must begin on a 32-bit boundary.</span></span> <span data-ttu-id="82fe2-109">Таким тем, для согласования последующей пары на 32-разрядной границе могут быть выполнены значения NULL байта.</span><span class="sxs-lookup"><span data-stu-id="82fe2-109">Thus, values may be followed with null bytes to align the subsequent pair on a 32-bit boundary.</span></span>

<span data-ttu-id="82fe2-110">В следующем примере кода вычисляется число байтов, необходимое для согласования на 32-разрядной границе с учетом числа байтов.</span><span class="sxs-lookup"><span data-stu-id="82fe2-110">The following example code calculates how many bytes are required to align on a 32-bit boundary, given a count of bytes.</span></span>


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



<span data-ttu-id="82fe2-111">В пределах вектора значений каждое повторение простого скалярного значения меньше 32 бит должно быть выровнено с естественным выравниванием, а не с помощью 32-разрядного выравнивания.</span><span class="sxs-lookup"><span data-stu-id="82fe2-111">Within a vector of values, each repetition of a simple scalar value smaller than 32 bits must align with its natural alignment rather than with a 32-bit alignment.</span></span> <span data-ttu-id="82fe2-112">На практике это очень важно только для типов **VT \_ UI1**, **VT \_ UI2**, **VT \_ I2** и **VT \_ bool** (с однобайтовым или двусторонним естественным выравниванием).</span><span class="sxs-lookup"><span data-stu-id="82fe2-112">In practice, this is only significant for types **VT\_UI1**, **VT\_UI2**, **VT\_I2**, and **VT\_BOOL** (which have one-byte or two-byte natural alignment).</span></span> <span data-ttu-id="82fe2-113">Все остальные типы имеют двухбайтовое естественное выравнивание.</span><span class="sxs-lookup"><span data-stu-id="82fe2-113">All other types have four-byte natural alignment.</span></span> <span data-ttu-id="82fe2-114">Некоторые типы, например **VT \_ R8**, фактически имеют 8-байтовое естественное выравнивание, но хранятся в виде четырех байтов.</span><span class="sxs-lookup"><span data-stu-id="82fe2-114">Some types, for example, **VT\_R8**, actually have 8-byte natural alignment, but are stored as if they have four-byte alignment.</span></span>

<span data-ttu-id="82fe2-115">Значение свойства с индикатором типа **VT \_ I2** \| **VT \_ vector** включает:</span><span class="sxs-lookup"><span data-stu-id="82fe2-115">A property value with type indicator **VT\_I2** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="82fe2-116">Число элементов **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="82fe2-116">A **DWORD** element count.</span></span>
-   <span data-ttu-id="82fe2-117">Последовательность упакованных двухбайтовых целых чисел без заполнения NULL между ними.</span><span class="sxs-lookup"><span data-stu-id="82fe2-117">A sequence of packed two-byte integers with no null padding between them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82fe2-118">Все 32-разрядные числа или типы свойств, которые хранятся в составе элемента свойства Vector, также должны быть согласованы с 32-битным.</span><span class="sxs-lookup"><span data-stu-id="82fe2-118">Any 32-bit counts or property types that are stored as a part of a vector property element must also be 32-bit aligned.</span></span>

 

<span data-ttu-id="82fe2-119">Значение свойства идентификатора типа **VT \_ LPSTR** \| **\_ вектор VT** включает:</span><span class="sxs-lookup"><span data-stu-id="82fe2-119">A property value of type identifier **VT\_LPSTR** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="82fe2-120">Число элементов **типа DWORD** (**DWORD** *целемс*).</span><span class="sxs-lookup"><span data-stu-id="82fe2-120">A **DWORD** element count (**DWORD** *cElems*).</span></span>
-   <span data-ttu-id="82fe2-121">Последовательность строк (**char** *РГЧ \[ \]*), каждая из которых предшествует **параметру типа DWORD** , а может следовать за заполнением значения NULL для округления до 32-разрядной границы.</span><span class="sxs-lookup"><span data-stu-id="82fe2-121">A sequence of strings (**char** *rgch\[\]*), each preceded by a length-count **DWORD** and possibly followed by null padding to round to a 32-bit boundary.</span></span>

 

 