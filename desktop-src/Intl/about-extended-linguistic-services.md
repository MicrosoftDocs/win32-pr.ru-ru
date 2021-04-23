---
description: Расширенные лингвистические службы (ELS) реализованы в виде библиотеки динамической компоновки (DLL), предоставляющей разнообразные функции лингвистической поддержки для текста, определяемого приложением.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: О расширенных лингвистических службах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683741"
---
# <a name="about-extended-linguistic-services"></a><span data-ttu-id="18b7a-103">О расширенных лингвистических службах</span><span class="sxs-lookup"><span data-stu-id="18b7a-103">About Extended Linguistic Services</span></span>

<span data-ttu-id="18b7a-104">Расширенные лингвистические службы (ELS) реализованы в виде библиотеки динамической компоновки (DLL), предоставляющей разнообразные функции лингвистической поддержки для текста, определяемого приложением.</span><span class="sxs-lookup"><span data-stu-id="18b7a-104">Extended Linguistic Services (ELS) is implemented as a dynamic-link library (DLL) that provides a variety of linguistic support functionality for text that the application specifies.</span></span> <span data-ttu-id="18b7a-105">Эта технология включает платформу и подключаемые модули ELS для нескольких предопределенных лингвистических типов служб, доступных для приложения через платформу.</span><span class="sxs-lookup"><span data-stu-id="18b7a-105">The technology includes the ELS platform and plug-ins for several predefined linguistic service types accessible to the application through the platform.</span></span>

> [!Note]  
> <span data-ttu-id="18b7a-106">Модуль ELS устанавливается автоматически вместе с Windows 7 и более поздними версиями.</span><span class="sxs-lookup"><span data-stu-id="18b7a-106">The ELS module is installed automatically with Windows 7 and later.</span></span>

 

## <a name="els-platform"></a><span data-ttu-id="18b7a-107">Платформа ELS</span><span class="sxs-lookup"><span data-stu-id="18b7a-107">ELS Platform</span></span>

<span data-ttu-id="18b7a-108">Платформа ELS — это интерфейс между приложением и службами ELS.</span><span class="sxs-lookup"><span data-stu-id="18b7a-108">The ELS platform is the interface between your application and the ELS services.</span></span> <span data-ttu-id="18b7a-109">Он предоставляет простой способ реализации нескольких видов лингвистической функциональности с помощью одного API, что позволяет приложению получать доступ к определенным службам и использовать их.</span><span class="sxs-lookup"><span data-stu-id="18b7a-109">It provides a simple way to implement several kinds of linguistic functionality through the same API, which allows the application to access and use specific services.</span></span> <span data-ttu-id="18b7a-110">Дополнительные сведения об API см. в разделе [Справочник по расширенным лингвистическим службам.](extended-linguistic-services-reference.md)</span><span class="sxs-lookup"><span data-stu-id="18b7a-110">For more information about the API, see [Extended Linguistic Services Reference.](extended-linguistic-services-reference.md)</span></span>

> [!Note]  
> <span data-ttu-id="18b7a-111">Когда приложение вызывает любую из функций API ELS, платформа выделяет память и ресурсы, необходимые для связи со службами.</span><span class="sxs-lookup"><span data-stu-id="18b7a-111">When the application calls any of the ELS API functions, the platform allocates memory and resources as needed for communication with the services.</span></span> <span data-ttu-id="18b7a-112">Приложение отвечает за вызов платформы еще раз для высвобождения этих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18b7a-112">The application is responsible for calling the platform again to free these resources.</span></span>

 

<span data-ttu-id="18b7a-113">Платформа выполняется внутри области виртуальной памяти приложения, а вся выделенная память является частью этого пространства.</span><span class="sxs-lookup"><span data-stu-id="18b7a-113">The platform runs inside the application virtual memory space, and all allocated memory is part of this space.</span></span> <span data-ttu-id="18b7a-114">Поэтому приложению нужно только связать библиотеку DLL компонента ELS (Elscore.dll) путем связывания с Елскоре. lib или динамически загрузкой Elscore.dll.</span><span class="sxs-lookup"><span data-stu-id="18b7a-114">Thus your application only needs to link to the ELS component DLL (Elscore.dll) by linking to Elscore.lib or by dynamically loading Elscore.dll.</span></span>

