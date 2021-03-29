---
title: Таблицы виртуальных функций
description: Таблицы виртуальных функций
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105650268"
---
# <a name="virtual-function-tables"></a><span data-ttu-id="6479b-103">Таблицы виртуальных функций</span><span class="sxs-lookup"><span data-stu-id="6479b-103">Virtual Function Tables</span></span>

<span data-ttu-id="6479b-104">Таблица виртуальных функций — это массив указателей на методы, которые поддерживает объект.</span><span class="sxs-lookup"><span data-stu-id="6479b-104">A virtual function table is an array of pointers to the methods an object supports.</span></span> <span data-ttu-id="6479b-105">Если вы используете C, то объект отображается как структура, первый элемент которой является указателем на таблицу виртуальных функций (**лпвтбл**); то есть первый элемент указывает на массив, содержащий указатели на функции.</span><span class="sxs-lookup"><span data-stu-id="6479b-105">If you're using C, an object appears as a structure whose first member is a pointer to the virtual function table (**lpVtbl**); that is, the first member points to an array containing function pointers.</span></span> <span data-ttu-id="6479b-106">Все методы принимают указатель на таблицу функций в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="6479b-106">The methods all take a pointer to the function table as the first parameter.</span></span> <span data-ttu-id="6479b-107">Таким образом, в следующем примере вызывается метод **Read** объекта **пстреам** :</span><span class="sxs-lookup"><span data-stu-id="6479b-107">Thus, the following example calls the **Read** method of a **pStream** object:</span></span>


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



<span data-ttu-id="6479b-108">В C + + указатель на таблицу виртуальной функции ( *этот* указатель) является неявным.</span><span class="sxs-lookup"><span data-stu-id="6479b-108">In C+ +, the pointer to the virtual function table, the *this* pointer, is implicit.</span></span> <span data-ttu-id="6479b-109">Следующий пример эквивалентен предыдущему примеру при использовании C + +:</span><span class="sxs-lookup"><span data-stu-id="6479b-109">The following is equivalent to the previous example when using C+ +:</span></span>


```C++
pStream->Read(parameters) 
 
```



 

 




