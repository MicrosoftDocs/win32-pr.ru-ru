---
title: Несколько уровней указателей
description: Использование нескольких уровней указателей в удаленном вызове процедур (RPC).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987727"
---
# <a name="multiple-levels-of-pointers"></a><span data-ttu-id="442fe-103">Несколько уровней указателей</span><span class="sxs-lookup"><span data-stu-id="442fe-103">Multiple Levels of Pointers</span></span>

<span data-ttu-id="442fe-104">При наличии нескольких уровней указателей атрибуты связываются с указателем, ближайшим к имени переменной.</span><span class="sxs-lookup"><span data-stu-id="442fe-104">When there are multiple levels of pointers, the attributes are associated with the pointer closest to the variable name.</span></span> <span data-ttu-id="442fe-105">Клиент по-прежнему отвечает за выделение памяти, связанной с ответом.</span><span class="sxs-lookup"><span data-stu-id="442fe-105">The client is still responsible for allocating any memory associated with the response.</span></span>

<span data-ttu-id="442fe-106">В следующем примере заглушка позволяет вызвать сервер, не зная заранее, сколько данных будет возвращено:</span><span class="sxs-lookup"><span data-stu-id="442fe-106">The following example allows the stub to call the server without knowing in advance how much data will be returned:</span></span>

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

<span data-ttu-id="442fe-107">В этом примере заглушка передает серверу уникальный указатель, который инициализируется сервером в **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="442fe-107">In this example, the stub passes the server a unique pointer, which the server initializes to **NULL**.</span></span> <span data-ttu-id="442fe-108">Затем сервер выделяет блок полос, устанавливает указатель, устанавливает аргумент size и возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="442fe-108">The server then allocates a block of BARs, sets the pointer, sets the size argument and returns.</span></span> <span data-ttu-id="442fe-109">Обратите внимание, что для того, чтобы сервер мог оказывать воздействие на вызывающий объект, необходимо передать \[ \] указатель ссылки на \[ [**уникальный**](/windows/desktop/Midl/unique) \] указатель на данные.</span><span class="sxs-lookup"><span data-stu-id="442fe-109">Note that in order for the server to have an effect on the caller you must pass a \[ref\] pointer to a \[[**unique**](/windows/desktop/Midl/unique)\] pointer to your data.</span></span> <span data-ttu-id="442fe-110">Также обратите внимание, что запятая в \[ [**size \_ имеет значение**](/windows/desktop/Midl/size-is)(, \* псизе) \] , которое указывает, что указатель верхнего уровня не является указателем размера, но указатель нижнего уровня имеет значение.</span><span class="sxs-lookup"><span data-stu-id="442fe-110">Also note the comma in \[[**size\_is**](/windows/desktop/Midl/size-is)( , \*pSize )\], which indicates that the top-level pointer is not a sized pointer, but that the lower-level pointer is.</span></span>

<span data-ttu-id="442fe-111">На стороне клиента заглушка задает \* для Ппбар **значение NULL** перед вызовом удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="442fe-111">On the client side, the stub sets \*ppBar to **NULL** before calling the remote procedure.</span></span> <span data-ttu-id="442fe-112">Затем заглушка выделяет и расмаршалирует массив UTF8 объектов BAR.</span><span class="sxs-lookup"><span data-stu-id="442fe-112">The stub then allocates and unmarshals the arry of BAR objects.</span></span> <span data-ttu-id="442fe-113">Аргумент Size указывает размер блока (и число неупакованных полос).</span><span class="sxs-lookup"><span data-stu-id="442fe-113">The size argument indicates the size of the block (and the number of unmarshaled BARs).</span></span> <span data-ttu-id="442fe-114">Клиент должен освободить возвращенный массив погрешностей, если он больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="442fe-114">The client must free the returned array of BAR objects when it is no longer required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="442fe-115">См. также</span><span class="sxs-lookup"><span data-stu-id="442fe-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="442fe-116">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="442fe-116">**size\_is**</span></span>](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 