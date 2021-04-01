---
description: Исключением является событие, возникающее во время выполнения программы, и требует выполнения кода за пределами обычного потока управления.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Структурированная обработка исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895442"
---
# <a name="structured-exception-handling"></a><span data-ttu-id="260e6-103">Структурированная обработка исключений</span><span class="sxs-lookup"><span data-stu-id="260e6-103">Structured Exception Handling</span></span>

<span data-ttu-id="260e6-104">*Исключением* является событие, возникающее во время выполнения программы, и требует выполнения кода за пределами обычного потока управления.</span><span class="sxs-lookup"><span data-stu-id="260e6-104">An *exception* is an event that occurs during the execution of a program, and requires the execution of code outside the normal flow of control.</span></span> <span data-ttu-id="260e6-105">Существует два типа исключений: исключения оборудования и исключения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="260e6-105">There are two kinds of exceptions: hardware exceptions and software exceptions.</span></span> <span data-ttu-id="260e6-106">*Аппаратные исключения* инициируются ЦП.</span><span class="sxs-lookup"><span data-stu-id="260e6-106">*Hardware exceptions* are initiated by the CPU.</span></span> <span data-ttu-id="260e6-107">Они могут быть результатом выполнения определенных последовательностей инструкций, таких как деление на ноль или попытка доступа к недопустимому адресу памяти.</span><span class="sxs-lookup"><span data-stu-id="260e6-107">They can result from the execution of certain instruction sequences, such as division by zero or an attempt to access an invalid memory address.</span></span> <span data-ttu-id="260e6-108">*Программные исключения* инициируются явным образом приложениями или операционной системой.</span><span class="sxs-lookup"><span data-stu-id="260e6-108">*Software exceptions* are initiated explicitly by applications or the operating system.</span></span> <span data-ttu-id="260e6-109">Например, система может определить, когда указано недопустимое значение параметра.</span><span class="sxs-lookup"><span data-stu-id="260e6-109">For example, the system can detect when an invalid parameter value is specified.</span></span>

<span data-ttu-id="260e6-110">*Структурированная обработка исключений* — это механизм обработки исключений оборудования и программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="260e6-110">*Structured exception handling* is a mechanism for handling both hardware and software exceptions.</span></span> <span data-ttu-id="260e6-111">Таким образом, код обрабатывает исключения оборудования и программного обеспечения одинаково.</span><span class="sxs-lookup"><span data-stu-id="260e6-111">Therefore, your code will handle hardware and software exceptions identically.</span></span> <span data-ttu-id="260e6-112">Структурированная обработка исключений позволяет получить полный контроль над обработкой исключений, обеспечивает поддержку отладчиков и может использоваться на всех языках программирования и на компьютерах.</span><span class="sxs-lookup"><span data-stu-id="260e6-112">Structured exception handling enables you to have complete control over the handling of exceptions, provides support for debuggers, and is usable across all programming languages and machines.</span></span> <span data-ttu-id="260e6-113">*Векторная обработка исключений* является расширением для структурированной обработки исключений.</span><span class="sxs-lookup"><span data-stu-id="260e6-113">*Vectored exception handling* is an extension to structured exception handling.</span></span>

<span data-ttu-id="260e6-114">Система также поддерживает *обработку завершения*, что позволяет гарантировать, что при выполнении защищенного текста кода также выполняется указанный блок кода завершения.</span><span class="sxs-lookup"><span data-stu-id="260e6-114">The system also supports *termination handling*, which enables you to ensure that whenever a guarded body of code is executed, a specified block of termination code is also executed.</span></span> <span data-ttu-id="260e6-115">Код завершения выполняется независимо от того, как поток управления оставляет защищенный текст.</span><span class="sxs-lookup"><span data-stu-id="260e6-115">The termination code is executed regardless of how the flow of control leaves the guarded body.</span></span> <span data-ttu-id="260e6-116">Например, обработчик завершения может гарантировать, что задачи очистки выполняются даже в том случае, если во время выполнения защищенного текста кода возникло исключение или какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="260e6-116">For example, a termination handler can guarantee that clean-up tasks are performed even if an exception or some other error occurs while the guarded body of code is being executed.</span></span>

-   [<span data-ttu-id="260e6-117">Сведения об структурированной обработке исключений</span><span class="sxs-lookup"><span data-stu-id="260e6-117">About Structured Exception Handling</span></span>](about-structured-exception-handling.md)
-   [<span data-ttu-id="260e6-118">Использование структурированной обработки исключений</span><span class="sxs-lookup"><span data-stu-id="260e6-118">Using Structured Exception Handling</span></span>](using-structured-exception-handling.md)
-   [<span data-ttu-id="260e6-119">Ссылка на структурированную обработку исключений</span><span class="sxs-lookup"><span data-stu-id="260e6-119">Structured Exception Handling Reference</span></span>](structured-exception-handling-reference.md)

 

 



