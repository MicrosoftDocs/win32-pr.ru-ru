---
description: Обработка ошибок в COM+ CRM
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Обработка ошибок в COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496341"
---
# <a name="error-handling-in-the-com-crm"></a><span data-ttu-id="2fa06-103">Обработка ошибок в COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="2fa06-103">Error Handling in the COM+ CRM</span></span>

<span data-ttu-id="2fa06-104">Серверные приложения COM+ реализуют политику FailFast.</span><span class="sxs-lookup"><span data-stu-id="2fa06-104">COM+ server applications implement a failfast policy.</span></span> <span data-ttu-id="2fa06-105">При обнаружении серьезной внутренней ошибки процесс серверного приложения завершает работу и записывает сообщение об ошибке в журнал событий Windows.</span><span class="sxs-lookup"><span data-stu-id="2fa06-105">If a serious internal error is detected, the server application process exits and writes an error message to the Windows event log.</span></span> <span data-ttu-id="2fa06-106">Это обеспечивает быстрое обнаружение проблем и может быть вызвано защитой данных приложения путем обработки транзакций.</span><span class="sxs-lookup"><span data-stu-id="2fa06-106">This allows quick detection of problems and is possible due to the protection of application data by transaction processing.</span></span> <span data-ttu-id="2fa06-107">Всегда проверяйте журнал событий Windows на наличие ошибок в CRM во время разработки или в окончательном развертывании.</span><span class="sxs-lookup"><span data-stu-id="2fa06-107">Always check the Windows event log for any errors from the CRM, either during development or during final deployment.</span></span>

<span data-ttu-id="2fa06-108">Основные ошибки в использовании интерфейсов CRM, например недопустимые аргументы или ошибки последовательности (например, попытка записи записи журнала перед регистрацией компенсатора CRM), возвращают коды ошибок и не должны активировать FailFast.</span><span class="sxs-lookup"><span data-stu-id="2fa06-108">Basic errors in using the CRM interfaces, such as invalid arguments or sequence errors (for example, trying to write a log record before registering the CRM Compensator), return error codes and should not trigger failfast.</span></span> <span data-ttu-id="2fa06-109">Для разработки CRM вы можете задать раздел реестра VTRACE1 (см. раздел [параметры реестра com+ CRM](com--crm-registry-settings.md)), в результате чего сообщение будет отображаться в окне вывод отладчика для каждой ошибки.</span><span class="sxs-lookup"><span data-stu-id="2fa06-109">For CRM development, you may choose to set the VTRACE1 registry key (see [COM+ CRM Registry Settings](com--crm-registry-settings.md)), which causes a message to appear in the debugger output window for each error.</span></span>

<span data-ttu-id="2fa06-110">Также могут возникать временные ошибки.</span><span class="sxs-lookup"><span data-stu-id="2fa06-110">Transient errors can also occur.</span></span> <span data-ttu-id="2fa06-111">Эти ошибки обычно вызываются условиями времени и приводят к возвращению кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="2fa06-111">These errors are typically caused by timing conditions and result in an error code being returned.</span></span> <span data-ttu-id="2fa06-112">Разработчик CRM должен убедиться, что эти условия возникновения ошибок обработаны.</span><span class="sxs-lookup"><span data-stu-id="2fa06-112">The CRM developer should ensure that these error conditions are handled.</span></span> <span data-ttu-id="2fa06-113">Например, при записи записи в журнал транзакция может быть прервана из-за истечения времени ожидания. Затем метод возвращает ошибку, которую вызывающий объект должен проверять и правильно управлять.</span><span class="sxs-lookup"><span data-stu-id="2fa06-113">For example, while writing a log record, the transaction could abort due to a time-out. The method then returns an error, which the caller should check for and handle appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fa06-114">См. также</span><span class="sxs-lookup"><span data-stu-id="2fa06-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fa06-115">Основные понятия о компенсации диспетчер ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="2fa06-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



