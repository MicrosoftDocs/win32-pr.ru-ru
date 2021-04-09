---
description: Поиск источника ошибки
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Поиск источника ошибки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072519"
---
# <a name="finding-the-source-of-an-error"></a><span data-ttu-id="a1f64-103">Поиск источника ошибки</span><span class="sxs-lookup"><span data-stu-id="a1f64-103">Finding the Source of an Error</span></span>

<span data-ttu-id="a1f64-104">Вы можете диагностировать источник и получить описание ошибок приложения с помощью COM+ и других средств.</span><span class="sxs-lookup"><span data-stu-id="a1f64-104">You can diagnose the source and obtain a description of application errors by using COM+ and other tools.</span></span> <span data-ttu-id="a1f64-105">Если обнаруживается, что ошибка приложения вызвана COM+, сообщение об ошибке можно интерпретировать при просмотре файла Winerror. h или с помощью служебной программы Microsoft Visual C++ Error.</span><span class="sxs-lookup"><span data-stu-id="a1f64-105">If you discover that the application error is caused by COM+, you can interpret the error message viewing the Winerror.h file or by using the Microsoft Visual C++ error utility.</span></span>

<span data-ttu-id="a1f64-106">Если серверное приложение завершается сбоем или вызывает непредвиденное поведение, необходимо сначала определить, где произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a1f64-106">If your server application is failing or causing unexpected behavior, you must first determine where the error occurred.</span></span> <span data-ttu-id="a1f64-107">Система Просмотр событий отслеживает события приложений, безопасности и системы.</span><span class="sxs-lookup"><span data-stu-id="a1f64-107">The system Event Viewer tracks application, security, and system events.</span></span> <span data-ttu-id="a1f64-108">Здесь записываются многие ошибки "без предупреждения".</span><span class="sxs-lookup"><span data-stu-id="a1f64-108">Many "silent" errors are recorded here.</span></span> <span data-ttu-id="a1f64-109">Однако не все ошибки отображаются в Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="a1f64-109">However, not all errors are shown in the Event Viewer.</span></span>

<span data-ttu-id="a1f64-110">Сначала следует обратиться к журналу приложений в Просмотр событий, чтобы проверить приложение, связанное с сообщением о событии.</span><span class="sxs-lookup"><span data-stu-id="a1f64-110">You should first refer to the application log in the Event Viewer to check the application associated with the event message.</span></span> <span data-ttu-id="a1f64-111">(Так как можно также архивировать журналы событий, можно отвести журнал событий ошибки.) Двойной щелчок записи в журнале активирует страницу **свойств события** , которая предоставляет дополнительные сведения о системном событии.</span><span class="sxs-lookup"><span data-stu-id="a1f64-111">(Because you can also archive event logs, you can track an event history of the error.) Double-clicking an entry in your log activates an **Event Properties** page, which provides further information about the system event.</span></span>

<span data-ttu-id="a1f64-112">Дополнительные сведения об отладке приложения COM+ см. в разделе [Отладка приложений COM+](debugging-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="a1f64-112">For more information on debugging a COM+ application, see [Debugging COM+ Applications](debugging-com--applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1f64-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a1f64-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1f64-114">Изоляция сбоев и политика FailFast</span><span class="sxs-lookup"><span data-stu-id="a1f64-114">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="a1f64-115">Изменение возвращаемых значений COM+</span><span class="sxs-lookup"><span data-stu-id="a1f64-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="a1f64-116">Анализ кодов ошибок</span><span class="sxs-lookup"><span data-stu-id="a1f64-116">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="a1f64-117">Стратегии обработки ошибок в COM+</span><span class="sxs-lookup"><span data-stu-id="a1f64-117">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="a1f64-118">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="a1f64-118">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



