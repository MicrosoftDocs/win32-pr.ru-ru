---
title: Вопросы упаковки C-компилятора
description: Уровни упаковки влияют на компоновку памяти типов как для MIDL, так и для компилятора Microsoft C/C++ аналогичным образом.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL-компилятор MIDL, проблемы с упаковкой в компиляторе C
- Упаковка MIDL
- MIDL макета памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890576"
---
# <a name="c-compiler-packing-issues"></a><span data-ttu-id="7894b-106">Вопросы упаковки C-компилятора</span><span class="sxs-lookup"><span data-stu-id="7894b-106">C-Compiler Packing Issues</span></span>

<span data-ttu-id="7894b-107">Уровни упаковки влияют на компоновку памяти типов как для MIDL, так и для компилятора Microsoft C/C++ аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="7894b-107">Packing levels affect the memory layout of types for both MIDL and the Microsoft C/C++ compiler in the same way.</span></span> <span data-ttu-id="7894b-108">В средах Microsoft Build, таких как среда сборки, определенная с помощью VC + + или пакета средств разработки программного обеспечения платформы (SDK), уровень упаковки по умолчанию для компиляторов MIDL и C/C++ не отличается. по умолчанию для 32-разрядных и 64-разрядных сред сборки Windows используется уровень упаковки 8.</span><span class="sxs-lookup"><span data-stu-id="7894b-108">In Microsoft build environments, such as the build environment defined by VC++ or the Platform Software Development Kit (SDK), the default packing level for MIDL and C/C++ compilers is the same; the default packing level for the 32-bit and 64-bit Windows build environments is 8.</span></span>

## <a name="natural-alignment"></a><span data-ttu-id="7894b-109">Естественное выравнивание</span><span class="sxs-lookup"><span data-stu-id="7894b-109">Natural Alignment</span></span>

<span data-ttu-id="7894b-110">Для типов в памяти выравнивание по умолчанию аналогично его естественному выравниванию.</span><span class="sxs-lookup"><span data-stu-id="7894b-110">For types in memory, the default alignment is the same as its natural alignment.</span></span>

-   <span data-ttu-id="7894b-111">Базовый тип, например Short, float и \_ \_ Int64, и указатель выровнены естественным образом, если его представление начинается с адреса по модулю его размера.</span><span class="sxs-lookup"><span data-stu-id="7894b-111">A base type, such as short, float and \_\_int64, and a pointer is aligned naturally if its representation starts at an address that is modulo its size.</span></span> <span data-ttu-id="7894b-112">Все поддерживаемые в настоящее время базовые типы имеют размеры 1, 2, 4 или 8.</span><span class="sxs-lookup"><span data-stu-id="7894b-112">All the currently supported base types have sizes of 1, 2, 4 or 8.</span></span> <span data-ttu-id="7894b-113">Указатели имеют размер 4 в 32-разрядных средах и 8 в 64-разрядных средах.</span><span class="sxs-lookup"><span data-stu-id="7894b-113">Pointers have a size of 4 in 32-bit environments and 8 in 64-bit environments.</span></span>
-   <span data-ttu-id="7894b-114">Составной тип согласуется естественным образом, если каждый из его компонентов выровнен естественным образом относительно начала типа, и если между компонентами нет лишних пробелов (заполнений).</span><span class="sxs-lookup"><span data-stu-id="7894b-114">A compound type is aligned naturally if each of its components is aligned naturally relative to the beginning of the type, and if there are no unnecessary gaps (padding) between components.</span></span> <span data-ttu-id="7894b-115">Комплексные компоненты, такие как поля или элементы, рекурсируют на компоненты указателя или базового типа.</span><span class="sxs-lookup"><span data-stu-id="7894b-115">Compound components, such as fields or elements, are recursed to pointer or base type components.</span></span>

<span data-ttu-id="7894b-116">Простое правило, помогающее запомнить это поведение, заключается в том, что естественное выравнивание типа равно наибольшему выравниванию его компонентов.</span><span class="sxs-lookup"><span data-stu-id="7894b-116">A simple rule to help remember this behavior is that the natural alignment of a type is equal to the biggest alignments of its components.</span></span>

