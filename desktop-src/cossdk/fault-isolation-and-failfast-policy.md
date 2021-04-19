---
description: Изоляция сбоев и политика FailFast
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Изоляция сбоев и политика FailFast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538726"
---
# <a name="fault-isolation-and-failfast-policy"></a><span data-ttu-id="4d2d5-103">Изоляция сбоев и политика FailFast</span><span class="sxs-lookup"><span data-stu-id="4d2d5-103">Fault Isolation and Failfast Policy</span></span>

<span data-ttu-id="4d2d5-104">COM+ выполняет широкие внутренние проверки целостности и согласованности.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-104">COM+ performs extensive internal integrity and consistency checks.</span></span> <span data-ttu-id="4d2d5-105">Если в COM+ возникает непредвиденная внутренняя ошибка, она немедленно завершает процесс.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-105">If COM+ encounters an unexpected internal error condition, it immediately terminates the process.</span></span> <span data-ttu-id="4d2d5-106">Эта политика, называемая *FailFast*, упрощает включение и отдает результаты в более надежных и надежных системах.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-106">This policy, called *failfast*, facilitates fault containment and results in more reliable and robust systems.</span></span>

<span data-ttu-id="4d2d5-107">Рассмотрим случай, когда COM+ обнаруживает, что одна из ее структур данных находится в поврежденном состоянии.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-107">Consider a case in which COM+ detects that one of its data structures is in a corrupted state.</span></span> <span data-ttu-id="4d2d5-108">На этом этапе причина и величина повреждения неизвестны, и увы, COM+ не может определить степень распространения ущерба.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-108">At this point, both the cause and the magnitude of the corruption are unknown and, unfortunately, COM+ cannot tell how far the damage has spread.</span></span> <span data-ttu-id="4d2d5-109">Однако даже если COM+ находится в неопределенном состоянии, он не выполняется в режиме изоляции.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-109">However, even though COM+ is in an indeterminate state, it does not run in isolation.</span></span> <span data-ttu-id="4d2d5-110">Как и другие библиотеки DLL, она размещается в среде процесса и использует одно адресное пространство с исполняемым файлом основной программы и многими другими библиотеками DLL.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-110">Like other DLLs, it is hosted in a process environment and shares a single address space with the main program executable and many other DLLs.</span></span> <span data-ttu-id="4d2d5-111">Таким образом, в COM+ предполагается, что весь процесс был поврежден, и процесс немедленно завершается, чтобы предотвратить распространение потенциально поврежденных данных в другие процессы или, что еще хуже, из-за возможности зафиксировать поврежденные данные и сделать их устойчивыми.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-111">Therefore, COM+ assumes that the entire process has been corrupted, and the process is immediately terminated to prevent it from spreading potentially corrupted information to other processes or, worse yet, from allowing corrupted data to be committed and made durable.</span></span>

<span data-ttu-id="4d2d5-112">COM+ не позволяет распространять исключения за пределы контекста.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-112">COM+ does not allow exceptions to propagate outside of a context.</span></span> <span data-ttu-id="4d2d5-113">Если исключение возникает при выполнении в контексте COM+ и приложение не перехватывает исключение перед возвратом из контекста, COM+ перехватывает исключение и завершает процесс.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-113">If an exception occurs while executing within a COM+ context and the application doesn't catch the exception before returning from the context, COM+ catches the exception and terminates the process.</span></span> <span data-ttu-id="4d2d5-114">Использование политики FailFast в этом случае основано на предположении, что исключение поместит процесс в неопределенное состояние. продолжить обработку необязательно.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-114">Using the failfast policy in this case is based on the assumption that the exception has put the process into an indeterminate state; it is not safe to continue processing.</span></span>

<span data-ttu-id="4d2d5-115">Разработчик или администратор должен изучить журнал приложений Просмотр событий, чтобы получить подробные сведения о любом действии FailFast или серьезных ошибках приложения.</span><span class="sxs-lookup"><span data-stu-id="4d2d5-115">As a developer or administrator, you should inspect the Event Viewer application log for details on any failfast action or serious application errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d2d5-116">См. также</span><span class="sxs-lookup"><span data-stu-id="4d2d5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d2d5-117">Поиск источника ошибки</span><span class="sxs-lookup"><span data-stu-id="4d2d5-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="4d2d5-118">Изменение возвращаемых значений COM+</span><span class="sxs-lookup"><span data-stu-id="4d2d5-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="4d2d5-119">Анализ кодов ошибок</span><span class="sxs-lookup"><span data-stu-id="4d2d5-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="4d2d5-120">Стратегии обработки ошибок в COM+</span><span class="sxs-lookup"><span data-stu-id="4d2d5-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="4d2d5-121">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="4d2d5-121">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



