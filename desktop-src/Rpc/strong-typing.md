---
title: Строгая типизация
description: C — это слабо типизированный язык, т. е. компилятор позволяет выполнять такие операции, как назначение и сравнение переменных различных типов.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- Удаленный вызов процедур RPC, описание, ввод данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986818"
---
# <a name="strong-typing"></a><span data-ttu-id="bba83-104">Строгая типизация</span><span class="sxs-lookup"><span data-stu-id="bba83-104">Strong Typing</span></span>

<span data-ttu-id="bba83-105">C — это слабо типизированный язык, т. е. компилятор позволяет выполнять такие операции, как назначение и сравнение переменных различных типов.</span><span class="sxs-lookup"><span data-stu-id="bba83-105">C is a weakly typed language, that is, the compiler allows operations such as assignment and comparison among variables of different types.</span></span> <span data-ttu-id="bba83-106">Например, C позволяет приведение значения переменной к другому типу.</span><span class="sxs-lookup"><span data-stu-id="bba83-106">For example, C allows the value of a variable to be cast to another type.</span></span> <span data-ttu-id="bba83-107">Возможность использования переменных различных типов в одном выражении повышает гибкость и эффективность.</span><span class="sxs-lookup"><span data-stu-id="bba83-107">The ability to use variables of different types in the same expression promotes flexibility as well as efficiency.</span></span>

<span data-ttu-id="bba83-108">Строго типизированный язык накладывает ограничения на операции между переменными различных типов.</span><span class="sxs-lookup"><span data-stu-id="bba83-108">A strongly typed language imposes restrictions on operations among variables of different types.</span></span> <span data-ttu-id="bba83-109">В таких случаях компилятор выдает ошибку, запрещающую операцию.</span><span class="sxs-lookup"><span data-stu-id="bba83-109">In those cases, the compiler issues an error prohibiting the operation.</span></span> <span data-ttu-id="bba83-110">Эти строгие рекомендации относительно типов данных предназначены для предотвращения потенциальных ошибок.</span><span class="sxs-lookup"><span data-stu-id="bba83-110">These strict guidelines regarding data types are designed to avoid potential errors.</span></span>

<span data-ttu-id="bba83-111">Сложность использования нестрого типизированного языка, такого как C для удаленных вызовов процедур, заключается в том, что распределенные приложения могут работать на нескольких разных компьютерах с разными компиляторами C и разными архитектурами.</span><span class="sxs-lookup"><span data-stu-id="bba83-111">The difficulty with using a weakly typed language such as C for remote procedure calls is that distributed applications can run on several different computers with different C compilers and different architectures.</span></span> <span data-ttu-id="bba83-112">Если приложение выполняется только на одном компьютере, не нужно думать о внутреннем формате данных, так как данные обрабатываются единообразно.</span><span class="sxs-lookup"><span data-stu-id="bba83-112">When an application runs on only one computer, you don't have to be concerned with the internal data format because the data is handled in a consistent manner.</span></span> <span data-ttu-id="bba83-113">Однако в распределенных вычислительных средах разные компьютеры могут использовать разные определения для их базовых типов данных.</span><span class="sxs-lookup"><span data-stu-id="bba83-113">However, in a distributed computing environment, different computers can use different definitions for their base data types.</span></span> <span data-ttu-id="bba83-114">Например, некоторые компьютеры определяют тип **int** , поэтому его внутреннее представление — 16 бит, в то время как другие компьютеры используют 32 бит.</span><span class="sxs-lookup"><span data-stu-id="bba83-114">For example, some computers define the **int** type, so its internal representation is 16 bits, while other computers use 32 bits.</span></span> <span data-ttu-id="bba83-115">Одна компьютерная архитектура, называемая «прямым порядком байтов», назначает минимальный значащий байт данных минимальному адресу в памяти и наиболее значимому байту для самого высокого адреса.</span><span class="sxs-lookup"><span data-stu-id="bba83-115">One computer architecture, known as "little endian," assigns the least significant byte of data to the lowest memory address and the most significant byte to the highest address.</span></span> <span data-ttu-id="bba83-116">Другая архитектура, называемая "Big endian", назначает самый значащий байт наибольшему адресу памяти, связанному с этими данными.</span><span class="sxs-lookup"><span data-stu-id="bba83-116">Another architecture, known as "big endian," assigns the least significant byte to the highest memory address associated with that data.</span></span>

