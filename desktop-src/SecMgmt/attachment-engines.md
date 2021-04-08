---
description: Подсистема вложений — это библиотека DLL, которая обрабатывает запросы конфигурации и анализа, зависящие от конкретной службы.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Модули вложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911580"
---
# <a name="attachment-engines"></a><span data-ttu-id="78a87-103">Модули вложений</span><span class="sxs-lookup"><span data-stu-id="78a87-103">Attachment Engines</span></span>

<span data-ttu-id="78a87-104">Подсистема вложений — это библиотека DLL, которая обрабатывает запросы конфигурации и анализа, зависящие от конкретной службы.</span><span class="sxs-lookup"><span data-stu-id="78a87-104">An attachment engine is a DLL that handles service-specific configuration and analysis requests.</span></span>

<span data-ttu-id="78a87-105">Пользователь выполняет зависящую от службы конфигурацию и запрос на анализ с помощью расширения оснастки вложения.</span><span class="sxs-lookup"><span data-stu-id="78a87-105">The user makes a service-specific configuration and analysis request using the attachment snap-in extension.</span></span> <span data-ttu-id="78a87-106">Затем этот запрос передается через оснастки настройки безопасности в общую подсистему настройки безопасности, которая, в свою очередь, передает обработку соответствующему подсистеме, зависящей от службы.</span><span class="sxs-lookup"><span data-stu-id="78a87-106">This request is then passed through the Security Configuration snap-ins to the general Security Configuration Engine, which in turn passes the service-specific processing to the appropriate attachment engine.</span></span> <span data-ttu-id="78a87-107">Затем подсистема вложений подключается к службе и изменяет ее конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="78a87-107">The attachment engine then connects to the service and changes its configuration.</span></span> <span data-ttu-id="78a87-108">Иными словами, подсистема вложений предоставляет серверную обработку, поддерживающую расширение оснастки вложения.</span><span class="sxs-lookup"><span data-stu-id="78a87-108">In other words, the attachment engine provides the back-end processing that supports the attachment snap-in extension.</span></span>

<span data-ttu-id="78a87-109">Подсистема вложений должна реализовывать следующие три функции:</span><span class="sxs-lookup"><span data-stu-id="78a87-109">An attachment engine must implement the following three functions:</span></span>

-   <span data-ttu-id="78a87-110">[**Сцесвкаттачментанализе**](scesvcattachmentanalyze.md), который рассчитывает разницу между конфигурацией службы и конфигурацией, хранящейся в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="78a87-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), which computes the difference between the service's configuration and the configuration stored in the security database.</span></span> <span data-ttu-id="78a87-111">Различия записываются в базу данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="78a87-111">The differences are written to the security database.</span></span>
-   <span data-ttu-id="78a87-112">[**Сцесвкаттачментконфиг**](scesvcattachmentconfig.md), который настраивает службу, как указано в пользовательском интерфейсе оснастки.</span><span class="sxs-lookup"><span data-stu-id="78a87-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), which configures the service as specified in the snap-in user interface.</span></span>
-   <span data-ttu-id="78a87-113">[**Сцесвкаттачментупдате**](scesvcattachmentupdate.md), который обновляет базовую конфигурацию и анализ конфигурации для службы в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="78a87-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), which updates the base configuration and configuration analysis for the service in the security database.</span></span>

<span data-ttu-id="78a87-114">Для упрощения реализации предыдущих функций набор средств настройки безопасности предоставляет функции и структуры поддержки, которые приложение может использовать для запроса и настройки сведений в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="78a87-114">To simplify implementation of the preceding functions, the Security Configuration tool set provides support functions and structures that your application can use to query and set information in the security database.</span></span> <span data-ttu-id="78a87-115">Дополнительные сведения см. в разделе [функции обратного вызова вложений](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="78a87-115">For more information, see [Attachment Callback Functions](management-functions.md).</span></span>

<span data-ttu-id="78a87-116">При создании библиотеки DLL подсистемы вложений необходимо установить ее, а затем зарегистрировать в подсистеме настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="78a87-116">When you create an attachment engine DLL, you must install it and then register it with the Security Configuration Engine.</span></span> <span data-ttu-id="78a87-117">Чтобы зарегистрировать библиотеку DLL, добавьте в реестр конкретный ключ.</span><span class="sxs-lookup"><span data-stu-id="78a87-117">To register the DLL, you add a specific key to the registry.</span></span> <span data-ttu-id="78a87-118">При запуске подсистема настройки безопасности проверяет реестр и загружает все зарегистрированные библиотеки DLL подсистемы вложений.</span><span class="sxs-lookup"><span data-stu-id="78a87-118">When the Security Configuration Engine starts, it checks the registry and loads all registered attachment engine DLLs.</span></span> <span data-ttu-id="78a87-119">Затем он передает специфические для службы запросы конфигурации и анализа соответствующему подсистеме вложений.</span><span class="sxs-lookup"><span data-stu-id="78a87-119">It then passes service-specific configuration and analysis requests to the appropriate attachment engine.</span></span> <span data-ttu-id="78a87-120">Стандартные запросы на настройку и анализ, не зависящие от службы, обрабатываются модулем настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="78a87-120">Standard configuration and analysis requests, those that are not service-specific, are handled by the Security Configuration Engine.</span></span>

 

 



