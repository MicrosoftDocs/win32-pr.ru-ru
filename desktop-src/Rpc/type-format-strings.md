---
title: Строки формата типов
description: Форматирование символов обозначают объекты, представляющие собой подсистема доставки ОНД.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068338"
---
# <a name="type-format-strings"></a><span data-ttu-id="4d02a-103">Строки формата типов</span><span class="sxs-lookup"><span data-stu-id="4d02a-103">Type Format Strings</span></span>

<span data-ttu-id="4d02a-104">Форматирование символов обозначают объекты, представляющие собой подсистема доставки ОНД.</span><span class="sxs-lookup"><span data-stu-id="4d02a-104">Format characters denote objects of interest to the NDR engine.</span></span> <span data-ttu-id="4d02a-105">Существует символ формата для каждого базового типа, для различных сложных типов и описания указателей, упаковки, выравнивания и других прочих объектов.</span><span class="sxs-lookup"><span data-stu-id="4d02a-105">There is a format character for each basic type, for various complex types, and for descriptions of pointers, packing, alignment, and other miscellaneous objects.</span></span> <span data-ttu-id="4d02a-106">Для составных типов несколько категорий структур и массивов распознаются на основе их свойств производительности.</span><span class="sxs-lookup"><span data-stu-id="4d02a-106">For compound types, several categories of structures and arrays are recognized based on their performance properties.</span></span> <span data-ttu-id="4d02a-107">Строка формата для каждой категории начинается с токена FC, идентифицирующего определенную строку формата.</span><span class="sxs-lookup"><span data-stu-id="4d02a-107">A format string for each category starts with an FC token identifying the particular format string.</span></span> <span data-ttu-id="4d02a-108">Символы формата для структур и категорий массивов могут совместно использовать in-Names в имени ведущего маркера FC, показанного в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4d02a-108">Format characters for structures and arrays categories may share the in-fixes in the name of the leading FC token shown in the following table.</span></span>



| <span data-ttu-id="4d02a-109">Символ формата</span><span class="sxs-lookup"><span data-stu-id="4d02a-109">Format character</span></span> | <span data-ttu-id="4d02a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4d02a-110">Description</span></span>                                    |
|------------------|------------------------------------------------|
| <span data-ttu-id="4d02a-111">C</span><span class="sxs-lookup"><span data-stu-id="4d02a-111">C</span></span>                | <span data-ttu-id="4d02a-112">Указывает сведения о соотношении соответствия в типе.</span><span class="sxs-lookup"><span data-stu-id="4d02a-112">Indicates conformance information in the type.</span></span> |
| <span data-ttu-id="4d02a-113">V</span><span class="sxs-lookup"><span data-stu-id="4d02a-113">V</span></span>                | <span data-ttu-id="4d02a-114">Указывает сведения о дисперсии в типе.</span><span class="sxs-lookup"><span data-stu-id="4d02a-114">Indicates variance information in the type.</span></span>    |
| <span data-ttu-id="4d02a-115">С</span><span class="sxs-lookup"><span data-stu-id="4d02a-115">P</span></span>                | <span data-ttu-id="4d02a-116">Указывает, что указатели являются частью типа.</span><span class="sxs-lookup"><span data-stu-id="4d02a-116">Indicates pointers are a part of the type.</span></span>     |



 

<span data-ttu-id="4d02a-117">Например, FC \_ кструкт и FC \_ CARRAY определяли согласованную структуру и согласованные дескрипторы массивов соответственно.</span><span class="sxs-lookup"><span data-stu-id="4d02a-117">For example, FC\_CSTRUCT and FC\_CARRAY identify the conformant structure and conformant array descriptors, respectively.</span></span>

<span data-ttu-id="4d02a-118">Ниже приведены символы форматирования со специальными значениями.</span><span class="sxs-lookup"><span data-stu-id="4d02a-118">The following are format characters with special meanings.</span></span>



| <span data-ttu-id="4d02a-119">Символ формата</span><span class="sxs-lookup"><span data-stu-id="4d02a-119">Format character</span></span> | <span data-ttu-id="4d02a-120">Описание</span><span class="sxs-lookup"><span data-stu-id="4d02a-120">Description</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4d02a-121">FC \_ PP</span><span class="sxs-lookup"><span data-stu-id="4d02a-121">FC\_PP</span></span>           | <span data-ttu-id="4d02a-122">Указывает начало раздела описания указателя в структуре или массиве.</span><span class="sxs-lookup"><span data-stu-id="4d02a-122">Indicates the beginning of the pointer description section of a structure or array.</span></span> |



 

<span data-ttu-id="4d02a-123">Строки формата типа NDR RPC более подробно описаны в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="4d02a-123">RPC NDR type format strings are described in more detail in the following topics:</span></span>

-   [<span data-ttu-id="4d02a-124">Простые типы</span><span class="sxs-lookup"><span data-stu-id="4d02a-124">Simple Types</span></span>](simple-types-tfs.md)
-   [<span data-ttu-id="4d02a-125">Указатели</span><span class="sxs-lookup"><span data-stu-id="4d02a-125">Pointers</span></span>](pointers-tfs.md)
-   [<span data-ttu-id="4d02a-126">Массивы</span><span class="sxs-lookup"><span data-stu-id="4d02a-126">Arrays</span></span>](arrays-tfs.md)
-   [<span data-ttu-id="4d02a-127">Строки</span><span class="sxs-lookup"><span data-stu-id="4d02a-127">Strings</span></span>](strings-tfs.md)
-   [<span data-ttu-id="4d02a-128">Дескрипторы корреляции</span><span class="sxs-lookup"><span data-stu-id="4d02a-128">Correlation Descriptors</span></span>](correlation-descriptors-tfs.md)
-   [<span data-ttu-id="4d02a-129">Структуры</span><span class="sxs-lookup"><span data-stu-id="4d02a-129">Structures</span></span>](structures-tfs.md)
-   [<span data-ttu-id="4d02a-130">Макет указателя</span><span class="sxs-lookup"><span data-stu-id="4d02a-130">Pointer Layout</span></span>](pointer-layout-tfs.md)
-   [<span data-ttu-id="4d02a-131">Объединения</span><span class="sxs-lookup"><span data-stu-id="4d02a-131">Unions</span></span>](unions-tfs.md)
-   [<span data-ttu-id="4d02a-132">Передать \_ как и представить \_ как</span><span class="sxs-lookup"><span data-stu-id="4d02a-132">Transmit\_as and Represent\_as</span></span>](transmit-as-and-represent-as-tfs.md)
-   [<span data-ttu-id="4d02a-133">Пользовательская упаковка</span><span class="sxs-lookup"><span data-stu-id="4d02a-133">User-marshal</span></span>](user-marshal-tfs.md)

 

 