<span data-ttu-id="7894b-117">Между выравниванием и размером памяти для типа в таких языках, как C или C++ и IDL, существует соединение, выраженное оператором **sizeof ()**.</span><span class="sxs-lookup"><span data-stu-id="7894b-117">There is a connection between alignment and memory size of a type in languages like C or C++ and IDL as expressed by the operator **sizeof()**.</span></span> <span data-ttu-id="7894b-118">Размер является кратным выравниванию (минимально кратным охвату типа).</span><span class="sxs-lookup"><span data-stu-id="7894b-118">The size is a multiple of the alignment (the minimal multiple spanning the type).</span></span> <span data-ttu-id="7894b-119">Это следует за представлением массива в памяти.</span><span class="sxs-lookup"><span data-stu-id="7894b-119">This follows from an array representation in memory.</span></span>

<span data-ttu-id="7894b-120">Естественное выравнивание важно, так как доступ к невыровненным данным может вызвать исключение в некоторых системах.</span><span class="sxs-lookup"><span data-stu-id="7894b-120">Natural alignment is important because accessing misaligned data may cause an exception on some systems.</span></span> <span data-ttu-id="7894b-121">Данные могут быть помечены для безопасной манипуляции при неправильном согласовании, но обычно это подразумевает снижение скорости, которое может быть значительным на некоторых платформах.</span><span class="sxs-lookup"><span data-stu-id="7894b-121">Data can be marked for a safe manipulation when misaligned, but typically that involves a speed penalty that may be substantial on some platforms.</span></span>

> [!Note]  
> <span data-ttu-id="7894b-122">В памяти объекты типов с естественным выравниванием *n* гарантированно должны быть правильно выровнены при размещении по адресам, кратным *n*.</span><span class="sxs-lookup"><span data-stu-id="7894b-122">In memory, objects of types with a natural alignment of *n* are guaranteed to be aligned properly when placed at addresses that are a multiple of *n*.</span></span>

 

## <a name="packing-versus-alignment"></a><span data-ttu-id="7894b-123">Упаковка и выравнивание</span><span class="sxs-lookup"><span data-stu-id="7894b-123">Packing versus Alignment</span></span>

<span data-ttu-id="7894b-124">Задание уровня упаковки, превышающего естественное выравнивание типа, не изменяет выравнивание типа.</span><span class="sxs-lookup"><span data-stu-id="7894b-124">Specifying a packing level larger than the natural alignment of a type does not change the type alignment.</span></span> <span data-ttu-id="7894b-125">Задание уровня упаковки меньше естественного выравнивания уменьшает выравнивание типа до уровня упаковки.</span><span class="sxs-lookup"><span data-stu-id="7894b-125">Specifying a packing level smaller than the natural alignment reduces the type alignment to the packing level.</span></span> <span data-ttu-id="7894b-126">В результате Упакованные типы могут размещаться в памяти по адресам, кратным уровню упаковки (сокращенное выравнивание), не вызывая неправильного выравнивания.</span><span class="sxs-lookup"><span data-stu-id="7894b-126">As a result, the packed types may be placed in memory at addresses that are a multiple of the packing level (the reduced alignment) without causing a misalignment.</span></span> <span data-ttu-id="7894b-127">Это влияет на простые типы и типы компонентов.</span><span class="sxs-lookup"><span data-stu-id="7894b-127">This affects both simple types and component types.</span></span> <span data-ttu-id="7894b-128">Для составных типов может быть затронуто внутренняя структура типа, так как уменьшение выравнивания компонентов может изменить размер заполнения, необходимый для правильного выравнивания компонентов, таким образом уменьшая размер типа.</span><span class="sxs-lookup"><span data-stu-id="7894b-128">For compound types, the internal layout of the type may be affected, because the reduced alignment of the components may change the size of padding necessary for the proper alignment of the components, thus reducing the size of the type.</span></span>

<span data-ttu-id="7894b-129">Простое правило, помогающее запомнить это поведение, заключается в том, что новое выравнивание упакованного типа меньше уровня упаковки и его естественного выравнивания.</span><span class="sxs-lookup"><span data-stu-id="7894b-129">A simple rule to help remember this behavior is that the new alignment of a packed type is the smaller of the packing level and its natural alignment.</span></span> <span data-ttu-id="7894b-130">Размер типа является кратным новому выравниванию.</span><span class="sxs-lookup"><span data-stu-id="7894b-130">The size of the type is a multiple of the new alignment.</span></span> <span data-ttu-id="7894b-131">Оператор **sizeof ()** Возвращает уменьшенный размер упакованных типов.</span><span class="sxs-lookup"><span data-stu-id="7894b-131">The **sizeof()** operator returns the reduced size for packed types.</span></span>

