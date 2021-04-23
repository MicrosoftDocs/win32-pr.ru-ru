---
title: Top-Level и внедренные указатели
description: Чтобы понять, как указатели и связанные с ними элементы данных выделяются в Microsoft RPC, необходимо различать указатели верхнего уровня и внедренные указатели.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487000"
---
# <a name="top-level-and-embedded-pointers"></a><span data-ttu-id="9661a-103">Top-Level и внедренные указатели</span><span class="sxs-lookup"><span data-stu-id="9661a-103">Top-Level and Embedded Pointers</span></span>

<span data-ttu-id="9661a-104">Чтобы понять, как указатели и связанные с ними элементы данных выделяются в Microsoft RPC, необходимо различать *указатели верхнего уровня* и *внедренные указатели*.</span><span class="sxs-lookup"><span data-stu-id="9661a-104">To understand how pointers and their associated data elements are allocated in Microsoft RPC, you have to differentiate between *top-level pointers* and *embedded pointers*.</span></span> <span data-ttu-id="9661a-105">Также полезно ссылаться на набор всех указателей, не являющихся указателями верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="9661a-105">It is also useful to refer to the set of all pointers that are not top-level pointers.</span></span>

<span data-ttu-id="9661a-106">*Указатели верхнего уровня* — это те, которые указаны в качестве имен параметров в прототипах функций.</span><span class="sxs-lookup"><span data-stu-id="9661a-106">*Top-level pointers* are those that are specified as the names of parameters in function prototypes.</span></span> <span data-ttu-id="9661a-107">Указатели верхнего уровня и их референтс всегда выделяются на сервере.</span><span class="sxs-lookup"><span data-stu-id="9661a-107">Top-level pointers and their referents are always allocated on the server.</span></span>

<span data-ttu-id="9661a-108">*Внедренные указатели* — это указатели, которые внедряются в структуры данных, такие как массивы, структуры и объединения.</span><span class="sxs-lookup"><span data-stu-id="9661a-108">*Embedded pointers* are pointers that are embedded in data structures such as arrays, structures, and unions.</span></span> <span data-ttu-id="9661a-109">Если внедренные указатели записывают выходные данные в буфер и имеют значение null, серверное приложение может изменить их значения на отличные от NULL.</span><span class="sxs-lookup"><span data-stu-id="9661a-109">When embedded pointers only write output to a buffer and are null on input, the server application can change their values to non-null.</span></span> <span data-ttu-id="9661a-110">В этом случае клиентские заглушки выделяют новую память для этих данных.</span><span class="sxs-lookup"><span data-stu-id="9661a-110">In this case, the client stubs allocate new memory for this data.</span></span>

<span data-ttu-id="9661a-111">Если встроенный указатель не имеет значение NULL на клиенте перед вызовом, заглушки не распределяют память на клиенте при возврате.</span><span class="sxs-lookup"><span data-stu-id="9661a-111">If the embedded pointer is not null on the client before the call, the stubs do not allocate memory on the client on return.</span></span> <span data-ttu-id="9661a-112">Вместо этого заглушки пытаются записать память, связанную с внедренным указателем, в существующую память на клиенте, связанную с этим указателем, перезаписывая данные уже там.</span><span class="sxs-lookup"><span data-stu-id="9661a-112">Instead, the stubs attempt to write the memory associated with the embedded pointer into the existing memory on the client associated with that pointer, overwriting the data already there.</span></span>

> [!Note]  
> <span data-ttu-id="9661a-113">Для данных, считываемых из или записанный в буфер и не указывающих размер буфера, длина выходного значения должна быть меньше или равна длине ввода.</span><span class="sxs-lookup"><span data-stu-id="9661a-113">For data read from or writen to a buffer, and which does not specify the buffer size, output length must be less than or equal to input length.</span></span> <span data-ttu-id="9661a-114">При обнаружении переполнения возникает исключение RPC.</span><span class="sxs-lookup"><span data-stu-id="9661a-114">An RPC exception is raised when overflow is detected.</span></span> <span data-ttu-id="9661a-115">Для строковых данных длина вывода определяется путем проверки длины входной строки.</span><span class="sxs-lookup"><span data-stu-id="9661a-115">For string data, output length is determined by checking length of the input string.</span></span> <span data-ttu-id="9661a-116">Поэтому длина выходных строк не может превышать длину входных строк.</span><span class="sxs-lookup"><span data-stu-id="9661a-116">Therefore, output strings cannot exceed length of input strings.</span></span> <span data-ttu-id="9661a-117">Рекомендуется избегать этого, так как следует всегда включать параметр size, чтобы указать размер буфера.</span><span class="sxs-lookup"><span data-stu-id="9661a-117">Best practice guidance is to avoid this by always including a size-specified parameter to indicate size of the buffer.</span></span>

 

<span data-ttu-id="9661a-118">Внедренные указатели только на запись обсуждаются в разделе [сочетание атрибутов указателя и направления](combining-pointer-and-directional-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="9661a-118">Embedded write-only pointers are discussed in [Combining Pointer and Directional Attributes](combining-pointer-and-directional-attributes.md).</span></span>

<span data-ttu-id="9661a-119">Термины « *указатель уровня нонтоп* » ссылаются на все указатели, которые не указаны в качестве имен параметров в прототипе функции, включая внедренные указатели и несколько уровней вложенных указателей.</span><span class="sxs-lookup"><span data-stu-id="9661a-119">The term *nontop-level pointers* refers to all pointers that are not specified as parameter names in the function prototype, including both embedded pointers and multiple levels of nested pointers.</span></span>

 

 




