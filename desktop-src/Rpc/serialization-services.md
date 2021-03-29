---
title: Службы сериализации
description: Microsoft RPC поддерживает два метода кодирования и декодирования данных, называемые сериализацией данных.
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- Удаленный вызов процедур RPC, описание, сериализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc5b877e29f7a7f6cd102663017f64bebfdff04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779079"
---
# <a name="serialization-services"></a><span data-ttu-id="662ee-104">Службы сериализации</span><span class="sxs-lookup"><span data-stu-id="662ee-104">Serialization Services</span></span>

<span data-ttu-id="662ee-105">Microsoft RPC поддерживает два метода кодирования и декодирования данных, называемые *сериализацией данных*.</span><span class="sxs-lookup"><span data-stu-id="662ee-105">Microsoft RPC supports two methods for encoding and decoding data, collectively called *serializing data*.</span></span> <span data-ttu-id="662ee-106">Сериализация означает, что данные маршалируются в и расмаршалируются из буферов, которыми вы управляете.</span><span class="sxs-lookup"><span data-stu-id="662ee-106">Serialization means that the data is marshaled to and unmarshaled from buffers that you control.</span></span> <span data-ttu-id="662ee-107">Это отличается от традиционного использования RPC, в котором заглушки и библиотека времени выполнения RPC полностью контролируют буферы упаковки, а сам процесс является прозрачным.</span><span class="sxs-lookup"><span data-stu-id="662ee-107">This differs from the traditional usage of RPC, in which the stubs and the RPC run-time library have full control of the marshaling buffers, and the process is transparent.</span></span> <span data-ttu-id="662ee-108">Буфер можно использовать для хранения на постоянных носителях, шифрования и т. д.</span><span class="sxs-lookup"><span data-stu-id="662ee-108">You can use the buffer for storage on permanent media, encryption, and so on.</span></span> <span data-ttu-id="662ee-109">При кодировании данных заглушки RPC маршалируются данные в буфер и передают буфер.</span><span class="sxs-lookup"><span data-stu-id="662ee-109">When you encode data, the RPC stubs marshal the data to a buffer and pass the buffer to you.</span></span> <span data-ttu-id="662ee-110">При декодировании данных вы предоставляете буфер для упаковки с данными, а данные демаршалируются из буфера в память.</span><span class="sxs-lookup"><span data-stu-id="662ee-110">When you decode data, you supply a marshaling buffer with data in it, and the data is unmarshaled from the buffer to memory.</span></span> <span data-ttu-id="662ee-111">Можно выполнить сериализацию по процедуре или типу.</span><span class="sxs-lookup"><span data-stu-id="662ee-111">You can serialize on a procedure or type basis.</span></span>

> [!Note]  
> <span data-ttu-id="662ee-112">Термин « *раскрывающийся* список» обычно используется разработчиками для описания сериализации.</span><span class="sxs-lookup"><span data-stu-id="662ee-112">The term *pickling* is commonly used among developers to describe serialization.</span></span> <span data-ttu-id="662ee-113">На самом деле Windows SDK образцы содержат каталог *с именем,* который сохраняет образцы программ RPC Serialization.</span><span class="sxs-lookup"><span data-stu-id="662ee-113">In fact, the Windows SDK samples contains a directory called *pickle* that preserves the RPC serialization sample programs.</span></span>

 

<span data-ttu-id="662ee-114">Сериализация использует механизмы RPC для упаковки и распаковки данных в других целях.</span><span class="sxs-lookup"><span data-stu-id="662ee-114">Serialization leverages the RPC mechanisms for marshaling and unmarshaling data for other purposes.</span></span> <span data-ttu-id="662ee-115">Например, вместо использования нескольких операций ввода-вывода для сериализации группы объектов в поток приложение может оптимизировать производительность путем сериализации нескольких объектов разных типов в буфер и последующей записи всего буфера в одну операцию.</span><span class="sxs-lookup"><span data-stu-id="662ee-115">For example, instead of using several I/O operations to serialize a group of objects to a stream, an application can optimize performance by serializing several objects of different types into a buffer and then writing the entire buffer in a single operation.</span></span> <span data-ttu-id="662ee-116">Функции, управляющие дескрипторами сериализации, не зависят от типа используемой сериализации.</span><span class="sxs-lookup"><span data-stu-id="662ee-116">The functions that manipulate serialization handles are independent of the type of serialization you are using.</span></span>

