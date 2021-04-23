---
title: " в, size_is и out size_is prototype"
description: В следующем прототипе функции используются две подсчитанные строки. Разработчик должен написать код как на клиенте, так и на сервере, чтобы контролировать длину массивов символов и передавать параметры, которые указывают заглушкам, сколько элементов массива передавать.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413541"
---
# <a name="in-size_is-and-out-size_is-prototype"></a><span data-ttu-id="7f9b2-104">\[в, размер \_ \] и \[ , размер \_ — \] прототип</span><span class="sxs-lookup"><span data-stu-id="7f9b2-104">\[in, size\_is\] and \[out, size\_is\] Prototype</span></span>

<span data-ttu-id="7f9b2-105">В следующем прототипе функции используются две подсчитанные строки.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-105">The following function prototype uses two counted strings.</span></span> <span data-ttu-id="7f9b2-106">Разработчик должен написать код как на клиенте, так и на сервере, чтобы контролировать длину массивов символов и передавать параметры, которые указывают заглушкам, сколько элементов массива передавать.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-106">The developer must write code on both client and server to keep track of the character array lengths and pass parameters that tell the stubs how many array elements to transmit.</span></span>

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

<span data-ttu-id="7f9b2-107">Обратите внимание, что параметры, описывающие длину массива, передаются в том же направлении, что и массивы: *кбин* и *Ачин* находятся \[ [**в**](/windows/desktop/Midl/in) \] параметрах, тогда как *пкбаут* и *ачаут* являются \[ [**выходными**](/windows/desktop/Midl/out-idl) \] параметрами.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-107">Note the parameters that describe the array length are transmitted in the same direction as the arrays: *cbIn* and *achIn* are \[[**in**](/windows/desktop/Midl/in)\] parameters while *pcbOut* and *achOut* are \[[**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="7f9b2-108">В качестве параметра **\[ \] out** параметр *Пкбаут* должен следовать соглашению C и объявляться как указатель.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-108">As an **\[out\]** parameter, the parameter *pcbOut* must follow C convention and be declared as a pointer.</span></span>

<span data-ttu-id="7f9b2-109">Клиентский код подсчитывает количество символов в строке, включая замыкающий нуль, перед вызовом удаленной процедуры, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="7f9b2-109">The client code counts the number of characters in the string, including the trailing zero, before calling the remote procedure as shown:</span></span>

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

<span data-ttu-id="7f9b2-110">Удаленная процедура на сервере предоставляет длину буфера возврата в *кбаут* , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="7f9b2-110">The remote procedure on the server supplies the length of the return buffer in *cbOut* as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

<span data-ttu-id="7f9b2-111">\[  \] Если известно, что параметр является строковым, можно использовать атрибут String.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-111">The \[**string**\] attribute can be utilized when a parameter is known to be a string.</span></span> <span data-ttu-id="7f9b2-112">Этот атрибут направляет заглушку для вычисления размера строки, тем самым устраняя издержки, связанные с \[ [**длиной, —**](/windows/desktop/Midl/size-is) \] параметрами.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-112">This attribute directs the stub to calculate the string size, thus eliminating the overhead associated with the \[[**length is**](/windows/desktop/Midl/size-is)\] parameters.</span></span> <span data-ttu-id="7f9b2-113">Кроме того, она будет направлять заглушку для проверки того, что строка **была прервана, перед** передачей параметра в приложение.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-113">Additionally, it will direct the stub to verify the string is **NULL** terminated before passing the parameter to the application.</span></span>

 

 