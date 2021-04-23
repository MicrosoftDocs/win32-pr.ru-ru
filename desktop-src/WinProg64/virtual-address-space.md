---
title: Виртуальное адресное пространство (руководством по программированию для 64-разрядной версии Windows)
description: По умолчанию для 64-разрядных приложений на основе Microsoft Windows используется адресное пространство пользовательского режима, равное нескольким терабайтам.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- '64-разрядное программное обеспечено в Windows: 64-разрядное программирование для Windows, виртуальное адресное пространство'
- виртуальное адресное пространство 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070926"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a><span data-ttu-id="81d94-105">Виртуальное адресное пространство (руководством по программированию для 64-разрядной версии Windows)</span><span class="sxs-lookup"><span data-stu-id="81d94-105">Virtual Address Space (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="81d94-106">По умолчанию для 64-разрядных приложений на основе Microsoft Windows используется адресное пространство пользовательского режима, равное нескольким терабайтам.</span><span class="sxs-lookup"><span data-stu-id="81d94-106">By default, 64-bit Microsoft Windows-based applications have a user-mode address space of several terabytes.</span></span> <span data-ttu-id="81d94-107">Точные значения см. в разделе [ограничения памяти для выпусков Windows и Windows Server](/windows/desktop/Memory/memory-limits-for-windows-releases).</span><span class="sxs-lookup"><span data-stu-id="81d94-107">For precise values, see [Memory Limits for Windows and Windows Server Releases](/windows/desktop/Memory/memory-limits-for-windows-releases).</span></span> <span data-ttu-id="81d94-108">Однако приложения могут указать, что система должна выделить всю память для приложения, приведенного ниже 2 гигабайта.</span><span class="sxs-lookup"><span data-stu-id="81d94-108">However, applications can specify that the system should allocate all memory for the application below 2 gigabytes.</span></span> <span data-ttu-id="81d94-109">Эта функция полезна для 64-разрядных приложений, если выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="81d94-109">This feature is beneficial for 64-bit applications if the following conditions are true:</span></span>

-   <span data-ttu-id="81d94-110">Достаточно пространства адресов в 2 ГБ.</span><span class="sxs-lookup"><span data-stu-id="81d94-110">A 2 GB address space is sufficient.</span></span>
-   <span data-ttu-id="81d94-111">В коде содержится много предупреждений усечения указателя.</span><span class="sxs-lookup"><span data-stu-id="81d94-111">The code has many pointer truncation warnings.</span></span>
-   <span data-ttu-id="81d94-112">Указатели и целые числа могут быть свободно смешанными.</span><span class="sxs-lookup"><span data-stu-id="81d94-112">Pointers and integers are freely mixed.</span></span>
-   <span data-ttu-id="81d94-113">В коде имеется полиморфизм, использующий 32-разрядные типы данных.</span><span class="sxs-lookup"><span data-stu-id="81d94-113">The code has polymorphism using 32-bit data types.</span></span>

<span data-ttu-id="81d94-114">Все указатели по-прежнему являются 64-битовыми указателями, но система гарантирует, что каждое выделение памяти будет выполняться ниже ограничения в 2 ГБ, поэтому если приложение усекает указатель, существенные данные не теряются.</span><span class="sxs-lookup"><span data-stu-id="81d94-114">All pointers are still 64-bit pointers, but the system ensures that every memory allocation occurs below the 2 GB limit, so that if the application truncates a pointer, no significant data is lost.</span></span> <span data-ttu-id="81d94-115">Указатели могут быть усечены до 32-битных значений, затем расширены до 64-разрядных значений с помощью расширения знака или нулевого расширения.</span><span class="sxs-lookup"><span data-stu-id="81d94-115">Pointers can be truncated to 32-bit values, then extended to 64-bit values by either sign extension or zero extension.</span></span>

<span data-ttu-id="81d94-116">Чтобы указать это ограничение памяти, используйте параметр компоновщика **/LARGEADDRESSAWARE: No** .</span><span class="sxs-lookup"><span data-stu-id="81d94-116">To specify this memory limitation, use the **/LARGEADDRESSAWARE:NO** linker option.</span></span> <span data-ttu-id="81d94-117">Обратите внимание, что **/LARGEADDRESSAWARE: No** не учитывается для двоичного файла ARM64.</span><span class="sxs-lookup"><span data-stu-id="81d94-117">Note that **/LARGEADDRESSAWARE:NO** is ignored for an ARM64 binary.</span></span> <span data-ttu-id="81d94-118">Однако имейте в виду, что при использовании этого параметра могут возникнуть проблемы.</span><span class="sxs-lookup"><span data-stu-id="81d94-118">However, be aware that problems can occur when using this option.</span></span> <span data-ttu-id="81d94-119">Если создается библиотека DLL, использующая этот параметр, а библиотека DLL вызывается приложением, которое не использует этот параметр, то библиотека DLL может усечь 64-разрядный указатель, верхний 32 которого имеет большое значение.</span><span class="sxs-lookup"><span data-stu-id="81d94-119">If you build a DLL that uses this option and the DLL is called by an application that does not use this option, the DLL could truncate a 64-bit pointer whose upper 32 bits are significant.</span></span> <span data-ttu-id="81d94-120">Это может привести к сбою приложения без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="81d94-120">This can cause application failure without any warning.</span></span>

 

 
