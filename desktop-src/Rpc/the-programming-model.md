---
title: Модель программирования
description: В первые дни программирования компьютера каждая программа была написана как большой монолитный блок, заполненный операторами goto.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776430"
---
# <a name="the-programming-model"></a><span data-ttu-id="91d2c-103">Модель программирования</span><span class="sxs-lookup"><span data-stu-id="91d2c-103">The Programming Model</span></span>

<span data-ttu-id="91d2c-104">В первые дни программирования компьютера каждая программа была написана как большой монолитный блок, заполненный операторами **goto** .</span><span class="sxs-lookup"><span data-stu-id="91d2c-104">In the early days of computer programming, each program was written as a large monolithic chunk, filled with **goto** statements.</span></span> <span data-ttu-id="91d2c-105">Каждая программа должна было управлять собственными входными и выходными данными на различных аппаратных устройствах.</span><span class="sxs-lookup"><span data-stu-id="91d2c-105">Each program had to manage its own input and output to different hardware devices.</span></span> <span data-ttu-id="91d2c-106">По мере разработки дисциплины программирования этот монолитный код был организован в процедуры, а наиболее часто используемые процедуры упакованы в библиотеки для совместного использования и повторного использования.</span><span class="sxs-lookup"><span data-stu-id="91d2c-106">As the programming discipline matured, this monolithic code was organized into procedures, with the most commonly used procedures packed in libraries for sharing and reuse.</span></span>

![монолитные инструкции GOTO и процедуры, Упакованные в общие библиотеки](images/prog-a06.png)

<span data-ttu-id="91d2c-108">Язык программирования C поддерживает процессно-ориентированное программирование.</span><span class="sxs-lookup"><span data-stu-id="91d2c-108">The C programming language supports procedure-oriented programming.</span></span> <span data-ttu-id="91d2c-109">В C Главная процедура относится ко всем остальным процедурам как к черным прямоугольникам.</span><span class="sxs-lookup"><span data-stu-id="91d2c-109">In C, the main procedure relates to all other procedures as black boxes.</span></span> <span data-ttu-id="91d2c-110">Например, основная процедура не может определить, как процедуры A, B и X выполняют свою работу.</span><span class="sxs-lookup"><span data-stu-id="91d2c-110">For example, the main procedure cannot find out how procedures A, B, and X do their work.</span></span> <span data-ttu-id="91d2c-111">Основная процедура вызывает только другую процедуру. Он не содержит сведений о реализации этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="91d2c-111">The main procedure only calls another procedure; it has no information about how that procedure is implemented.</span></span>

![изоляция действий, выполняемых за пределами процедур](images/prog-a08.png)

<span data-ttu-id="91d2c-113">Ориентированные на процедуры языки программирования предоставляют простые механизмы для указания и написания процедур.</span><span class="sxs-lookup"><span data-stu-id="91d2c-113">Procedure-oriented programming languages provide simple mechanisms for specifying and writing procedures.</span></span> <span data-ttu-id="91d2c-114">Например, стандартом ANSI-Function prototype является конструкция, используемая для указания имени процедуры, тип возвращаемого результата (если есть), а также число, последовательность и тип его параметров.</span><span class="sxs-lookup"><span data-stu-id="91d2c-114">For example, the ANSI-standard C-function prototype is a construct used to specify the name of a procedure, the type of the result it returns (if any) and the number, sequence, and type of its parameters.</span></span> <span data-ttu-id="91d2c-115">Использование прототипа функции является формальным способом указания интерфейса между процедурами.</span><span class="sxs-lookup"><span data-stu-id="91d2c-115">Using the function prototype is a formal way to specify an interface between procedures.</span></span>

<span data-ttu-id="91d2c-116">Microsoft RPC строится на этой модели программирования, позволяя процедурам, объединенным в интерфейсы, размещаться в разных процессах, чем вызывающий.</span><span class="sxs-lookup"><span data-stu-id="91d2c-116">Microsoft RPC builds on that programming model by allowing procedures, grouped together in interfaces, to reside in different processes than the caller.</span></span> <span data-ttu-id="91d2c-117">Microsoft RPC также добавляет более формальный подход к определению процедуры, который позволяет вызывающей стороне и вызываемой процедуре принять контракт для удаленного обмена данными и вызова функциональности.</span><span class="sxs-lookup"><span data-stu-id="91d2c-117">Microsoft RPC also adds a more formal approach to procedure definition that allows the caller and the called routine to adopt a contract for remotely exchanging data and invoking functionality.</span></span> <span data-ttu-id="91d2c-118">В модели программирования Microsoft RPC традиционные вызовы функций дополняются двумя дополнительными элементами.</span><span class="sxs-lookup"><span data-stu-id="91d2c-118">In the Microsoft RPC programming model, traditional function calls are supplemented with two additional elements.</span></span>

-   <span data-ttu-id="91d2c-119">Первый элемент — это файл. idl/. ACF, который точно описывает обмен данными и механизм передачи параметров между вызывающей и вызываемой процедурой.</span><span class="sxs-lookup"><span data-stu-id="91d2c-119">The first element is an .idl/.acf file that precisely describes the data exchange and parameter-passing mechanism between the caller and called procedure.</span></span>
-   <span data-ttu-id="91d2c-120">Второй элемент — это набор интерфейсов API времени выполнения, которые предоставляют разработчикам детализированный контроль над удаленным вызовом процедур, включая аспекты безопасности, управление состоянием на сервере, указание клиентов, которые могут обмениваться данными с сервером, и т. д.</span><span class="sxs-lookup"><span data-stu-id="91d2c-120">The second element is a set of run-time APIs that provide developers with granular control of the remote procedure call, including security aspects, managing state on the server, specifying which clients can talk to the server, and so on.</span></span>

 

 




