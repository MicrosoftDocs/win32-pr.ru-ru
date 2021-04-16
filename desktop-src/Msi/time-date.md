---
description: Тип данных "время/Дата" имеет время и дату, хранимую по отдельности, с использованием целых чисел без знака в качестве битовых полей, упакованных следующим образом.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Время и Дата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650846"
---
# <a name="timedate"></a><span data-ttu-id="cbfa5-103">Время и Дата</span><span class="sxs-lookup"><span data-stu-id="cbfa5-103">Time/Date</span></span>

<span data-ttu-id="cbfa5-104">Тип данных "время/Дата" имеет время и дату, хранимую по отдельности, с использованием целых чисел без знака в качестве битовых полей, упакованных следующим образом.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-104">The Time/Date data type has the time and the date stored individually, using unsigned integers as bit fields, packed as follows.</span></span>

## <a name="time"></a><span data-ttu-id="cbfa5-105">Время</span><span class="sxs-lookup"><span data-stu-id="cbfa5-105">Time</span></span>

<span data-ttu-id="cbfa5-106">Время кодируется в виде 2-байтового целого числа без знака со следующими битовыми полями.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-106">Time is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="cbfa5-107">Содержимое</span><span class="sxs-lookup"><span data-stu-id="cbfa5-107">Contents</span></span>           | <span data-ttu-id="cbfa5-108">Bits</span><span class="sxs-lookup"><span data-stu-id="cbfa5-108">Bits</span></span>        | <span data-ttu-id="cbfa5-109">Диапазон значений</span><span class="sxs-lookup"><span data-stu-id="cbfa5-109">Value range</span></span> |
|--------------------|-------------|-------------|
| <span data-ttu-id="cbfa5-110">часы</span><span class="sxs-lookup"><span data-stu-id="cbfa5-110">hours</span></span>              | <span data-ttu-id="cbfa5-111">0 1 2 3 4</span><span class="sxs-lookup"><span data-stu-id="cbfa5-111">0 1 2 3 4</span></span>   | <span data-ttu-id="cbfa5-112">0–23</span><span class="sxs-lookup"><span data-stu-id="cbfa5-112">0–23</span></span>        |
| <span data-ttu-id="cbfa5-113">minutes</span><span class="sxs-lookup"><span data-stu-id="cbfa5-113">minutes</span></span>            | <span data-ttu-id="cbfa5-114">5 6 7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="cbfa5-114">5 6 7 8 9 A</span></span> | <span data-ttu-id="cbfa5-115">0–59</span><span class="sxs-lookup"><span data-stu-id="cbfa5-115">0–59</span></span>        |
| <span data-ttu-id="cbfa5-116">2-секундные интервалы</span><span class="sxs-lookup"><span data-stu-id="cbfa5-116">2-second intervals</span></span> | <span data-ttu-id="cbfa5-117">B C D E F</span><span class="sxs-lookup"><span data-stu-id="cbfa5-117">B C D E F</span></span>   | <span data-ttu-id="cbfa5-118">0 – 29</span><span class="sxs-lookup"><span data-stu-id="cbfa5-118">0–29</span></span>        |



 

## <a name="date"></a><span data-ttu-id="cbfa5-119">Дата</span><span class="sxs-lookup"><span data-stu-id="cbfa5-119">Date</span></span>

<span data-ttu-id="cbfa5-120">Дата кодируется в виде 2-байтового целого числа без знака со следующими битовыми полями.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-120">Date is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="cbfa5-121">Содержимое</span><span class="sxs-lookup"><span data-stu-id="cbfa5-121">Contents</span></span> | <span data-ttu-id="cbfa5-122">Bits</span><span class="sxs-lookup"><span data-stu-id="cbfa5-122">Bits</span></span>          | <span data-ttu-id="cbfa5-123">Диапазон значений</span><span class="sxs-lookup"><span data-stu-id="cbfa5-123">Value range</span></span>              |
|----------|---------------|--------------------------|
| <span data-ttu-id="cbfa5-124">year</span><span class="sxs-lookup"><span data-stu-id="cbfa5-124">year</span></span>     | <span data-ttu-id="cbfa5-125">0 1 2 3 4 5 6</span><span class="sxs-lookup"><span data-stu-id="cbfa5-125">0 1 2 3 4 5 6</span></span> | <span data-ttu-id="cbfa5-126">0 – 119 (относительно 1980)</span><span class="sxs-lookup"><span data-stu-id="cbfa5-126">0–119 (relative to 1980)</span></span> |
| <span data-ttu-id="cbfa5-127">month</span><span class="sxs-lookup"><span data-stu-id="cbfa5-127">month</span></span>    | <span data-ttu-id="cbfa5-128">7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="cbfa5-128">7 8 9 A</span></span>       | <span data-ttu-id="cbfa5-129">1–12</span><span class="sxs-lookup"><span data-stu-id="cbfa5-129">1–12</span></span>                     |
| <span data-ttu-id="cbfa5-130">day</span><span class="sxs-lookup"><span data-stu-id="cbfa5-130">day</span></span>      | <span data-ttu-id="cbfa5-131">B C D E F</span><span class="sxs-lookup"><span data-stu-id="cbfa5-131">B C D E F</span></span>     | <span data-ttu-id="cbfa5-132">1–31</span><span class="sxs-lookup"><span data-stu-id="cbfa5-132">1–31</span></span>                     |



 

 

 