## <a name="els-services"></a><span data-ttu-id="18b7a-115">ELS Services</span><span class="sxs-lookup"><span data-stu-id="18b7a-115">ELS Services</span></span>

<span data-ttu-id="18b7a-116">В Windows 7 и более поздних версиях платформа ELS поддерживает только следующие стандартные службы.</span><span class="sxs-lookup"><span data-stu-id="18b7a-116">For Windows 7 and later, the ELS platform supports only the following predefined services.</span></span>

-   [<span data-ttu-id="18b7a-117">Microsoft распознавание языка</span><span class="sxs-lookup"><span data-stu-id="18b7a-117">Microsoft Language Detection</span></span>](microsoft-language-detection.md)
-   [<span data-ttu-id="18b7a-118">Обнаружение сценариев Майкрософт</span><span class="sxs-lookup"><span data-stu-id="18b7a-118">Microsoft Script Detection</span></span>](microsoft-script-detection.md)
-   [<span data-ttu-id="18b7a-119">Службы транслитерации</span><span class="sxs-lookup"><span data-stu-id="18b7a-119">Transliteration services</span></span>](transliteration-services.md)

> [!Note]  
> <span data-ttu-id="18b7a-120">Будущие версии ELS будут поддерживать дополнительные службы, предоставляемые корпорацией Майкрософт или поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="18b7a-120">Future versions of ELS will support additional services provided by Microsoft or service providers.</span></span>

 

<span data-ttu-id="18b7a-121">Каждая служба связана с категорией службы, которая описывает, что делает служба.</span><span class="sxs-lookup"><span data-stu-id="18b7a-121">Each service is associated with a service category describing what the service does.</span></span> <span data-ttu-id="18b7a-122">Категория представлена нелокализованной строкой.</span><span class="sxs-lookup"><span data-stu-id="18b7a-122">The category is represented by a nonlocalizable string.</span></span> <span data-ttu-id="18b7a-123">Он используется приложениями для перечисления доступных служб.</span><span class="sxs-lookup"><span data-stu-id="18b7a-123">It is used by applications to enumerate available services.</span></span> <span data-ttu-id="18b7a-124">Текущие категории служб:</span><span class="sxs-lookup"><span data-stu-id="18b7a-124">The current service categories are:</span></span>

-   <span data-ttu-id="18b7a-125">"Распознавание языка"</span><span class="sxs-lookup"><span data-stu-id="18b7a-125">"Language Detection"</span></span>
-   <span data-ttu-id="18b7a-126">«Определение сценария»</span><span class="sxs-lookup"><span data-stu-id="18b7a-126">"Script Detection"</span></span>
-   <span data-ttu-id="18b7a-127">Латиницу</span><span class="sxs-lookup"><span data-stu-id="18b7a-127">"Transliteration"</span></span>

<span data-ttu-id="18b7a-128">Платформа использует метаданные службы для перечисления служб, запрошенных приложением.</span><span class="sxs-lookup"><span data-stu-id="18b7a-128">The platform uses service metadata to enumerate the services requested by the application.</span></span> <span data-ttu-id="18b7a-129">Такие свойства, как глобальный уникальный идентификатор (GUID) службы, Поддерживаемые языки ввода и вывода и скрипты, а также Категория службы могут использоваться приложением для перечисления требуемых ELS служб.</span><span class="sxs-lookup"><span data-stu-id="18b7a-129">Properties such as the service globally unique identifier (GUID), supported input and output languages and scripts, and the service category can be used by the application to enumerate the desired ELS services.</span></span>

