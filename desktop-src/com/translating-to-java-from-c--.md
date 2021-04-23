---
title: Перевод на Java из C++
description: Используя язык программирования C++, разработчики могут напрямую обращаться к памяти, в которой хранится определенная переменная. Указатели памяти обеспечивают прямой доступ. В Java указатели обрабатываются самостоятельно.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410663"
---
# <a name="translating-to-java-from-c"></a><span data-ttu-id="6ab93-105">Перевод на Java из C++</span><span class="sxs-lookup"><span data-stu-id="6ab93-105">Translating to Java from C++</span></span>

<span data-ttu-id="6ab93-106">Используя язык программирования C++, разработчики могут напрямую обращаться к памяти, в которой хранится определенная переменная.</span><span class="sxs-lookup"><span data-stu-id="6ab93-106">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="6ab93-107">Указатели памяти обеспечивают прямой доступ.</span><span class="sxs-lookup"><span data-stu-id="6ab93-107">Memory pointers provide this direct access.</span></span> <span data-ttu-id="6ab93-108">В Java указатели обрабатываются самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="6ab93-108">In Java, pointers are handled for you.</span></span>

<span data-ttu-id="6ab93-109">В составных типах данных Java, **struct**, **Union** и **typedef** обрабатываются исключительно с помощью классов.</span><span class="sxs-lookup"><span data-stu-id="6ab93-109">In Java, **struct**, **union**, and **typedef** composite data types are handled exclusively through the use of classes.</span></span> <span data-ttu-id="6ab93-110">Например, тип данных **Variant** C++ соответствует **com. MS. com. Variant** в Java.</span><span class="sxs-lookup"><span data-stu-id="6ab93-110">For example, the C++ **VARIANT** data type maps to **com.ms.com.Variant** in Java.</span></span>

<span data-ttu-id="6ab93-111">В C++ строки представляют собой массив символов.</span><span class="sxs-lookup"><span data-stu-id="6ab93-111">In C++, strings are an array of characters.</span></span> <span data-ttu-id="6ab93-112">В Java строки являются объектами.</span><span class="sxs-lookup"><span data-stu-id="6ab93-112">In Java, strings are objects.</span></span> <span data-ttu-id="6ab93-113">Методы, действующие в строках, обрабатывают строку как полный объект.</span><span class="sxs-lookup"><span data-stu-id="6ab93-113">Methods that act on strings treat the string as a complete object.</span></span>

<span data-ttu-id="6ab93-114">Методы COM возвращают значение, известное как **HRESULT**, который представляет собой 32-разрядный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="6ab93-114">COM methods return a value known as a **HRESULT**, which is a 32-bit error code.</span></span> <span data-ttu-id="6ab93-115">Поддержка Java для Microsoft Internet Explorer определяет класс **com. MS. com. ComException**, который заключает в оболочку код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ab93-115">The Java support for Microsoft Internet Explorer defines a class, **com.ms.com.ComException**, which wraps the **HRESULT** error code.</span></span>

<span data-ttu-id="6ab93-116">Java не поддерживает неподписанные типы данных, за исключением **char**, которое представляет собой 16-битовое целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="6ab93-116">Java does not support unsigned data types except for **char**, which is a 16-bit unsigned integer.</span></span> <span data-ttu-id="6ab93-117">Методы, которые принимают или возвращают другие неподписанные типы данных, не могут использоваться из Java.</span><span class="sxs-lookup"><span data-stu-id="6ab93-117">Methods that accept or return other unsigned data types cannot be used from Java.</span></span>

<span data-ttu-id="6ab93-118">Java не поддерживает многомерные массивы.</span><span class="sxs-lookup"><span data-stu-id="6ab93-118">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="6ab93-119">Методы, которые принимают или возвращают многомерные массивы, недоступны в Java.</span><span class="sxs-lookup"><span data-stu-id="6ab93-119">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="6ab93-120">Логические значения в Java не могут быть приведены к 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="6ab93-120">Boolean values in Java cannot be cast to 0 and 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ab93-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6ab93-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab93-122">Перевод на Java</span><span class="sxs-lookup"><span data-stu-id="6ab93-122">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