<span data-ttu-id="bba83-117">Для удаленных вызовов процедур требуется более полный контроль над типами параметров.</span><span class="sxs-lookup"><span data-stu-id="bba83-117">Remote procedure calls require strict control over parameter types.</span></span> <span data-ttu-id="bba83-118">Для обработки передачи и преобразования данных по сети MIDL строго применяет ограничения типа данных, передаваемых по сети.</span><span class="sxs-lookup"><span data-stu-id="bba83-118">To handle data transmission and conversion over the network, MIDL strictly enforces type restrictions for data transferred over the network.</span></span> <span data-ttu-id="bba83-119">По этой причине MIDL включает набор четко определенных [базовых типов](base-types.md).</span><span class="sxs-lookup"><span data-stu-id="bba83-119">For this reason, MIDL includes a set of well-defined [base types](base-types.md).</span></span> <span data-ttu-id="bba83-120">MIDL обеспечивает строгую типизацию, предписывания использование ключевых слов, которые однозначно определяют размер и тип данных.</span><span class="sxs-lookup"><span data-stu-id="bba83-120">MIDL enforces strong typing by mandating the use of keywords that unambiguously define the size and type of data.</span></span> <span data-ttu-id="bba83-121">Наиболее видимым результатом строгой типизации является то, что MIDL не позволяет использовать переменные **типа \* void**.</span><span class="sxs-lookup"><span data-stu-id="bba83-121">The most visible effect of strong typing is that MIDL does not allow variables of the type **void \***.</span></span>

<span data-ttu-id="bba83-122">В следующих разделах в этом разделе обсуждаются функции языка MIDL, обеспечивающие строгую типизацию данных:</span><span class="sxs-lookup"><span data-stu-id="bba83-122">In the following topics, this section discusses the MIDL language features that enforce strong data typing:</span></span>

-   [<span data-ttu-id="bba83-123">Базовые типы</span><span class="sxs-lookup"><span data-stu-id="bba83-123">Base Types</span></span>](base-types.md)
-   [<span data-ttu-id="bba83-124">Подписанные и неподписанные типы</span><span class="sxs-lookup"><span data-stu-id="bba83-124">Signed and Unsigned Types</span></span>](signed-and-unsigned-types.md)
-   [<span data-ttu-id="bba83-125">Типы расширенных символов</span><span class="sxs-lookup"><span data-stu-id="bba83-125">Wide-Character Types</span></span>](wide-character-types.md)
-   [<span data-ttu-id="bba83-126">Структуры</span><span class="sxs-lookup"><span data-stu-id="bba83-126">Structures</span></span>](structures.md)
-   [<span data-ttu-id="bba83-127">Объединения</span><span class="sxs-lookup"><span data-stu-id="bba83-127">Unions</span></span>](unions.md)
-   [<span data-ttu-id="bba83-128">Перечислимые типы</span><span class="sxs-lookup"><span data-stu-id="bba83-128">Enumerated Types</span></span>](enumerated-types.md)
-   [<span data-ttu-id="bba83-129">Массивы</span><span class="sxs-lookup"><span data-stu-id="bba83-129">Arrays</span></span>](arrays.md)
-   [<span data-ttu-id="bba83-130">Атрибуты функций</span><span class="sxs-lookup"><span data-stu-id="bba83-130">Function Attributes</span></span>](function-attributes.md)
-   [<span data-ttu-id="bba83-131">Атрибуты поля</span><span class="sxs-lookup"><span data-stu-id="bba83-131">Field Attributes</span></span>](field-attributes.md)
-   [<span data-ttu-id="bba83-132">Три типа указателей</span><span class="sxs-lookup"><span data-stu-id="bba83-132">Three Pointer Types</span></span>](three-pointer-types.md)
-   [<span data-ttu-id="bba83-133">Атрибуты типа</span><span class="sxs-lookup"><span data-stu-id="bba83-133">Type Attributes</span></span>](type-attributes.md)

 

 