<span data-ttu-id="18b7a-130">Каждая служба ELS реализуется как подключаемый модуль, поддерживаемый библиотекой DLL, которая может быть установлена в операционной системе, чтобы платформа ELS могла обнаружить и использовать ее.</span><span class="sxs-lookup"><span data-stu-id="18b7a-130">Each ELS service is implemented as a plug-in supported by a DLL that can be installed on the operating system so that the ELS platform can detect and use it.</span></span> <span data-ttu-id="18b7a-131">При необходимости службы могут предоставлять собственные подслужбы.</span><span class="sxs-lookup"><span data-stu-id="18b7a-131">Services can expose their own subservices, if required.</span></span>

## <a name="main-els-operations"></a><span data-ttu-id="18b7a-132">Основные операции ELS</span><span class="sxs-lookup"><span data-stu-id="18b7a-132">Main ELS Operations</span></span>

<span data-ttu-id="18b7a-133">В этом разделе описаны основные операции, поддерживаемые платформой ELS.</span><span class="sxs-lookup"><span data-stu-id="18b7a-133">This section describes the main operations supported by the ELS platform.</span></span> <span data-ttu-id="18b7a-134">Платформа поддерживает как синхронные, так и асинхронные режимы вызова.</span><span class="sxs-lookup"><span data-stu-id="18b7a-134">The platform supports both synchronous and asynchronous calling modes.</span></span> <span data-ttu-id="18b7a-135">Режим асинхронного вызова использует пул потоков приложения, чтобы запланировать потоки на обработку запросов.</span><span class="sxs-lookup"><span data-stu-id="18b7a-135">The asynchronous calling mode uses an application thread pool to schedule threads for processing requests.</span></span>

> [!Note]  
> <span data-ttu-id="18b7a-136">Поскольку платформа поддерживает асинхронный режим, ELS Services не требуется реализовывать этот тип функций самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="18b7a-136">Since the platform supports an asynchronous mode, ELS services do not have to implement this type of functionality on their own.</span></span>

 

### <a name="service-enumeration"></a><span data-ttu-id="18b7a-137">Перечисление служб</span><span class="sxs-lookup"><span data-stu-id="18b7a-137">Service Enumeration</span></span>

