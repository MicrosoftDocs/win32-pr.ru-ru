---
description: Определяет идентификатор GUID, который может использоваться в других шаблонах.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: GUID (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537226"
---
# <a name="guid-directx-9"></a><span data-ttu-id="76617-103">GUID (DirectX 9)</span><span class="sxs-lookup"><span data-stu-id="76617-103">Guid (DirectX 9)</span></span>

<span data-ttu-id="76617-104">Определяет идентификатор GUID, который может использоваться в других шаблонах.</span><span class="sxs-lookup"><span data-stu-id="76617-104">Defines a GUID that can be used in other templates.</span></span>

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

<span data-ttu-id="76617-105">Где параметры вместе формируют формат двоичного хранилища для GUID:</span><span class="sxs-lookup"><span data-stu-id="76617-105">Where the parameters together form the binary storage format for a GUID:</span></span>

-   <span data-ttu-id="76617-106">файл1 — 32-разрядное целочисленное значение без знака</span><span class="sxs-lookup"><span data-stu-id="76617-106">data1 - 32-bit unsigned integer data value</span></span>
-   <span data-ttu-id="76617-107">значение файл2 — 16-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="76617-107">data2 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="76617-108">data3 — 16-разрядное целочисленное значение без знака</span><span class="sxs-lookup"><span data-stu-id="76617-108">data3 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="76617-109">data4 — Массив беззнаковых символов</span><span class="sxs-lookup"><span data-stu-id="76617-109">data4 - An array of unsigned characters</span></span>

## <a name="see-also"></a><span data-ttu-id="76617-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76617-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76617-111">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="76617-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



