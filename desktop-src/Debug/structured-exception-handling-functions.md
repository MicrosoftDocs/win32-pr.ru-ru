---
description: В структурированной обработке исключений используются следующие функции.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Функции структурированной обработки исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655769"
---
# <a name="structured-exception-handling-functions"></a><span data-ttu-id="a869d-103">Функции структурированной обработки исключений</span><span class="sxs-lookup"><span data-stu-id="a869d-103">Structured Exception Handling Functions</span></span>

<span data-ttu-id="a869d-104">В структурированной обработке исключений используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="a869d-104">The following functions are used in structured exception handling.</span></span>

-   [<span data-ttu-id="a869d-105">**абнормалтерминатион**</span><span class="sxs-lookup"><span data-stu-id="a869d-105">**AbnormalTermination**</span></span>](abnormaltermination.md)

    <span data-ttu-id="a869d-106">Указывает, завершается ли блок **\_ \_ try** обработчика завершения в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="a869d-106">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span>

-   [<span data-ttu-id="a869d-107">**аддвекторедконтинуехандлер**</span><span class="sxs-lookup"><span data-stu-id="a869d-107">**AddVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    <span data-ttu-id="a869d-108">Регистрирует обработчик векторного продолжения.</span><span class="sxs-lookup"><span data-stu-id="a869d-108">Registers a vectored continue handler.</span></span>

-   [<span data-ttu-id="a869d-109">**аддвекторедексцептионхандлер**</span><span class="sxs-lookup"><span data-stu-id="a869d-109">**AddVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    <span data-ttu-id="a869d-110">Регистрирует векторный обработчик исключений.</span><span class="sxs-lookup"><span data-stu-id="a869d-110">Registers a vectored exception handler.</span></span>

-   [<span data-ttu-id="a869d-111">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="a869d-111">**GetExceptionCode**</span></span>](getexceptioncode.md)

    <span data-ttu-id="a869d-112">Извлекает код, определяющий тип произошедшего исключения.</span><span class="sxs-lookup"><span data-stu-id="a869d-112">Retrieves a code that identifies the type of exception that occurred.</span></span>

-   [<span data-ttu-id="a869d-113">**жетексцептионинформатион**</span><span class="sxs-lookup"><span data-stu-id="a869d-113">**GetExceptionInformation**</span></span>](getexceptioninformation.md)

    <span data-ttu-id="a869d-114">Извлекает независимое от компьютера описание исключения и сведения о состоянии компьютера, существовавшего для потока при возникновении исключения.</span><span class="sxs-lookup"><span data-stu-id="a869d-114">Retrieves a machine-independent description of an exception, and information about the machine state that existed for the thread when the exception occurred.</span></span>

-   [<span data-ttu-id="a869d-115">**RaiseException**</span><span class="sxs-lookup"><span data-stu-id="a869d-115">**RaiseException**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    <span data-ttu-id="a869d-116">Вызывает исключение в вызывающем потоке.</span><span class="sxs-lookup"><span data-stu-id="a869d-116">Raises an exception in the calling thread.</span></span>

-   [<span data-ttu-id="a869d-117">**ремовевекторедконтинуехандлер**</span><span class="sxs-lookup"><span data-stu-id="a869d-117">**RemoveVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    <span data-ttu-id="a869d-118">Отменяет регистрацию обработчика векторного продолжения.</span><span class="sxs-lookup"><span data-stu-id="a869d-118">Unregisters a vectored continue handler.</span></span>

-   [<span data-ttu-id="a869d-119">**ремовевекторедексцептионхандлер**</span><span class="sxs-lookup"><span data-stu-id="a869d-119">**RemoveVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    <span data-ttu-id="a869d-120">Отменяет регистрацию векторного обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="a869d-120">Unregisters a vectored exception handler.</span></span>

-   [<span data-ttu-id="a869d-121">**ртладдгроваблефунктионтабле**</span><span class="sxs-lookup"><span data-stu-id="a869d-121">**RtlAddGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    <span data-ttu-id="a869d-122">Информирует систему о динамической таблице функций, представляющей область памяти, в которой находится код.</span><span class="sxs-lookup"><span data-stu-id="a869d-122">Informs the system of a dynamic function table representing a region of memory containing code.</span></span>

-   [<span data-ttu-id="a869d-123">**ртлделетегроваблефунктионтабле**</span><span class="sxs-lookup"><span data-stu-id="a869d-123">**RtlDeleteGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    <span data-ttu-id="a869d-124">Информирует систему о том, что ранее указанная таблица динамической функции больше не используется.</span><span class="sxs-lookup"><span data-stu-id="a869d-124">Informs the system that a previously reported dynamic function table is no longer in use.</span></span>

-   [<span data-ttu-id="a869d-125">**ртлгровфунктионтабле**</span><span class="sxs-lookup"><span data-stu-id="a869d-125">**RtlGrowFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    <span data-ttu-id="a869d-126">Сообщает о увеличении размера таблицы динамической функции.</span><span class="sxs-lookup"><span data-stu-id="a869d-126">Reports that a dynamic function table has increased in size.</span></span>

-   [<span data-ttu-id="a869d-127">**сетунхандледексцептионфилтер**</span><span class="sxs-lookup"><span data-stu-id="a869d-127">**SetUnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    <span data-ttu-id="a869d-128">Позволяет приложению заменять обработчик исключений верхнего уровня для каждого потока и процесса.</span><span class="sxs-lookup"><span data-stu-id="a869d-128">Enables an application to supersede the top-level exception handler of each thread and process.</span></span>

-   [<span data-ttu-id="a869d-129">**UnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="a869d-129">**UnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    <span data-ttu-id="a869d-130">Передает необработанные исключения в отладчик, если процесс отлаживается.</span><span class="sxs-lookup"><span data-stu-id="a869d-130">Passes unhandled exceptions to the debugger, if the process is being debugged.</span></span>

-   [<span data-ttu-id="a869d-131">**векторедхандлер**</span><span class="sxs-lookup"><span data-stu-id="a869d-131">**VectoredHandler**</span></span>](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    <span data-ttu-id="a869d-132">Определяемая приложением функция, которая служит в качестве векторного обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="a869d-132">An application-defined function that serves as a vectored exception handler.</span></span>

<span data-ttu-id="a869d-133">Следующие функции используются только в 64-разрядных Windows.</span><span class="sxs-lookup"><span data-stu-id="a869d-133">The following functions are used only on 64-bit Windows.</span></span>

-   [<span data-ttu-id="a869d-134">**ртладдфунктионтабле**</span><span class="sxs-lookup"><span data-stu-id="a869d-134">**RtlAddFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    <span data-ttu-id="a869d-135">Добавляет таблицу динамической функции в список таблиц динамических функций.</span><span class="sxs-lookup"><span data-stu-id="a869d-135">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="a869d-136">**ртлкаптуреконтекст**</span><span class="sxs-lookup"><span data-stu-id="a869d-136">**RtlCaptureContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    <span data-ttu-id="a869d-137">Извлекает запись контекста в контексте вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="a869d-137">Retrieves a context record in the context of the caller.</span></span>

-   [<span data-ttu-id="a869d-138">**ртлделетефунктионтабле**</span><span class="sxs-lookup"><span data-stu-id="a869d-138">**RtlDeleteFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    <span data-ttu-id="a869d-139">Удаляет таблицу динамической функции из списка таблиц динамических функций.</span><span class="sxs-lookup"><span data-stu-id="a869d-139">Removes a dynamic function table from the dynamic function table list.</span></span>

-   [<span data-ttu-id="a869d-140">**ртлинсталлфунктионтаблекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="a869d-140">**RtlInstallFunctionTableCallback**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    <span data-ttu-id="a869d-141">Добавляет таблицу динамической функции в список таблиц динамических функций.</span><span class="sxs-lookup"><span data-stu-id="a869d-141">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="a869d-142">**ртлрестореконтекст**</span><span class="sxs-lookup"><span data-stu-id="a869d-142">**RtlRestoreContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    <span data-ttu-id="a869d-143">Восстанавливает контекст вызывающего объекта в указанную запись контекста.</span><span class="sxs-lookup"><span data-stu-id="a869d-143">Restores the context of the caller to the specified context record.</span></span>

 

 