<span data-ttu-id="18b7a-138">Платформа ELS загружает все службы ELS и управляет ими, делая операцию прозрачной для приложения.</span><span class="sxs-lookup"><span data-stu-id="18b7a-138">The ELS platform loads and manages all ELS services, making operation transparent to the application.</span></span> <span data-ttu-id="18b7a-139">Приложение перечисляет доступные службы путем вызова [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span><span class="sxs-lookup"><span data-stu-id="18b7a-139">The application enumerates the available services by calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span></span> <span data-ttu-id="18b7a-140">Инструкции по программированию см. в разделе [перечисление и освобождение служб](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="18b7a-140">For programming instructions, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="18b7a-141">Рекомендуется по соображениям производительности, чтобы приложение перечислило доступные службы только один раз.</span><span class="sxs-lookup"><span data-stu-id="18b7a-141">It is advisable for performance reasons to have your application enumerate the available services only once.</span></span> <span data-ttu-id="18b7a-142">Платформа ELS снова проверяет службы при следующем перечислении, чтобы убедиться, что результаты перечисления всегда актуальны.</span><span class="sxs-lookup"><span data-stu-id="18b7a-142">The ELS platform checks the services again on the next enumeration to ensure that its enumeration results are always current.</span></span>

 

### <a name="text-recognition"></a><span data-ttu-id="18b7a-143">Распознавание текста</span><span class="sxs-lookup"><span data-stu-id="18b7a-143">Text Recognition</span></span>

<span data-ttu-id="18b7a-144">После перечисления служб приложение вызывает функцию [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) , чтобы использовать определенную службу ELS для отображения любого текстового диапазона входного текста для вывода.</span><span class="sxs-lookup"><span data-stu-id="18b7a-144">After service enumeration, the application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to use a particular ELS service to map any text range of input text to output text.</span></span> <span data-ttu-id="18b7a-145">Примером распознавания текста является использование службы обнаружения языка, которая получает текстовый сегмент и обнаруживает наиболее вероятный язык.</span><span class="sxs-lookup"><span data-stu-id="18b7a-145">An example of text recognition is the use of a language detection service that receives a text segment and detects its most probable language.</span></span>

<span data-ttu-id="18b7a-146">После того как служба распознает текст, [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) возвращает структуру [**\_ \_ контейнера свойств сопоставления**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) , заполненную выходными данными и свойствами, созданными службой.</span><span class="sxs-lookup"><span data-stu-id="18b7a-146">After the service has recognized the text, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns with a [**MAPPING\_PROPERTY\_BAG**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) structure populated with output data and properties produced by the service.</span></span> <span data-ttu-id="18b7a-147">Чтобы избежать утечек памяти, приложение должно освободить контейнер свойств путем вызова [**маппингфрипропертибаг**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) для каждого момента, когда [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) возвращает значение \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="18b7a-147">To avoid memory leaks, the application must free the property bag by calling [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) for each time that the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns S\_OK.</span></span> <span data-ttu-id="18b7a-148">Обычно приложение делает это при завершении использования выходных данных или когда выходные данные больше не нужны, так как входная область текста была изменена, например, изменена или удалена.</span><span class="sxs-lookup"><span data-stu-id="18b7a-148">Usually the application does this either when it finishes using the output data or when the output data is no longer relevant because the input region of text has been modified, for example, edited or deleted.</span></span> <span data-ttu-id="18b7a-149">При освобождении контейнера свойств **маппингфрипропертибаг** возвращает.</span><span class="sxs-lookup"><span data-stu-id="18b7a-149">When the property bag is released, **MappingFreePropertyBag** returns.</span></span>

<span data-ttu-id="18b7a-150">Инструкции по программированию для распознавания текста приведены в статье [запрос распознавания текста](requesting-text-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="18b7a-150">Programming instructions for text recognition are provided in [Requesting Text Recognition](requesting-text-recognition.md).</span></span>

### <a name="service-termination"></a><span data-ttu-id="18b7a-151">Завершение работы службы</span><span class="sxs-lookup"><span data-stu-id="18b7a-151">Service Termination</span></span>

<span data-ttu-id="18b7a-152">Если приложению больше не требуются службы ELS Services, оно вызывает [**маппингфрисервицес**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) перед завершением.</span><span class="sxs-lookup"><span data-stu-id="18b7a-152">When your application no longer requires ELS services, it calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) before it terminates.</span></span> <span data-ttu-id="18b7a-153">Дополнительные сведения см. в разделе [перечисление и освобождение служб](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="18b7a-153">For more information, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

### <a name="versioning"></a><span data-ttu-id="18b7a-154">Управление версиями</span><span class="sxs-lookup"><span data-stu-id="18b7a-154">Versioning</span></span>

<span data-ttu-id="18b7a-155">Будущие версии ELS позволяют обновлять службы ELS.</span><span class="sxs-lookup"><span data-stu-id="18b7a-155">Future versions of ELS will allow the ELS services to be updated.</span></span> <span data-ttu-id="18b7a-156">Приложение сможет проверить номер версии структуры [**\_ \_ сведений о службе сопоставления**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) , чтобы обнаружить изменения в службах.</span><span class="sxs-lookup"><span data-stu-id="18b7a-156">The application will be able to check the version numbers of the [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure to detect any changes in the services.</span></span>

> [!Note]  
> <span data-ttu-id="18b7a-157">Приложение ELS не должно предполагать, что разные версии одной и той же службы могут извлекать точно такие же результаты.</span><span class="sxs-lookup"><span data-stu-id="18b7a-157">Your ELS application should not make the assumption that different versions of the same service can retrieve exactly the same results.</span></span>

 

 

 



