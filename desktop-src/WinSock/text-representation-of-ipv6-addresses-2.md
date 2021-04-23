---
description: Этот раздел копируется из &\# 0034; Архитектура адресации IPv6&\# 0034; по R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Текстовое представление адресов IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711758"
---
# <a name="text-representation-of-ipv6-addresses"></a><span data-ttu-id="eefe0-103">Текстовое представление адресов IPv6</span><span class="sxs-lookup"><span data-stu-id="eefe0-103">Text Representation of IPv6 Addresses</span></span>

<span data-ttu-id="eefe0-104">Этот раздел копируется с "Архитектура IPv6-адресации" на R. хинден и S. Диринг.</span><span class="sxs-lookup"><span data-stu-id="eefe0-104">This section is copied from "IPv6 Addressing Architecture" by R. Hinden and S. Deering.</span></span> <span data-ttu-id="eefe0-105">Существуют три обычные формы для представления IPv6-адресов в виде текстовых строк:</span><span class="sxs-lookup"><span data-stu-id="eefe0-105">There are three conventional forms for representing IPv6 addresses as text strings:</span></span>

-   <span data-ttu-id="eefe0-106">Предпочтительная форма — x:x: x:x: x:x: x:x, где «x — шестнадцатеричные значения 8 16-разрядного фрагмента адреса.</span><span class="sxs-lookup"><span data-stu-id="eefe0-106">The preferred form is x:x:x:x:x:x:x:x, where the 'x's are the hexadecimal values of the eight 16-bit pieces of the address.</span></span>

    <span data-ttu-id="eefe0-107">Примеры:</span><span class="sxs-lookup"><span data-stu-id="eefe0-107">Examples:</span></span>

    <dl> <span data-ttu-id="eefe0-108">ФЕДК: BA98:7654:3210: ФЕДК: BA98:7654:3210</span><span class="sxs-lookup"><span data-stu-id="eefe0-108">FEDC:BA98:7654:3210:FEDC:BA98:7654:3210</span></span>  
    <span data-ttu-id="eefe0-109">1080:0: 0:0: 8:800:200C: 417A</span><span class="sxs-lookup"><span data-stu-id="eefe0-109">1080:0:0:0:8:800:200C:417A</span></span>  
    </dl>

> [!Note]  
> <span data-ttu-id="eefe0-110">Нет необходимости писать ведущие нули в отдельном поле, но в каждом поле должно быть по крайней мере одно число (за исключением случая, описанного во второй форме).</span><span class="sxs-lookup"><span data-stu-id="eefe0-110">It is not necessary to write the leading zeros in an individual field, but there must be at least one numeral in every field (except for the case described in the second form).</span></span>

 

-   <span data-ttu-id="eefe0-111">Из-за метода выделения определенных стилей IPv6-адресов обычно адреса содержат длинные строки нулевых битов.</span><span class="sxs-lookup"><span data-stu-id="eefe0-111">Due to the method of allocating certain styles of IPv6 addresses, it is common for addresses to contain long strings of zero bits.</span></span> <span data-ttu-id="eefe0-112">Чтобы упростить запись адресов, содержащих нулевые биты, можно использовать специальный синтаксис для сжатия нулей.</span><span class="sxs-lookup"><span data-stu-id="eefe0-112">In order to make writing addresses containing zero bits easier, a special syntax is available to compress the zeros.</span></span> <span data-ttu-id="eefe0-113">Использование двойных двоеточий ("::") указывает на множество групп 16-разрядных нулей.</span><span class="sxs-lookup"><span data-stu-id="eefe0-113">The use of double colons ("::") indicates multiple groups of 16-bits of zeros.</span></span>

    <span data-ttu-id="eefe0-114">Например, адрес многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="eefe0-114">For example, the multicast address</span></span>

    <dl> <span data-ttu-id="eefe0-115">FF01:0: 0:0: 0:0: 0:43</span><span class="sxs-lookup"><span data-stu-id="eefe0-115">FF01:0:0:0:0:0:0:43</span></span>  
    </dl>

    <span data-ttu-id="eefe0-116">может быть представлено следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eefe0-116">may be represented as:</span></span>

    <dl> <span data-ttu-id="eefe0-117">FF01:: 43</span><span class="sxs-lookup"><span data-stu-id="eefe0-117">FF01::43</span></span>  
    </dl>

    <span data-ttu-id="eefe0-118">Двойные кавычки ("::") могут появляться в адресе только один раз.</span><span class="sxs-lookup"><span data-stu-id="eefe0-118">The double quotation marks ("::") can only appear once in an address.</span></span> <span data-ttu-id="eefe0-119">Они могут использоваться для сжатия начальных и конечных нулей в адресе.</span><span class="sxs-lookup"><span data-stu-id="eefe0-119">They can be used to compress leading or trailing zeros in an address.</span></span>

-   <span data-ttu-id="eefe0-120">Альтернативная форма, которая может быть удобнее при работе со смешанной средой узлов IPv4 и IPv6, — это x:x: x:x: x:x: d. d. d. d, где "x" — это шестнадцатеричные значения шести 16-разрядных частей адреса, а "d" — десятичные значения четырех младших 8-разрядных частей адреса (стандартное представление IPv4).</span><span class="sxs-lookup"><span data-stu-id="eefe0-120">An alternative form that may be more convenient when dealing with a mixed environment of IPv4 and IPv6 nodes is x:x:x:x:x:x:d.d.d.d, where the 'x's are the hexadecimal values of the six high-order 16-bit pieces of the address, and the 'd's are the decimal values of the four low-order 8-bit pieces of the address (standard IPv4 representation).</span></span>

    <span data-ttu-id="eefe0-121">Примеры:</span><span class="sxs-lookup"><span data-stu-id="eefe0-121">Examples:</span></span>

    <dl> <span data-ttu-id="eefe0-122">0:0: 0 — 0:0: 0:13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="eefe0-122">0:0:0:0:0:0:13.1.68.3</span></span>  
    <span data-ttu-id="eefe0-123">0:0 — 0:0: 0: FFFF: 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="eefe0-123">0:0:0:0:0:FFFF:129.144.52.38</span></span>  
    </dl>

    <span data-ttu-id="eefe0-124">или в сжатой форме:</span><span class="sxs-lookup"><span data-stu-id="eefe0-124">or in compressed form:</span></span>

    <dl> <span data-ttu-id="eefe0-125">:: 13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="eefe0-125">::13.1.68.3</span></span>  
    <span data-ttu-id="eefe0-126">:: FFFF: 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="eefe0-126">::FFFF:129.144.52.38</span></span>  
    </dl>

 

 



