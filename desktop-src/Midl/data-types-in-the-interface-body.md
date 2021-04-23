---
title: Типы данных в теле интерфейса
description: Тело интерфейса, заключенное в фигурные скобки (), содержит типы данных, которые будут использоваться в удаленных вызовах процедур и прототипах для функций, которые будут выполняться удаленно.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- интерфейсы MIDL, типы данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681404"
---
# <a name="data-types-in-the-interface-body"></a><span data-ttu-id="8474e-104">Типы данных в теле интерфейса</span><span class="sxs-lookup"><span data-stu-id="8474e-104">Data Types in the Interface Body</span></span>

<span data-ttu-id="8474e-105">Тело интерфейса, заключенное в фигурные скобки ({}), содержит типы данных, которые будут использоваться в удаленных вызовах процедур и прототипах для функций, которые будут выполняться удаленно.</span><span class="sxs-lookup"><span data-stu-id="8474e-105">The interface body, which is enclosed in braces ({ }), contains the data types that will be used in remote procedure calls and prototypes for the functions that will be executed remotely.</span></span> <span data-ttu-id="8474e-106">Тело интерфейса может содержать операции импорта, директивы pragma, объявления констант, объявления типов и объявления функций.</span><span class="sxs-lookup"><span data-stu-id="8474e-106">An interface body can contain imports, pragmas, constant declarations, type declarations, and function declarations.</span></span> <span data-ttu-id="8474e-107">Кроме режима совместимости с использование, компилятор MIDL также допускает неявные объявления в форме определений переменных.</span><span class="sxs-lookup"><span data-stu-id="8474e-107">Except in OSF-compatibility mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="8474e-108">Обратите внимание, что спецификация использование-DCE для интерфейсов RPC не позволяет использовать несколько интерфейсов в одном IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="8474e-108">Note that the OSF-DCE specification for RPC interfaces does not allow multiple interfaces in a single IDL file.</span></span> <span data-ttu-id="8474e-109">Таким образом, если компиляция выполняется в режиме совместимости с использование ( [**/ОСФ**](-osf.md)) MIDL, файл IDL может содержать только один интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8474e-109">Therefore, if you are compiling in MIDL's OSF-compatibility mode ( [**/osf**](-osf.md)), your IDL file can contain only one interface.</span></span>

<span data-ttu-id="8474e-110">Дополнительные сведения об использовании компилятора MIDL для создания библиотек типов см. в разделе [Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md).</span><span class="sxs-lookup"><span data-stu-id="8474e-110">For details on using the MIDL compiler to produce type libraries, see [Generating a Type Library with MIDL](generating-a-type-library-with-midl-2.md).</span></span>

<span data-ttu-id="8474e-111">В Microsoft RPC файл IDL может содержать несколько интерфейсов, и эти интерфейсы могут быть объявлены прямо (в IDL-файле, определяющем их).</span><span class="sxs-lookup"><span data-stu-id="8474e-111">In Microsoft RPC, an IDL file can contain multiple interfaces and these interfaces can be forward declared (within the IDL file that defines them).</span></span> <span data-ttu-id="8474e-112">Пример:</span><span class="sxs-lookup"><span data-stu-id="8474e-112">For example:</span></span>

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




