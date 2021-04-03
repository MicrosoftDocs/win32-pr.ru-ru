---
description: В этом разделе описывается синтаксис и использование структурированной обработки исключений в соответствии с реализацией в оптимизирующих компиляторе Microsoft C/C++. Компилятор интерпретирует следующие ключевые слова как часть структурированного механизма обработки исключений.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Синтаксис обработчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895449"
---
# <a name="handler-syntax"></a><span data-ttu-id="cd20f-104">Синтаксис обработчика</span><span class="sxs-lookup"><span data-stu-id="cd20f-104">Handler Syntax</span></span>

<span data-ttu-id="cd20f-105">В этом разделе описывается синтаксис и использование структурированной обработки исключений в соответствии с реализацией в оптимизирующих компиляторе Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="cd20f-105">This section describes the syntax and usage of structured exception handling as implemented in the Microsoft C/C++ Optimizing Compiler.</span></span> <span data-ttu-id="cd20f-106">Компилятор интерпретирует следующие ключевые слова как часть структурированного механизма обработки исключений.</span><span class="sxs-lookup"><span data-stu-id="cd20f-106">The following keywords are interpreted by the compiler as part of the structured exception-handling mechanism.</span></span>



| <span data-ttu-id="cd20f-107">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="cd20f-107">Keyword</span></span>         | <span data-ttu-id="cd20f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="cd20f-108">Description</span></span>                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd20f-109">**\_\_try**</span><span class="sxs-lookup"><span data-stu-id="cd20f-109">**\_\_try**</span></span>     | <span data-ttu-id="cd20f-110">Начинает защищенный текст кода.</span><span class="sxs-lookup"><span data-stu-id="cd20f-110">Begins a guarded body of code.</span></span> <span data-ttu-id="cd20f-111">Используется с ключевым словом **\_ \_ except** для создания [обработчика исключений](exception-handler-syntax.md)или с ключевым словом **\_ \_ finally** для создания [обработчика завершения](termination-handler-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cd20f-111">Used with the **\_\_except** keyword to construct an [exception handler](exception-handler-syntax.md), or with the **\_\_finally** keyword to construct a [termination handler](termination-handler-syntax.md).</span></span> |
| <span data-ttu-id="cd20f-112">**\_\_варианта**</span><span class="sxs-lookup"><span data-stu-id="cd20f-112">**\_\_except**</span></span>  | <span data-ttu-id="cd20f-113">Начинает блок кода, который выполняется, только если исключение возникает в связанном блоке **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="cd20f-113">Begins a block of code that is executed only when an exception occurs within its associated **\_\_try** block.</span></span>                                                                                                                                   |
| <span data-ttu-id="cd20f-114">**\_\_finally**</span><span class="sxs-lookup"><span data-stu-id="cd20f-114">**\_\_finally**</span></span> | <span data-ttu-id="cd20f-115">Начинает блок кода, который выполняется, когда поток управления оставляет связанный блок **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="cd20f-115">Begins a block of code that is executed whenever the flow of control leaves its associated **\_\_try** block.</span></span>                                                                                                                                    |
| <span data-ttu-id="cd20f-116">**\_\_выхода**</span><span class="sxs-lookup"><span data-stu-id="cd20f-116">**\_\_leave**</span></span>   | <span data-ttu-id="cd20f-117">Разрешает немедленное завершение блока **\_ \_ try** , не вызывая аварийное завершение работы и снижения его производительности.</span><span class="sxs-lookup"><span data-stu-id="cd20f-117">Allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span>                                                                                                                      |



 

<span data-ttu-id="cd20f-118">Компилятор также интерпретирует функции [**GetExceptionCode**](getexceptioncode.md), [**жетексцептионинформатион**](getexceptioninformation.md)и [**абнормалтерминатион**](abnormaltermination.md) как ключевые слова, и их использование вне соответствующего синтаксиса обработки исключений приводит к ошибке компилятора.</span><span class="sxs-lookup"><span data-stu-id="cd20f-118">The compiler also interprets the [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md), and [**AbnormalTermination**](abnormaltermination.md) functions as keywords, and their use outside the appropriate exception-handling syntax generates a compiler error.</span></span> <span data-ttu-id="cd20f-119">Ниже приведены краткие описания этих функций.</span><span class="sxs-lookup"><span data-stu-id="cd20f-119">The following are brief descriptions of these functions.</span></span>



| <span data-ttu-id="cd20f-120">Функция</span><span class="sxs-lookup"><span data-stu-id="cd20f-120">Function</span></span>                                                   | <span data-ttu-id="cd20f-121">Описание</span><span class="sxs-lookup"><span data-stu-id="cd20f-121">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd20f-122">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="cd20f-122">**GetExceptionCode**</span></span>](getexceptioncode.md)               | <span data-ttu-id="cd20f-123">Возвращает код, определяющий тип исключения.</span><span class="sxs-lookup"><span data-stu-id="cd20f-123">Returns a code that identifies the type of exception.</span></span> <span data-ttu-id="cd20f-124">Эта функция может быть вызвана только внутри выражения фильтра или блока обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="cd20f-124">This function can be called only from within the filter expression or the exception-handler block.</span></span>                                                                                                |
| [<span data-ttu-id="cd20f-125">**жетексцептионинформатион**</span><span class="sxs-lookup"><span data-stu-id="cd20f-125">**GetExceptionInformation**</span></span>](getexceptioninformation.md) | <span data-ttu-id="cd20f-126">Возвращает указатель на структуру [**\_ указателей исключений**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) , содержащую указатели на запись контекста и запись исключения.</span><span class="sxs-lookup"><span data-stu-id="cd20f-126">Returns a pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure containing pointers to the context record and the exception record.</span></span> <span data-ttu-id="cd20f-127">Эту функцию можно вызывать только в критерии фильтра обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="cd20f-127">This function can be called only from within the filter expression of an exception handler.</span></span> |
| [<span data-ttu-id="cd20f-128">**абнормалтерминатион**</span><span class="sxs-lookup"><span data-stu-id="cd20f-128">**AbnormalTermination**</span></span>](abnormaltermination.md)         | <span data-ttu-id="cd20f-129">Указывает, будет ли поток управления оставлять связанный блок **\_ \_ try** последовательно после выполнения последней инструкции в блоке.</span><span class="sxs-lookup"><span data-stu-id="cd20f-129">Indicates whether the flow of control left the associated **\_\_try** block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="cd20f-130">Эту функцию можно вызывать только в блоке **\_ \_ finally** обработчика завершения.</span><span class="sxs-lookup"><span data-stu-id="cd20f-130">This function can be called only from within the **\_\_finally** block of a termination handler.</span></span>              |



 

 

 



