---
description: При возникновении исключения в отлаживаемом процессе система уведомляет отладчик, передавая ему исключение. Это называется первым шансом уведомления. Затем система приостанавливает все потоки в отлаживаемом процессе.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Функции обработки исключений для отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895285"
---
# <a name="exception-handling-functions-for-debugging"></a><span data-ttu-id="02bbc-105">Функции обработки исключений для отладки</span><span class="sxs-lookup"><span data-stu-id="02bbc-105">Exception Handling Functions for Debugging</span></span>

<span data-ttu-id="02bbc-106">При возникновении исключения в отлаживаемом процессе система уведомляет отладчик, передавая ему исключение.</span><span class="sxs-lookup"><span data-stu-id="02bbc-106">When an exception occurs in a process that is being debugged, the system notifies the debugger by passing the exception to it.</span></span> <span data-ttu-id="02bbc-107">Это называется *первым шансом уведомления*.</span><span class="sxs-lookup"><span data-stu-id="02bbc-107">This is known as *first-chance notification*.</span></span> <span data-ttu-id="02bbc-108">Затем система приостанавливает все потоки в отлаживаемом процессе.</span><span class="sxs-lookup"><span data-stu-id="02bbc-108">The system then suspends all threads in the process being debugged.</span></span>

<span data-ttu-id="02bbc-109">Если отладчик не обрабатывает исключение, система пытается выполнить обнаружение соответствующего обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="02bbc-109">If the debugger does not handle the exception, the system attempts to locate an appropriate exception handler.</span></span> <span data-ttu-id="02bbc-110">Если система не может выбрать подходящий, система снова Уведомляет отладчик о том, что произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="02bbc-110">If the system cannot locate an appropriate one, the system again notifies the debugger that an exception has occurred.</span></span> <span data-ttu-id="02bbc-111">Это называется *уведомлением о последнем шансе*.</span><span class="sxs-lookup"><span data-stu-id="02bbc-111">This is known as *last-chance notification*.</span></span> <span data-ttu-id="02bbc-112">Если отладчик не обрабатывает исключение после уведомления о последнем шансе, система завершает отлаживаемый процесс.</span><span class="sxs-lookup"><span data-stu-id="02bbc-112">If the debugger does not handle the exception after the last-chance notification, the system terminates the process being debugged.</span></span>

<span data-ttu-id="02bbc-113">Дополнительные сведения см. в разделе [обработка исключений отладчика](debugger-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="02bbc-113">For more information, see [Debugger Exception Handling](debugger-exception-handling.md).</span></span>

 

 