<span data-ttu-id="662ee-117">Другой пример: Если необходимо использовать механизм сетевого транспорта, помимо RPC, например сокеты Microsoft Windows (Winsock).</span><span class="sxs-lookup"><span data-stu-id="662ee-117">As another example, if you need to use a network transport mechanism besides RPC, such as Microsoft Windows Sockets (Winsock).</span></span> <span data-ttu-id="662ee-118">Благодаря сериализации RPC программа может вызывать функции, которые маршалируются данные в буферы, а затем передавать эти данные с помощью Winsock.</span><span class="sxs-lookup"><span data-stu-id="662ee-118">With RPC serialization, your program can make calls to functions that marshal your data into buffers and then transmit this data using Winsock.</span></span> <span data-ttu-id="662ee-119">Когда приложение получает данные, оно может использовать механизм сериализации RPC для распаковки данных из буферов, заполненных подпрограммыми Winsock.</span><span class="sxs-lookup"><span data-stu-id="662ee-119">When your application receives data, it can use the RPC serialization mechanism to unmarshal data from buffers filled by the Winsock routines.</span></span> <span data-ttu-id="662ee-120">Это дает вам множество преимуществ приложений в стиле RPC и в то же время позволяет использовать механизмы транспорта, отличные от RPC.</span><span class="sxs-lookup"><span data-stu-id="662ee-120">This provides you with many of the advantages of RPC-style applications, and at the same time, it enables you to use non-RPC transport mechanisms.</span></span>

<span data-ttu-id="662ee-121">Можно также использовать сериализацию для целей, не связанных с сетевыми связями.</span><span class="sxs-lookup"><span data-stu-id="662ee-121">You can also use serialization for purposes unrelated to network communications.</span></span> <span data-ttu-id="662ee-122">Например, после использования функций кодирования RPC для маршалирования данных в буфер можно сохранить их в файл для использования другим приложением.</span><span class="sxs-lookup"><span data-stu-id="662ee-122">For example, once you use the RPC encoding functions to marshal data to a buffer, you can store it in a file for use by another application.</span></span> <span data-ttu-id="662ee-123">Его также можно зашифровать.</span><span class="sxs-lookup"><span data-stu-id="662ee-123">You can also encrypt it.</span></span> <span data-ttu-id="662ee-124">Его можно даже использовать для хранения независимого от оборудования и операционной системы представления данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="662ee-124">You can even use it to store a hardware- and operating system-independent representation of data in a database.</span></span>

<span data-ttu-id="662ee-125">В следующих разделах представлено обсуждение служб сериализации, поддерживаемых Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="662ee-125">The following topics present a discussion of the serialization services that Microsoft RPC supports:</span></span>

-   [<span data-ttu-id="662ee-126">Использование служб сериализации</span><span class="sxs-lookup"><span data-stu-id="662ee-126">Using Serialization Services</span></span>](using-serialization-services.md)
-   [<span data-ttu-id="662ee-127">Сериализация процедур</span><span class="sxs-lookup"><span data-stu-id="662ee-127">Procedure Serialization</span></span>](procedure-serialization.md)
-   [<span data-ttu-id="662ee-128">Сериализация типов</span><span class="sxs-lookup"><span data-stu-id="662ee-128">Type Serialization</span></span>](type-serialization.md)
-   [<span data-ttu-id="662ee-129">Дескрипторы сериализации</span><span class="sxs-lookup"><span data-stu-id="662ee-129">Serialization Handles</span></span>](serialization-handles.md)

 

 