<span data-ttu-id="7894b-132">Например, если уровень упаковки 2 является длинным, он выравнивается по 2 и, следовательно, может быть размещен на любом четном адресе, а не только на адресах, кратных 4, как при естественном выравнивании.</span><span class="sxs-lookup"><span data-stu-id="7894b-132">For example, with packing level 2 a long becomes aligned at 2, and therefore may be placed at any even address, not only at the addresses that are a multiple of 4 as would be the case with natural alignment.</span></span> <span data-ttu-id="7894b-133">Для структуры с коротким и длинным, упакованным в 2, не требуется внутренний зазор между коротким и длительным временем, который был необходим для естественного выравнивания. Следовательно, не только структура, выравниваемая по отношению к 2, также имеет размер, уменьшенный с 8 до 6.</span><span class="sxs-lookup"><span data-stu-id="7894b-133">A structure with a short and a long, packed at 2, does not need the internal gap between the short and the following long that was necessary for the natural alignment; hence, not only is the structure now aligned at 2, it also has its size reduced from 8 to 6.</span></span>

<span data-ttu-id="7894b-134">В качестве примера рассмотрим составной тип, состоящий из 1-байтного символа, целого числа 4 байт и 1-байтового символа:</span><span class="sxs-lookup"><span data-stu-id="7894b-134">As an example, consider a compound type consisting of a 1-byte character, an integer 4 bytes long, and a 1-byte character:</span></span>

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

<span data-ttu-id="7894b-135">Эта структура естественным образом выровнена по 4 и имеет натуральный размер 12.</span><span class="sxs-lookup"><span data-stu-id="7894b-135">This structure is naturally aligned at 4 and has the natural size of 12.</span></span>

<span data-ttu-id="7894b-136">Для уровня упаковки 4 или выше структура **MyStruct** соответствует 4 и `sizeof(struct mystructtype)` равна 12.</span><span class="sxs-lookup"><span data-stu-id="7894b-136">For packing level 4 or greater, the structure **mystruct** is aligned at 4 and `sizeof(struct mystructtype)` is equal to 12.</span></span> <span data-ttu-id="7894b-137">Структура будет неправильно согласована, если она находится в памяти по адресу, не кратному 4.</span><span class="sxs-lookup"><span data-stu-id="7894b-137">The structure will be misaligned if located in memory at an address that is not a multiple of 4.</span></span>

<span data-ttu-id="7894b-138">Для уровня упаковки 2 Структура выровняться по 2, а ее размер — 8.</span><span class="sxs-lookup"><span data-stu-id="7894b-138">For packing level 2, the structure is aligned at 2 and its size is 8.</span></span> <span data-ttu-id="7894b-139">Структура, упакованная с уровнем 2, будет неправильно согласована, если она находится в памяти по адресу, не кратному 2.</span><span class="sxs-lookup"><span data-stu-id="7894b-139">The structure packed with level 2 will be misaligned if located in memory at an address that is not a multiple of 2.</span></span>

<span data-ttu-id="7894b-140">Для уровня упаковки 1 структура соответствует 1, а ее размер — 6.</span><span class="sxs-lookup"><span data-stu-id="7894b-140">For packing level 1, the structure is aligned at 1 and its size is 6.</span></span> <span data-ttu-id="7894b-141">Структуру, упакованную с уровнем 1, можно разместить в любом месте, не вызывая ошибки выравнивания.</span><span class="sxs-lookup"><span data-stu-id="7894b-141">The structure packed with level 1 can be placed anywhere without causing a misalignment fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7894b-142">См. также</span><span class="sxs-lookup"><span data-stu-id="7894b-142">Related topics</span></span>

<dl> <span data-ttu-id="7894b-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="7894b-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="7894b-144">/ZP</span><span class="sxs-lookup"><span data-stu-id="7894b-144">/Zp</span></span>](./-zp.md)
</dt> <dt>

[<span data-ttu-id="7894b-145">/Pack</span><span class="sxs-lookup"><span data-stu-id="7894b-145">/pack</span></span>](./-pack.md)
</dt> </dl>

 

 