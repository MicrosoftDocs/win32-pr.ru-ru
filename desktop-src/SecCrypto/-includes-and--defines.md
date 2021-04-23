---
description: 'Все примеры в документации по пакету SDK для шифрования предполагают наличие следующих \# директив компилятора: include и \# define.'
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#включает и #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9834fd8103b9fd28a01e416bd1df8b03fb7ad680
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684759"
---
# <a name="includes-and-defines"></a><span data-ttu-id="9a094-103">\#включает и \# определяет</span><span class="sxs-lookup"><span data-stu-id="9a094-103">\#includes and \#defines</span></span>

<span data-ttu-id="9a094-104">Все примеры в документации по пакету SDK для шифрования предполагают наличие следующих директив компилятора **\# : include** и **\# define** .</span><span class="sxs-lookup"><span data-stu-id="9a094-104">All of the examples in the Cryptography SDK documentation are assumed to have the following **\#include** and **\#define** compiler directives.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



<span data-ttu-id="9a094-105">Кроме того, константа **\_ Win32 \_ WinNT** должна быть определена соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="9a094-105">Additionally, the **\_WIN32\_WINNT** constant must be appropriately defined.</span></span> <span data-ttu-id="9a094-106">Дополнительные сведения о **\_ Win32 \_ WinNT** см. [в разделе Использование заголовков Windows](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="9a094-106">For more information about **\_WIN32\_WINNT**, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

 

 
