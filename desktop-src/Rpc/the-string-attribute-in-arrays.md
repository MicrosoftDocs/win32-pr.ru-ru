---
title: Строковый атрибут в массивах
description: Для одномерных массивов символов, массивов двухбайтовых символов и массивов байтов, представляющих текстовые строки, можно использовать атрибут \ String \.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- строка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134238"
---
# <a name="the-string-attribute-in-arrays"></a><span data-ttu-id="3ee38-104">\[Строковый \] атрибут в массивах</span><span class="sxs-lookup"><span data-stu-id="3ee38-104">The \[string\] Attribute in Arrays</span></span>

<span data-ttu-id="3ee38-105">Можно использовать \[ [строковый](/windows/desktop/Midl/string) \] атрибут для одномерных массивов символов, массивов двухбайтовых символов и массивов байтов, представляющих текстовые строки.</span><span class="sxs-lookup"><span data-stu-id="3ee38-105">You can use the \[ [string](/windows/desktop/Midl/string)\] attribute for one-dimensional character arrays, wide-character arrays, and byte arrays that represent text strings.</span></span> <span data-ttu-id="3ee38-106">Если используется атрибут **\[ String \]** , клиентская заглушка использует функции C-Library **strlen** или **встрлен** для подсчета количества символов в строке.</span><span class="sxs-lookup"><span data-stu-id="3ee38-106">If you use the **\[string\]** attribute, the client stub uses the C-library functions **strlen** or **wstrlen** to count the number of characters in the string.</span></span> <span data-ttu-id="3ee38-107">Чтобы избежать возможных несоответствий, MIDL не позволяет использовать атрибут **\[ String \]** одновременно с \[ [первым \_ параметром —](/windows/desktop/Midl/first-is) \] , \[ [Last \_ —](/windows/desktop/Midl/last-is) \] , а \[ [size \_ —](/windows/desktop/Midl/size-is) \] атрибутами.</span><span class="sxs-lookup"><span data-stu-id="3ee38-107">To avoid possible inconsistencies, MIDL does not let you use the **\[string\]** attribute at the same time as the \[ [first\_is](/windows/desktop/Midl/first-is)\], \[ [last\_is](/windows/desktop/Midl/last-is)\], and \[ [size\_is](/windows/desktop/Midl/size-is)\] attributes.</span></span>

<span data-ttu-id="3ee38-108">При использовании строк с завершающим нулем в C необходимо разрешить пространство для нуль-символа в конце строки.</span><span class="sxs-lookup"><span data-stu-id="3ee38-108">With null-terminated strings in C, you must allow space for the null character at the end of the string.</span></span> <span data-ttu-id="3ee38-109">Например, при объявлении строки, которая будет содержать до 80 символов, выделите 81 символов.</span><span class="sxs-lookup"><span data-stu-id="3ee38-109">For example, when declaring a string that will hold up to 80 characters, allocate 81 characters.</span></span> <span data-ttu-id="3ee38-110">В следующем примере IDL-файла показано, как объявлять массивы с помощью **\[ строкового \]** атрибута.</span><span class="sxs-lookup"><span data-stu-id="3ee38-110">The following sample IDL file demonstrates how to declare arrays with the **\[string\]** attribute.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(8.0)
]
interface arraytest
{
  void fArray8([in, out, string] char achArray[]);
}
```

 

 