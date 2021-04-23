---
title: Строки (RPC)
description: Три типа строк и удаленный вызов процедур (RPC).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338708"
---
# <a name="strings-rpc"></a><span data-ttu-id="68fb1-103">Строки (RPC)</span><span class="sxs-lookup"><span data-stu-id="68fb1-103">Strings (RPC)</span></span>

<span data-ttu-id="68fb1-104">Существует три типа строк, обозначенных следующими завершающими подстроками в символе формата.</span><span class="sxs-lookup"><span data-stu-id="68fb1-104">There are three strings types denoted by the following ending sub-strings in the format character.</span></span>



| <span data-ttu-id="68fb1-105">Тип</span><span class="sxs-lookup"><span data-stu-id="68fb1-105">Type</span></span>                  | <span data-ttu-id="68fb1-106">Substring</span><span class="sxs-lookup"><span data-stu-id="68fb1-106">Substring</span></span> |
|-----------------------|-----------|
| <span data-ttu-id="68fb1-107">Строка символов</span><span class="sxs-lookup"><span data-stu-id="68fb1-107">Character string</span></span>      | <span data-ttu-id="68fb1-108">CSTRING</span><span class="sxs-lookup"><span data-stu-id="68fb1-108">CSTRING</span></span>   |
| <span data-ttu-id="68fb1-109">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="68fb1-109">Wide character string</span></span> | <span data-ttu-id="68fb1-110">WSTRING</span><span class="sxs-lookup"><span data-stu-id="68fb1-110">WSTRING</span></span>   |
| <span data-ttu-id="68fb1-111">Структура, доступная для строк</span><span class="sxs-lookup"><span data-stu-id="68fb1-111">String-able structure</span></span> | <span data-ttu-id="68fb1-112">сстринг</span><span class="sxs-lookup"><span data-stu-id="68fb1-112">SSTRING</span></span>   |



 

### <a name="nonconformant-strings"></a><span data-ttu-id="68fb1-113">Несоответствующие строки</span><span class="sxs-lookup"><span data-stu-id="68fb1-113">Nonconformant Strings</span></span>

<span data-ttu-id="68fb1-114">Примером несогласованной строки является **\[ строка \]** в массиве фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="68fb1-114">An example of nonconformant string is a **\[string\]** on a fixed-size array.</span></span>

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a><span data-ttu-id="68fb1-115">Согласованные строки</span><span class="sxs-lookup"><span data-stu-id="68fb1-115">Conformant Strings</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

<span data-ttu-id="68fb1-116">–или–</span><span class="sxs-lookup"><span data-stu-id="68fb1-116">–or–</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

<span data-ttu-id="68fb1-117">Первый формат описывает общие строки, например **\[ строковый \]** аргумент Char \* .</span><span class="sxs-lookup"><span data-stu-id="68fb1-117">The first format describes common strings, like a **\[string\]** char \* argument.</span></span> <span data-ttu-id="68fb1-118">Строка с указанием размера имеет Последнее описание.</span><span class="sxs-lookup"><span data-stu-id="68fb1-118">A sized conformant string has the latter description.</span></span>

<span data-ttu-id="68fb1-119">\_Описание соответствия<> является дескриптором корреляции и имеет 4 или 6 байт в зависимости от того, используется ли [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="68fb1-119">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

### <a name="structure-strings"></a><span data-ttu-id="68fb1-120">Строки структуры</span><span class="sxs-lookup"><span data-stu-id="68fb1-120">Structure Strings</span></span>

<span data-ttu-id="68fb1-121">Ниже приведена несоответствующая структура строк.</span><span class="sxs-lookup"><span data-stu-id="68fb1-121">The following is a nonconformant string-able structure:</span></span>

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

<span data-ttu-id="68fb1-122">Согласованная структура, поддерживающая строки:</span><span class="sxs-lookup"><span data-stu-id="68fb1-122">Conformant string-able structure:</span></span>

``` syntax
FC_C_SSTRING 
element_size<1>
```

<span data-ttu-id="68fb1-123">ни</span><span class="sxs-lookup"><span data-stu-id="68fb1-123">–or –</span></span>

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

<span data-ttu-id="68fb1-124">Последнее описание предназначено для структуры, которая может иметь размер строк.</span><span class="sxs-lookup"><span data-stu-id="68fb1-124">The latter description is for a sized string-able structure.</span></span>

 

 