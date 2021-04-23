---
title: Логическое значение (WMI)
description: '\_Параметр VT bool, принимающий значение Variant \_ TRUE (&\# 8211; 1) или вариант \_ false (0).'
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702839"
---
# <a name="boolean-wmi"></a><span data-ttu-id="8cf82-103">Логическое значение (WMI)</span><span class="sxs-lookup"><span data-stu-id="8cf82-103">boolean (WMI)</span></span>

<span data-ttu-id="8cf82-104">Логический тип данных — это \_ параметр логического типа VT, принимающий значение Variant \_ true (– 1) или Variant \_ false (0).</span><span class="sxs-lookup"><span data-stu-id="8cf82-104">The boolean data type is a VT\_BOOL parameter that takes on the value of VARIANT\_TRUE (–1) or VARIANT\_FALSE (0).</span></span> <span data-ttu-id="8cf82-105">В следующей таблице приведена разница между программными представлениями логического значения **true** в C/C++ и типом автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8cf82-105">The following table lists the difference between the programmatic representations of logical **TRUE** in C/C++ and the Automation type.</span></span>

| <span data-ttu-id="8cf82-106">Язык</span><span class="sxs-lookup"><span data-stu-id="8cf82-106">Language</span></span>   | <span data-ttu-id="8cf82-107">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf82-107">Value</span></span>         | <span data-ttu-id="8cf82-108">Числовое значение</span><span class="sxs-lookup"><span data-stu-id="8cf82-108">Numerical value</span></span> |
|------------|---------------|-----------------|
| <span data-ttu-id="8cf82-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="8cf82-109">C/C++</span></span>      | <span data-ttu-id="8cf82-110">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="8cf82-110">**TRUE**</span></span>      | <span data-ttu-id="8cf82-111">1</span><span class="sxs-lookup"><span data-stu-id="8cf82-111">1</span></span>               |
| <span data-ttu-id="8cf82-112">Автоматизация</span><span class="sxs-lookup"><span data-stu-id="8cf82-112">Automation</span></span> | <span data-ttu-id="8cf82-113">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="8cf82-113">VARIANT\_TRUE</span></span> | <span data-ttu-id="8cf82-114">–1</span><span class="sxs-lookup"><span data-stu-id="8cf82-114">–1</span></span>              |

<span data-ttu-id="8cf82-115">Оба типа являются ненулевыми и, следовательно, не равны **false**, но имеют разные представления для **true**.</span><span class="sxs-lookup"><span data-stu-id="8cf82-115">Both types are nonzero and therefore not **FALSE**, but have different representations for **TRUE**.</span></span>
