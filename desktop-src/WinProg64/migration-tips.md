---
title: Советы по миграции
description: Важно учитывать вычисления адресов и арифметические операции с указателями при переносе кода в 64-разрядную версию Windows.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- 64-разрядное руководством по программированию Windows 64-разрядное программирование для Windows, советы по миграции
- Советы по миграции — 64-разрядное программирование для Windows
- совместимость с 64-разрядным программированием для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777246"
---
# <a name="migration-tips"></a><span data-ttu-id="9430d-106">Советы по миграции</span><span class="sxs-lookup"><span data-stu-id="9430d-106">Migration Tips</span></span>

<span data-ttu-id="9430d-107">При проверке кода на совместимость с 64-разрядной архитектурой следует учитывать два основных аспекта:</span><span class="sxs-lookup"><span data-stu-id="9430d-107">The two primary areas of concern when examining your code for 64-bit compatibility are as follows:</span></span>

-   <span data-ttu-id="9430d-108">Вычисления адресов</span><span class="sxs-lookup"><span data-stu-id="9430d-108">Address calculations</span></span>
-   <span data-ttu-id="9430d-109">Расчеты указателей</span><span class="sxs-lookup"><span data-stu-id="9430d-109">Pointer arithmetic</span></span>

<span data-ttu-id="9430d-110">По многим причинам, разработчики могут хранить адреса в виде значения типа **ulong** .</span><span class="sxs-lookup"><span data-stu-id="9430d-110">For many reasons, developers have stored addresses as a **ULONG** value.</span></span> <span data-ttu-id="9430d-111">В конце концов, в 32-разрядных Windows адрес, указатель и значение **ulong** имеют длину 32 бит.</span><span class="sxs-lookup"><span data-stu-id="9430d-111">After all, on 32-bit Windows, an address, a pointer, and a **ULONG** value are all 32 bits long.</span></span> <span data-ttu-id="9430d-112">Однако в 64-разрядной Windows длина адреса и **ulong** не одинакова.</span><span class="sxs-lookup"><span data-stu-id="9430d-112">However, on 64-bit Windows, an address and a **ULONG** are not the same length.</span></span> <span data-ttu-id="9430d-113">Хотя **ulong** остается 32-битным значением, все указатели теперь являются 64-битовыми значениями.</span><span class="sxs-lookup"><span data-stu-id="9430d-113">While a **ULONG** remains a 32-bit value, all pointers are now 64-bit values.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9430d-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9430d-114">In this Section</span></span>

-   [<span data-ttu-id="9430d-115">Общие рекомендации по переносу</span><span class="sxs-lookup"><span data-stu-id="9430d-115">General Porting Guidelines</span></span>](general-porting-guidelines.md)
-   [<span data-ttu-id="9430d-116">Сохранение 64-разрядного значения</span><span class="sxs-lookup"><span data-stu-id="9430d-116">Storing a 64-bit Value</span></span>](storing-a-64-bit-value.md)
-   [<span data-ttu-id="9430d-117">Распространенные ошибки компилятора</span><span class="sxs-lookup"><span data-stu-id="9430d-117">Common Compiler Errors</span></span>](common-compiler-errors.md)
-   [<span data-ttu-id="9430d-118">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="9430d-118">Additional Considerations</span></span>](additional-considerations.md)

 

 




