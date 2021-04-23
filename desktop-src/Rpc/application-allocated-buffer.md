---
title: Буфер Application-Allocated
description: Атрибут ACF \ число байтов \_ \ направляет заглушки использовать предварительно выделенный буфер, который не выделяется или не освобождается подпрограммыми поддержки клиентов.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488120"
---
# <a name="application-allocated-buffer"></a><span data-ttu-id="da618-103">Буфер Application-Allocated</span><span class="sxs-lookup"><span data-stu-id="da618-103">Application-Allocated Buffer</span></span>

<span data-ttu-id="da618-104">\[ [**\_ Счетчик байтов**](/windows/desktop/Midl/byte-count) атрибута ACF \] указывает заглушкам использовать предварительно выделенный буфер, который не выделяется и не освобождается подпрограммыми поддержки клиентов.</span><span class="sxs-lookup"><span data-stu-id="da618-104">The ACF attribute \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] directs the stubs to use a preallocated buffer that is not allocated or freed by the client support routines.</span></span> <span data-ttu-id="da618-105">Атрибут \[ **\_ количества байтов** \] применяется к указателю или параметру массива, который указывает на буфер.</span><span class="sxs-lookup"><span data-stu-id="da618-105">The \[**byte\_count**\] attribute is applied to a pointer or array parameter that points to the buffer.</span></span> <span data-ttu-id="da618-106">Для этого требуется параметр, указывающий размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="da618-106">It requires a parameter that specifies the buffer size in bytes.</span></span>

<span data-ttu-id="da618-107">Область памяти, выделенная клиентом, может содержать сложные структуры данных с несколькими указателями.</span><span class="sxs-lookup"><span data-stu-id="da618-107">The client-allocated memory area can contain complex data structures with multiple pointers.</span></span> <span data-ttu-id="da618-108">Поскольку область памяти является непрерывной, приложению не нужно делать несколько вызовов для высвобождения каждого указателя и структуры по отдельности.</span><span class="sxs-lookup"><span data-stu-id="da618-108">Because the memory area is contiguous, the application does not have to make several calls to free each pointer and structure individually.</span></span> <span data-ttu-id="da618-109">Как и при использовании \[ атрибута [**allocate (все \_ узлы)**](/windows/desktop/Midl/allocate) \] , область памяти может быть выделена или освобождена с помощью одного вызова подпрограммы выделения памяти или бесплатной подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="da618-109">As when using the \[[**allocate(all\_nodes)**](/windows/desktop/Midl/allocate)\] attribute, the memory area can be allocated or freed with one call to the memory-allocation routine or the free routine.</span></span> <span data-ttu-id="da618-110">Однако, в отличие от атрибута \[ **allocate (все \_ узлы)** \] , параметр buffer не управляется клиентской заглушкой, а клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="da618-110">However, unlike using the \[**allocate(all\_nodes)**\] attribute, the buffer parameter is not managed by the client stub but by the client application.</span></span>

<span data-ttu-id="da618-111">Буфер должен быть \[ [](/windows/desktop/Midl/out-idl) \] параметром только для исходящих байтов, а длина буфера в байтах должна быть \[ [](/windows/desktop/Midl/in) \] параметром только для чтения.</span><span class="sxs-lookup"><span data-stu-id="da618-111">The buffer must be an \[[**out**](/windows/desktop/Midl/out-idl)\]-only parameter and the buffer length in bytes must be an \[[**in**](/windows/desktop/Midl/in)\]-only parameter.</span></span> <span data-ttu-id="da618-112">Атрибут \[ [**\_ количества байтов**](/windows/desktop/Midl/byte-count) \] может применяться только к типам указателей.</span><span class="sxs-lookup"><span data-stu-id="da618-112">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute can only be applied to pointer types.</span></span> <span data-ttu-id="da618-113">Атрибут \[ **ACF \_ Count** \] -Byte является РАСШИРЕНИЕМ Майкрософт для устройства DCE IDL и, таким образом, недоступен при компиляции с помощью параметра MIDL [**/ОСФ**](/windows/desktop/Midl/-osf) .</span><span class="sxs-lookup"><span data-stu-id="da618-113">The \[**byte\_count**\] ACF attribute is a Microsoft extension to DCE IDL and, as such, is not available if you compile using the MIDL [**/osf**](/windows/desktop/Midl/-osf) switch.</span></span>

<span data-ttu-id="da618-114">В следующем примере параметр *Прут* использует число байт:</span><span class="sxs-lookup"><span data-stu-id="da618-114">In the following example, the parameter *pRoot* uses byte count:</span></span>

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

<span data-ttu-id="da618-115">Атрибут \[ [**\_ количества БАЙТОВ**](/windows/desktop/Midl/byte-count) \] отображается в ACF как:</span><span class="sxs-lookup"><span data-stu-id="da618-115">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute appears in the ACF as:</span></span>

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

<span data-ttu-id="da618-116">Заглушка клиента, созданная из этих файлов IDL и ACF, не выделяет и не освобождает память для этого буфера.</span><span class="sxs-lookup"><span data-stu-id="da618-116">The client stub generated from these IDL and ACF files does not allocate or free the memory for this buffer.</span></span> <span data-ttu-id="da618-117">Заглушка сервера выделяет буфер и освобождает его в одном вызове, используя предоставленный параметр размера.</span><span class="sxs-lookup"><span data-stu-id="da618-117">The server stub allocates and frees the buffer in a single call using the provided size parameter.</span></span> <span data-ttu-id="da618-118">Если данные слишком велики для указанного размера буфера, возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="da618-118">If the data is too large for the specified buffer size, an exception is raised.</span></span>

 

 