---
title: " в, String и out, строковый прототип"
description: 'В следующем прототипе функции используются два параметра: "\ in", "String \" и "\ out", "String \".'
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987825"
---
# <a name="in-string-and-out-string-prototype"></a><span data-ttu-id="6f1af-103">\[в, String \] и \[ out, строковый \] прототип</span><span class="sxs-lookup"><span data-stu-id="6f1af-103">\[in, string\] and \[out, string\] Prototype</span></span>

<span data-ttu-id="6f1af-104">В следующем прототипе функции используются два параметра: \[ [**в**](/windows/desktop/Midl/in), [**строковый**](/windows/desktop/Midl/string) \] параметр и \[ параметр [**out**](/windows/desktop/Midl/out-idl), **строковый** \] .</span><span class="sxs-lookup"><span data-stu-id="6f1af-104">The following function prototype uses two parameters: an \[[**in**](/windows/desktop/Midl/in), [**string**](/windows/desktop/Midl/string)\] parameter and an \[[**out**](/windows/desktop/Midl/out-idl), **string**\] parameter.</span></span>

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

<span data-ttu-id="6f1af-105">Первый параметр доступен только \[ [**в**](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="6f1af-105">The first parameter is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="6f1af-106">Эта входная строка передается только с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="6f1af-106">This input string is only transmitted from the client to the server.</span></span> <span data-ttu-id="6f1af-107">Сервер использует его в качестве основания для дальнейшей обработки.</span><span class="sxs-lookup"><span data-stu-id="6f1af-107">The server uses it as the basis for further processing.</span></span> <span data-ttu-id="6f1af-108">Строка не изменяется и не требуется повторно клиентом, поэтому она не должна возвращаться клиенту.</span><span class="sxs-lookup"><span data-stu-id="6f1af-108">The string is not modified and is not required again by the client, so it does not have to be returned to the client.</span></span>

<span data-ttu-id="6f1af-109">Второй параметр, представляющий ответ врача, является \[ только [**выходом**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="6f1af-109">The second parameter, representing the doctor's response, is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="6f1af-110">Эта строка ответа передается клиенту только с сервера.</span><span class="sxs-lookup"><span data-stu-id="6f1af-110">This response string is only transmitted from the server to the client.</span></span> <span data-ttu-id="6f1af-111">Размер выделения предоставляется таким образом, чтобы заглушки сервера могли выделить память для него.</span><span class="sxs-lookup"><span data-stu-id="6f1af-111">The allocation size is provided so that the server stubs can allocate memory for it.</span></span> <span data-ttu-id="6f1af-112">Так как *псзаутпут* является \[ [**ссылочным**](/windows/desktop/Midl/ref) \] указателем, клиент должен иметь достаточно памяти, выделенной для строки перед вызовом.</span><span class="sxs-lookup"><span data-stu-id="6f1af-112">Since *pszOutput* is a \[[**ref**](/windows/desktop/Midl/ref)\] pointer, the client must have sufficient memory allocated for the string before the call.</span></span> <span data-ttu-id="6f1af-113">Строка ответа записывается в эту область памяти при возврате удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="6f1af-113">The response string is written into this area of memory when the remote procedure returns.</span></span>

 

 