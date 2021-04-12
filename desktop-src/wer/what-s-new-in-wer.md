---
title: Новые возможности в WER
description: На этой странице перечислены новые функции отчеты об ошибках Windows (WER) для каждого выпуска.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Отчеты об ошибках Windows отчетов об ошибках Windows, новые возможности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336825"
---
# <a name="whats-new-in-wer"></a><span data-ttu-id="6bc25-104">Новые возможности в WER</span><span class="sxs-lookup"><span data-stu-id="6bc25-104">What's New in WER</span></span>

<span data-ttu-id="6bc25-105">На этой странице перечислены новые функции отчеты об ошибках Windows (WER) для каждого выпуска.</span><span class="sxs-lookup"><span data-stu-id="6bc25-105">This page summarizes the new features of Windows Error Reporting (WER) for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="6bc25-106">Windows 7 и Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6bc25-106">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="6bc25-107">В следующем списке перечислены новые функции WER для Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6bc25-107">The following list summarizes the new WER features for Windows 7 and Windows Server 2008 R2.</span></span>

-   <span data-ttu-id="6bc25-108">Добавляет возможность вызвать исключение, которое обходит все обработчики исключений, тем самым завершая работу приложения немедленно и вызывая отчеты об ошибках Windows.</span><span class="sxs-lookup"><span data-stu-id="6bc25-108">Adds the ability to raise an exception that bypasses all exception handlers thus terminating the application immediately and invoking Windows Error Reporting.</span></span> <span data-ttu-id="6bc25-109">Дополнительные сведения см. в описании функции [**раисефаилфастексцептион**](/previous-versions/dd408166(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6bc25-109">For details, see the [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) function.</span></span>
-   <span data-ttu-id="6bc25-110">Добавляет возможность регистрации необработанного обработчика исключений, который сообщает о вызовах, когда происходит сбой для получения имени события, параметров отчетов и параметров запуска отладки.</span><span class="sxs-lookup"><span data-stu-id="6bc25-110">Adds the ability to register an out-of-process exception handler that WER calls when a crash occurs to collect the event name, reporting parameters, and debug launching options.</span></span> <span data-ttu-id="6bc25-111">Дополнительные сведения см. в описании функции [**веррегистеррунтимиксцептионмодуле**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) .</span><span class="sxs-lookup"><span data-stu-id="6bc25-111">For details, see the [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) function.</span></span>

<span data-ttu-id="6bc25-112">Добавленные функции:</span><span class="sxs-lookup"><span data-stu-id="6bc25-112">Functions that were added:</span></span>

-   [<span data-ttu-id="6bc25-113">**аутофпроцессексцептионевенткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="6bc25-113">**OutOfProcessExceptionEventCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [<span data-ttu-id="6bc25-114">**аутофпроцессексцептионевентсигнатурекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="6bc25-114">**OutOfProcessExceptionEventSignatureCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [<span data-ttu-id="6bc25-115">**аутофпроцессексцептионевентдебугжерлаунчкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="6bc25-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   <span data-ttu-id="6bc25-116">[**раисефаилфастексцептион**](/previous-versions/dd408166(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6bc25-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span></span>
-   [<span data-ttu-id="6bc25-117">**веррегистеррунтимиксцептионмодуле**</span><span class="sxs-lookup"><span data-stu-id="6bc25-117">**WerRegisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [<span data-ttu-id="6bc25-118">**верунрегистеррунтимиксцептионмодуле**</span><span class="sxs-lookup"><span data-stu-id="6bc25-118">**WerUnregisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

<span data-ttu-id="6bc25-119">Добавленные структуры:</span><span class="sxs-lookup"><span data-stu-id="6bc25-119">Structures that were added:</span></span>

-   [<span data-ttu-id="6bc25-120">**\_ \_ сведения об исключении среды выполнения WER \_**</span><span class="sxs-lookup"><span data-stu-id="6bc25-120">**WER\_RUNTIME\_EXCEPTION\_INFORMATION**</span></span>](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="6bc25-121">Windows Server 2008 и Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="6bc25-121">Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="6bc25-122">В следующем списке перечислены новые возможности WER для Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6bc25-122">The following list summarizes the new features of WER for Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

-   <span data-ttu-id="6bc25-123">WER можно настроить таким образом, чтобы полные дампы пользовательского режима собираются и сохранялись локально после аварийного завершения работы приложения пользовательского режима (приложения, которые выполняют собственные отчеты о сбоях, включая приложения .NET, не поддерживаются).</span><span class="sxs-lookup"><span data-stu-id="6bc25-123">WER can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes (applications that do their own custom crash reporting, including .NET applications are not supported).</span></span> <span data-ttu-id="6bc25-124">Дополнительные сведения см. в разделе [сбор User-Mode дампов](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="6bc25-124">For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="6bc25-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6bc25-125">Windows Vista</span></span>

<span data-ttu-id="6bc25-126">В следующем списке перечислены новые функции отчеты об ошибках Windows (WER) для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6bc25-126">The following list summarizes the new features of Windows Error Reporting (WER) for Windows Vista:</span></span>

-   <span data-ttu-id="6bc25-127">Средство WER было расширено за пределами мониторинга сбоев и неотвечающими процессами.</span><span class="sxs-lookup"><span data-stu-id="6bc25-127">WER has been extended beyond monitoring crashes and unresponsive processes.</span></span> <span data-ttu-id="6bc25-128">WER включает поддержку многих новых типов некритических событий, таких как проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="6bc25-128">WER includes support for many new types of non-critical events, such as performance issues.</span></span> <span data-ttu-id="6bc25-129">Это позволяет разработчикам больше узнать о работе своих клиентов с разрабатываемыми ими приложениями.</span><span class="sxs-lookup"><span data-stu-id="6bc25-129">This enables developers to learn more about the experiences their customers have with the applications they have developed.</span></span>
-   <span data-ttu-id="6bc25-130">Новые функции дают разработчикам гибкие возможности создания, настройки и отправки отчетов о проблемах.</span><span class="sxs-lookup"><span data-stu-id="6bc25-130">New functions give developers the flexibility in creating, customizing, and submitting problem reports.</span></span> <span data-ttu-id="6bc25-131">Дополнительные сведения см. в разделе [функции WER](wer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6bc25-131">For more information, see [WER Functions](wer-functions.md).</span></span>
-   <span data-ttu-id="6bc25-132">Улучшенные [веб-службы Windows Quality](https://www.microsoft.com/?ref=go) предоставляют разработчикам доступ к сведениям о проблемах, которые клиенты отправляют для своих приложений, и механизм для предоставления решений этим клиентам.</span><span class="sxs-lookup"><span data-stu-id="6bc25-132">The improved [Windows Quality Online Services](https://www.microsoft.com/?ref=go) provides developers with access to the problem information that customers are submitting for their applications, and a mechanism to deliver solutions to these customers.</span></span>
-   <span data-ttu-id="6bc25-133">Функции, появившиеся при [восстановлении приложений,](/windows/desktop/Recovery/application-recovery-and-restart-portal) а также при перезапуске и перезапуске [диспетчера](/windows/desktop/RstMgr/restart-manager-portal) , позволяют приложениям автоматически восстанавливать сведения и перезапускаться в случае критического сбоя.</span><span class="sxs-lookup"><span data-stu-id="6bc25-133">The functions introduced by [Application Recovery and Restart](/windows/desktop/Recovery/application-recovery-and-restart-portal) and [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) enable applications to automatically recover information and restart in the event of a critical failure.</span></span> <span data-ttu-id="6bc25-134">Разработчики могут использовать эти функции в своих приложениях для значительного улучшения взаимодействия с пользователями.</span><span class="sxs-lookup"><span data-stu-id="6bc25-134">Developers can use these features in their applications to significantly improve their user experience.</span></span>
-   <span data-ttu-id="6bc25-135">**Отчеты о проблемах и решения в Windows Vista или в центре действий в Windows 7** являются центральным местом для взаимодействия пользователей с WER.</span><span class="sxs-lookup"><span data-stu-id="6bc25-135">**Problem Reports and Solutions on Windows Vista or the Action Center on Windows 7** is the central location for users to interact with WER.</span></span> <span data-ttu-id="6bc25-136">Пользователи могут проверять наличие новых решений, управлять их журналом отчетов, просматривать сведения о проблеме и управлять параметрами отчетов, включая включение WER для автоматического поиска решений без прерывания работы пользователя.</span><span class="sxs-lookup"><span data-stu-id="6bc25-136">Users can check for new solutions, manage their reporting history, view the details of a problem report, and manage reporting settings including enabling WER to check for solutions automatically without interrupting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bc25-137">См. также</span><span class="sxs-lookup"><span data-stu-id="6bc25-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bc25-138">Отчеты об ошибках Windows</span><span class="sxs-lookup"><span data-stu-id="6bc25-138">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 