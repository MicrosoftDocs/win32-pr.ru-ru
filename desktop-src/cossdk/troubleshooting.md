---
description: Устранение неполадок
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Устранение неполадок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682349"
---
# <a name="troubleshooting"></a><span data-ttu-id="f5c35-103">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="f5c35-103">Troubleshooting</span></span>

<span data-ttu-id="f5c35-104">Если возникают проблемы при диагностике ошибок приложения, см. следующие советы по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="f5c35-104">If you are having trouble diagnosing your application errors, refer to the following of troubleshooting tips:</span></span>

-   <span data-ttu-id="f5c35-105">Убедитесь, что координатор распределенных транзакций (DTC) работает на всех серверах.</span><span class="sxs-lookup"><span data-stu-id="f5c35-105">Make sure that the Distributed Transaction Coordinator (DTC) is running on all servers.</span></span>
-   <span data-ttu-id="f5c35-106">Проверьте сетевое взаимодействие путем первого тестирования на локальном компьютере, чтобы убедиться, что приложение работает.</span><span class="sxs-lookup"><span data-stu-id="f5c35-106">Check network communication by first testing on a local computer to verify that the application works.</span></span> <span data-ttu-id="f5c35-107">При использовании протокола TCP/IP в сети можно использовать служебную программу ping.exe, чтобы убедиться, что компьютеры находятся в сети.</span><span class="sxs-lookup"><span data-stu-id="f5c35-107">If you are running TCP/IP on your network, you can use the ping.exe utility to verify that the machines are on the network.</span></span>
-   <span data-ttu-id="f5c35-108">Убедитесь, что SQL и DTC расположены на одном компьютере или программа настройки клиента DTC указывает, что DTC находится на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="f5c35-108">Make sure that SQL and DTC are located on the same computer or that the DTC Client Configuration program specifies that the DTC is on another computer.</span></span> <span data-ttu-id="f5c35-109">В противном случае SQLConnect будет возвращать ошибку внутренне при вызове из транзакционного компонента.</span><span class="sxs-lookup"><span data-stu-id="f5c35-109">If not, SQLConnect will return an error internally when called from a transactional component.</span></span>
-   <span data-ttu-id="f5c35-110">Задайте для времени ожидания транзакции большее значение, чем значение по умолчанию 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="f5c35-110">Set the transaction time-out to a higher number than the default 60 seconds.</span></span> <span data-ttu-id="f5c35-111">По истечении времени ожидания транзакции COM+ прерывает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="f5c35-111">After the transaction time-out has elapsed, COM+ aborts the transaction.</span></span> <span data-ttu-id="f5c35-112">Все последующие вызовы компонента возвращают немедленный результат с КОНТЕКСТом \_ E \_ .</span><span class="sxs-lookup"><span data-stu-id="f5c35-112">All subsequent calls to the component return immediately with CONTEXT\_E\_ABORTED.</span></span>
-   <span data-ttu-id="f5c35-113">Убедитесь, что драйверы ODBC являются потокобезопасными и не имеют сходства потоков.</span><span class="sxs-lookup"><span data-stu-id="f5c35-113">Make sure that your ODBC drivers are thread-safe and do not have thread affinity.</span></span>
-   <span data-ttu-id="f5c35-114">Если у вас возникли трудности с тем, чтобы приложение работало на нескольких серверах, перезагрузите клиент и убедитесь, что контроллер домена настроен правильно.</span><span class="sxs-lookup"><span data-stu-id="f5c35-114">If you have difficulty getting an application to work over several servers, reboot the client and then verify that your domain controller is configured properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5c35-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f5c35-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5c35-116">Изоляция сбоев и политика FailFast</span><span class="sxs-lookup"><span data-stu-id="f5c35-116">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="f5c35-117">Поиск источника ошибки</span><span class="sxs-lookup"><span data-stu-id="f5c35-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="f5c35-118">Изменение возвращаемых значений COM+</span><span class="sxs-lookup"><span data-stu-id="f5c35-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="f5c35-119">Анализ кодов ошибок</span><span class="sxs-lookup"><span data-stu-id="f5c35-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="f5c35-120">Стратегии обработки ошибок в COM+</span><span class="sxs-lookup"><span data-stu-id="f5c35-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



