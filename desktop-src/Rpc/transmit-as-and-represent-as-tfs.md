---
title: Transmit_as и Represent_as
description: Передача \_ as и представляется \_ совместно с одним и тем же макетом, за исключением начального маркера. Этот маркер считывает, что FC \_ передает \_ as или FC \_ \_ как, но базовый код является общим.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987551"
---
# <a name="transmit_as-and-represent_as"></a><span data-ttu-id="41fa0-103">Передать \_ как и представить \_ как</span><span class="sxs-lookup"><span data-stu-id="41fa0-103">Transmit\_as and Represent\_as</span></span>

<span data-ttu-id="41fa0-104">Передача \_ as и представляется \_ совместно с одним и тем же макетом, за исключением начального маркера. Этот маркер считывает, что FC \_ передает \_ as или FC \_ \_ как, но базовый код является общим.</span><span class="sxs-lookup"><span data-stu-id="41fa0-104">Transmit\_as and represent\_as share the same layout except for the leading token; the token reads FC\_TRANSMIT\_AS or FC\_REPRESENT\_AS, but the underlying code is common.</span></span>

<span data-ttu-id="41fa0-105">Описание имеет следующий макет:</span><span class="sxs-lookup"><span data-stu-id="41fa0-105">The description has the following layout:</span></span>

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

<span data-ttu-id="41fa0-106">Флаги<1> байт состоят из верхнего флага, а также более низкого выравнивания.</span><span class="sxs-lookup"><span data-stu-id="41fa0-106">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="41fa0-107">Выравнивание по сети обеспечивает выравнивание передачи для передаваемого типа.</span><span class="sxs-lookup"><span data-stu-id="41fa0-107">The alignment nibble keeps the wire alignment of the transmitted type.</span></span> <span data-ttu-id="41fa0-108">Это необходимо при определении размера буфера и использовании переданного размера типа из кода формата.</span><span class="sxs-lookup"><span data-stu-id="41fa0-108">This is needed when buffer sizing and using the transmitted type size from the format code.</span></span>

<span data-ttu-id="41fa0-109">Флаг может иметь следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="41fa0-109">The flag nibble can have the following flags:</span></span>

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

<span data-ttu-id="41fa0-110">ПРЕДСТАВЛЕНный \_ тип \_ является \_ флагом массива. аргумент передается как (или представляет AS) верхнего уровня как массив какого-либо значения, переданного по значению.</span><span class="sxs-lookup"><span data-stu-id="41fa0-110">The PRESENTED\_TYPE\_IS\_ARRAY flag marks a top-level transmit as (or represent as) argument being an array of something and passed-by value.</span></span> <span data-ttu-id="41fa0-111">Интерпретатор [**-Oi**](/windows/desktop/Midl/-oi) использует этот флаг для прохода по такому аргументу (который фактически является указателем в стеке, а не массивом).</span><span class="sxs-lookup"><span data-stu-id="41fa0-111">The [**–Oi**](/windows/desktop/Midl/-oi) interpreter uses this flag to step over such an argument (which is actually a pointer on stack, not the array).</span></span> <span data-ttu-id="41fa0-112">Два других флага также используются только в предыдущих интерпретаторах для корректного шага над представленным типом в стеке.</span><span class="sxs-lookup"><span data-stu-id="41fa0-112">The other two flags are also used only in previous interpreters to step correctly over a presented type on the stack.</span></span>

<span data-ttu-id="41fa0-113">Индекс пятиэлементные \_<2> является индексом подпрограммы обратного вызова пятиэлементные (на самом деле это четверное) функций.</span><span class="sxs-lookup"><span data-stu-id="41fa0-113">The quintuple\_index<2> is an index of the callback routine quintuple (this is actually a quadruple) of functions.</span></span> <span data-ttu-id="41fa0-114">Таблица обычно используется как для передачи как, так и для представления, и существует очевидное сопоставление для позиции подпрограмм, так как одна и та же служба точек входа может передавать и представлять как коды.</span><span class="sxs-lookup"><span data-stu-id="41fa0-114">The table is common to both transmit as and represent as and there is an obvious mapping for the position of the routines, as the same entry points service transmit as and represent as codes.</span></span> <span data-ttu-id="41fa0-115">Сопоставление происходит от \_ Local => к \_ xmit, to \_ Local => из \_ xmit, Free \_ inst => Free \_ xmit, бесплатное \_ локально => Free \_ inst.</span><span class="sxs-lookup"><span data-stu-id="41fa0-115">The mapping is from\_local => to\_xmit, to\_local => from\_xmit, free\_inst => free\_xmit, free\_local => free\_inst.</span></span>

<span data-ttu-id="41fa0-116">Размер отображаемого \_ типа \_ памяти \_<2> всегда предоставляет размер для представленного/локального типа, включая Unknown — как типы.</span><span class="sxs-lookup"><span data-stu-id="41fa0-116">The presented\_type\_memory\_size<2> always provides a size for the presented/local type, including unknown represent as types.</span></span>

<span data-ttu-id="41fa0-117">\_Размер переданного \_ буфера типа \_<2> равен нулю, при изменении размера или фактическим фиксированном размере.</span><span class="sxs-lookup"><span data-stu-id="41fa0-117">The transmitted\_type\_buffer\_size<2> is either zero, when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="41fa0-118">Это оптимизация, которая позволяет пропускать некоторые обратные вызовы при изменении размера буфера.</span><span class="sxs-lookup"><span data-stu-id="41fa0-118">This is an optimization that enables skipping some callbacks when sizing the buffer.</span></span>

<span data-ttu-id="41fa0-119">Переданное \_ \_ смещение типа<2> — это обычное смещение относительно типа к передаваемой строке формата типа.</span><span class="sxs-lookup"><span data-stu-id="41fa0-119">The transmitted\_type\_offset<2> is the usual relative type offset to the transmitted type format string.</span></span>

 

 