---
title: Пользовательская упаковка
description: Пользовательская упаковка в удаленном вызове процедур (RPC).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888376"
---
# <a name="user-marshal"></a><span data-ttu-id="a2e1a-103">Пользовательская упаковка</span><span class="sxs-lookup"><span data-stu-id="a2e1a-103">User-marshal</span></span>

<span data-ttu-id="a2e1a-104">Пользовательская упаковка имеет строку формата, похожую на \_ "передать как":</span><span class="sxs-lookup"><span data-stu-id="a2e1a-104">User marshal has a format string that is similar to transmit\_as:</span></span>

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

<span data-ttu-id="a2e1a-105">Флаги<1> байт состоят из верхнего флага, а также более низкого выравнивания.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-105">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="a2e1a-106">Верхние 2 бита флага используются для описания того, определен ли тип провода как уникальный указатель, указатель ссылки или отсутствие указателя (он не может быть PTR).</span><span class="sxs-lookup"><span data-stu-id="a2e1a-106">The upper 2 bits of the flag nibble are used to describe whether the wire type is defined as a unique pointer, reference pointer or no pointer (it cannot be a ptr).</span></span> <span data-ttu-id="a2e1a-107">Для установки и получения флагов определены следующие манифесты:</span><span class="sxs-lookup"><span data-stu-id="a2e1a-107">The following manifests have been defined to set/get the flags:</span></span>

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

<span data-ttu-id="a2e1a-108">Выравнивание по пометке в Word обеспечивает выравнивание передачи переданного типа.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-108">The alignment nibble of the flag word keeps the wire alignment of the transmitted type.</span></span>

<span data-ttu-id="a2e1a-109">Четверный \_ индекс<2> является индексом подпрограммы обратного вызова, четверной для пользовательских функций маршалирования.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-109">The quadruple\_index<2> is an index of the callback routine quadruple of the user marshal functions.</span></span> <span data-ttu-id="a2e1a-110">Ниже приведены положения подпрограмм: изменение размера, маршалирование, распаковка и освобождение подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-110">The routine positions are as follow: sizing, marshaling, unmarshaling, and freeing routine.</span></span>

<span data-ttu-id="a2e1a-111">\_ \_ Размер памяти пользовательского типа \_<2> предоставляет размер для конкретного типа пользователя, включая неизвестные типы.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-111">The user\_type\_memory\_size<2> provides a size for the user specific type, including unknown types.</span></span>

<span data-ttu-id="a2e1a-112">\_Размер переданного \_ буфера типа \_<2> равен нулю, если размер изменен, или фактический фиксированный размер.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-112">The transmitted\_type\_buffer\_size<2> is either zero when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="a2e1a-113">Это оптимизация, позволяющая MIDL пропустить обратные вызовы при определении размера буфера, а также при освобождении.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-113">This is an optimization that enables MIDL to skip callbacks when sizing the buffer, and also when freeing.</span></span>

## <a name="range"></a><span data-ttu-id="a2e1a-114">Диапазон</span><span class="sxs-lookup"><span data-stu-id="a2e1a-114">Range</span></span>

<span data-ttu-id="a2e1a-115">\[Проверка диапазона \] предоставляет дополнительные средства для проверки аргументов на уровне NDR.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-115">The \[range\] checking provides additional means for argument validation at the NDR layer.</span></span> <span data-ttu-id="a2e1a-116">\[Дескриптор диапазона \] имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="a2e1a-116">The \[range\] descriptor has the following format:</span></span>

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

<span data-ttu-id="a2e1a-117">Флаги занимают верхнюю часть, а тип — нижнюю посекунду второго байта.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-117">The flags take the upper nibble and the type the lower nibble of the second byte.</span></span> <span data-ttu-id="a2e1a-118">Низкие и высокие значения зависят от типа проверяемой переменной.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-118">The low and high values depend on the type of the variable to be checked.</span></span>

<span data-ttu-id="a2e1a-119">Флаги предназначены для расширения; компилятор установил в качестве значения "ноль" значение 0.</span><span class="sxs-lookup"><span data-stu-id="a2e1a-119">The flags are meant as an expansion vehicle; the compiler has been setting the nibble to zero.</span></span>

 

 




