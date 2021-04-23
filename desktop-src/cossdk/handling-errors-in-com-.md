---
description: Наиболее проблематичной частью написания компонентов является работа с возможными ошибками.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Обработка ошибок в COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142967"
---
# <a name="handling-errors-in-com"></a><span data-ttu-id="c95c7-103">Обработка ошибок в COM+</span><span class="sxs-lookup"><span data-stu-id="c95c7-103">Handling Errors in COM+</span></span>

<span data-ttu-id="c95c7-104">Наиболее проблематичной частью написания компонентов является работа с возможными ошибками.</span><span class="sxs-lookup"><span data-stu-id="c95c7-104">The most problematic part of writing components is dealing with possible errors.</span></span> <span data-ttu-id="c95c7-105">Попытка определить, что может быть неправильной, и что делать с ним может быть непростой при лучших условиях.</span><span class="sxs-lookup"><span data-stu-id="c95c7-105">Trying to determine what can go wrong and what to do about it can be challenging under the best conditions.</span></span> <span data-ttu-id="c95c7-106">Распространенные ошибки, которые компонент может проверить на наличие и обработку, не прошли сетевые подключения, ошибки безопасности и сбои, связанные с недостижимыми объектами.</span><span class="sxs-lookup"><span data-stu-id="c95c7-106">Common errors that your component might check for and handle are failed network connections, security errors, and failures associated with unreachable objects.</span></span>

<span data-ttu-id="c95c7-107">Кроме того, можно разработать собственные коды ошибок, чтобы сообщить об ошибках, связанных с интерфейсом, например о нарушении бизнес-правила.</span><span class="sxs-lookup"><span data-stu-id="c95c7-107">Additionally, you can develop your own error codes to report interface-specific errors such as when a business rule has been violated.</span></span>

<span data-ttu-id="c95c7-108">В соответствии с моделью программирования COM+ объект может (и часто) вызывать методы интерфейса для других объектов для выполнения работы.</span><span class="sxs-lookup"><span data-stu-id="c95c7-108">In keeping with the COM+ programming model, an object can (and often does) call interface methods on other objects to perform work.</span></span> <span data-ttu-id="c95c7-109">Поскольку программисты могут писать компоненты на разных языках программирования, COM+ требует, чтобы все механизмы обработки ошибок были нейтральными к языку, например: HRESULTs и [**errorInfo**](errorinfo.md) Collections.</span><span class="sxs-lookup"><span data-stu-id="c95c7-109">Because programmers can write components in different programming languages, COM+ requires that all error-handling mechanisms be language-neutral, for example: HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span>

<span data-ttu-id="c95c7-110">Этот раздел содержит разделы, описанные в следующей таблице, в которых обсуждаются методы обработки ошибок в приложениях COM+, функции COM+, которые влияют на поведение при сбое, а также рекомендации по диагностике ошибок COM+.</span><span class="sxs-lookup"><span data-stu-id="c95c7-110">This section includes topics, described in the following table, that discuss techniques for handling errors in COM+ applications, features in COM+ that affect failure behavior, and suggestions for diagnosing COM+ errors.</span></span>



| <span data-ttu-id="c95c7-111">Раздел</span><span class="sxs-lookup"><span data-stu-id="c95c7-111">Topic</span></span>                                                                                           | <span data-ttu-id="c95c7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c95c7-112">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c95c7-113">Стратегии обработки ошибок в COM+</span><span class="sxs-lookup"><span data-stu-id="c95c7-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)<br/> | <span data-ttu-id="c95c7-114">Содержит список и описывает основные рекомендации по обработке ошибок в COM+, в том числе, когда следует использовать коллекции HRESULTs и [**errorInfo**](errorinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c95c7-114">Lists and describes basic guidelines for handling errors in COM+, including when to use HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span><br/> |
| [<span data-ttu-id="c95c7-115">Изменение возвращаемых значений COM+</span><span class="sxs-lookup"><span data-stu-id="c95c7-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)<br/>               | <span data-ttu-id="c95c7-116">Определяет одно условие, в котором COM+ преобразует стандартное значение HRESULT в код ошибки COM+, прежде чем передать его обратно вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="c95c7-116">Identifies the single condition in which COM+ converts a standard HRESULT to a COM+ error code before passing it back to the caller.</span></span><br/>             |
| [<span data-ttu-id="c95c7-117">Изоляция сбоев и политика FailFast</span><span class="sxs-lookup"><span data-stu-id="c95c7-117">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)<br/>       | <span data-ttu-id="c95c7-118">Показывает, как изоляция сбоев и политика FailFast влияют на поведение COM+.</span><span class="sxs-lookup"><span data-stu-id="c95c7-118">Shows how fault isolation and the failfast policy affect COM+ behavior.</span></span><br/>                                                                          |
| [<span data-ttu-id="c95c7-119">Поиск источника ошибки</span><span class="sxs-lookup"><span data-stu-id="c95c7-119">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)<br/>                 | <span data-ttu-id="c95c7-120">Описывает, как можно диагностировать источник и получить описание ошибок приложения.</span><span class="sxs-lookup"><span data-stu-id="c95c7-120">Describes how you can diagnose the source and obtain a description of application errors.</span></span> <br/>                                                       |
| [<span data-ttu-id="c95c7-121">Анализ кодов ошибок</span><span class="sxs-lookup"><span data-stu-id="c95c7-121">Interpreting Error Codes</span></span>](interpreting-error-codes.md)<br/>                             | <span data-ttu-id="c95c7-122">Определяет предварительный механизм обработки ошибок для Microsoft Visual C++, язык Java и Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c95c7-122">Identifies the predominant error-handling mechanism for Microsoft Visual C++, the Java language, and Microsoft Visual Basic.</span></span> <br/>                    |
| [<span data-ttu-id="c95c7-123">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="c95c7-123">Troubleshooting</span></span>](troubleshooting.md)<br/>                                               | <span data-ttu-id="c95c7-124">Предоставляет дополнительную помощь в диагностике ошибок.</span><span class="sxs-lookup"><span data-stu-id="c95c7-124">Provides additional assistance in diagnosing errors.</span></span><br/>                                                                                             |
| [<span data-ttu-id="c95c7-125">Обращение в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="c95c7-125">Contacting Support</span></span>](contacting-support.md)<br/>                                         | <span data-ttu-id="c95c7-126">Определяет важные сведения по решению проблем, которые следует предоставить при обращении в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c95c7-126">Identifies important problem-solving information you should provide when contacting support.</span></span><br/>                                                     |



 

<span data-ttu-id="c95c7-127">Подробные сведения об обработке ошибок, связанных с различными службами COM+, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="c95c7-127">For detailed information on handling errors associated with various COM+ services, see the following sections:</span></span>

-   [<span data-ttu-id="c95c7-128">Ускорение транзакций путем уведомления корневого объекта</span><span class="sxs-lookup"><span data-stu-id="c95c7-128">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
-   <span data-ttu-id="c95c7-129">[Обработка ошибок](handling-errors-in-queued-components.md) (для компонентов в очереди)</span><span class="sxs-lookup"><span data-stu-id="c95c7-129">[Handling Errors](handling-errors-in-queued-components.md) (for queued components)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c95c7-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c95c7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c95c7-131">Отладка приложений COM+</span><span class="sxs-lookup"><span data-stu-id="c95c7-131">Debugging COM+ Applications</span></span>](debugging-com--applications.md)
</dt> </dl>

 

 




