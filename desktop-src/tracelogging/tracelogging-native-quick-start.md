---
title: Трацелоггинг C/C++ Быстрое начало
description: В следующем разделе описаны основные шаги, необходимые для добавления Трацелоггинг в собственный код пользовательского режима.
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: 7be18feb7f372922b7e3b811cd0c9941240e18e3
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2020
ms.locfileid: "103987245"
---
# <a name="tracelogging-cc-quick-start"></a><span data-ttu-id="60f58-103">Трацелоггинг C/C++ Быстрое начало</span><span class="sxs-lookup"><span data-stu-id="60f58-103">TraceLogging C/C++ Quick Start</span></span>

<span data-ttu-id="60f58-104">В следующем разделе описаны основные шаги, необходимые для добавления Трацелоггинг в собственный код пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="60f58-104">The following section describes the basic steps required to add TraceLogging to native user-mode code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="60f58-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="60f58-105">Prerequisites</span></span>

-   <span data-ttu-id="60f58-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="60f58-106">Windows 10</span></span>
-   <span data-ttu-id="60f58-107">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="60f58-107">Microsoft Visual Studio 2013</span></span>
-   <span data-ttu-id="60f58-108">Для создания поставщика пользовательского режима требуется пакет средств разработки программного обеспечения (SDK) Windows 10.</span><span class="sxs-lookup"><span data-stu-id="60f58-108">Windows 10 Software Development Kit (SDK) is required to write a user-mode provider</span></span>
-   <span data-ttu-id="60f58-109">Для создания поставщика в режиме ядра требуется набор драйверов Windows (WDK) для Windows 10.</span><span class="sxs-lookup"><span data-stu-id="60f58-109">Windows Driver Kit (WDK) for Windows 10 is required to write a kernel-mode provider</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60f58-110">Чтобы скомпилировать эти примеры, свяжите advapi32. lib.</span><span class="sxs-lookup"><span data-stu-id="60f58-110">Link advapi32.lib in order to compile these examples.</span></span>

### <a name="simpletraceloggingexampleh"></a><span data-ttu-id="60f58-111">Симплетрацелоггинжексампле. h</span><span class="sxs-lookup"><span data-stu-id="60f58-111">SimpleTraceLoggingExample.h</span></span>

<span data-ttu-id="60f58-112">Этот пример заголовка включает в себя API Трацелоггинг и прямую объявляет маркер поставщика, который будет использоваться для регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="60f58-112">This example header includes the TraceLogging APIs and forward declares the provider handle that will be used to log events.</span></span> <span data-ttu-id="60f58-113">Любой класс, желающий использовать Трацелоггинг, будет включать этот заголовок и может начать ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="60f58-113">Any class that wishes to use TraceLogging will include this header and can then start logging.</span></span>

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

<span data-ttu-id="60f58-114">Файл заголовка содержит Трацелоггингпровидер. h, который определяет собственный API Трацелоггинг.</span><span class="sxs-lookup"><span data-stu-id="60f58-114">The header file includes TraceLoggingProvider.h which defines the native TraceLogging API.</span></span> <span data-ttu-id="60f58-115">Сначала необходимо включить Windows. h, так как он определяет константы, используемые Трацелоггингпровидер. h.</span><span class="sxs-lookup"><span data-stu-id="60f58-115">You must include Windows.h first because it defines constants used by TraceLoggingProvider.h.</span></span>

<span data-ttu-id="60f58-116">Файл заголовка Forward объявляет маркер поставщика `g_hMyComponentProvider` , который передается API-интерфейсам трацелоггинг для регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="60f58-116">The header file forward declares the provider handle `g_hMyComponentProvider` that you will pass to the TraceLogging APIs to log events.</span></span> <span data-ttu-id="60f58-117">Этот маркер должен быть доступен любому коду, который хочет использовать Трацелоггинг.</span><span class="sxs-lookup"><span data-stu-id="60f58-117">This handle needs to be accessible to any code that wishes to use TraceLogging.</span></span>

<span data-ttu-id="60f58-118">[**Трацелоггинг \_ ОБЪЯВЛЕНИЕ \_ provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) — это макрос, который создает `extern const TraceLoggingHProvider` маркер, используя предоставленное вами имя, которое в приведенном выше примере имеет значение `g_hMyComponentProvider` .</span><span class="sxs-lookup"><span data-stu-id="60f58-118">[**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) is a macro that creates an `extern const TraceLoggingHProvider` handle using the name that you provide, which in the example above is `g_hMyComponentProvider`.</span></span> <span data-ttu-id="60f58-119">Фактическая переменная обработчика поставщика будет выделена в файле кода.</span><span class="sxs-lookup"><span data-stu-id="60f58-119">You will allocate the actual provider handle variable in a code file.</span></span>

### <a name="simpletraceloggingexamplecpp"></a><span data-ttu-id="60f58-120">Симплетрацелоггинжексампле. cpp</span><span class="sxs-lookup"><span data-stu-id="60f58-120">SimpleTraceLoggingExample.cpp</span></span>

<span data-ttu-id="60f58-121">В следующем примере регистрируется поставщик, записывается событие и отменяется регистрация поставщика.</span><span class="sxs-lookup"><span data-stu-id="60f58-121">The following example registers the provider, logs an event, and unregisters the provider.</span></span>

```C++
#include "SimpleTraceLoggingExample.h"

    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
}
```

<span data-ttu-id="60f58-122">В приведенном выше примере содержится Симплетрацелоггинжексампле. h, содержащий глобальную переменную поставщика, которую ваш код будет использовать для регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="60f58-122">The example above includes SimpleTraceLoggingExample.h which contains the global provider variable that your code will use to log events.</span></span>

<span data-ttu-id="60f58-123">Макрос [**трацелоггинг \_ определение \_ поставщика**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) выделяет хранилище и определяет переменную обработчика поставщика.</span><span class="sxs-lookup"><span data-stu-id="60f58-123">The [**TRACELOGGING\_DEFINE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) macro allocates storage and defines the provider handle variable.</span></span> <span data-ttu-id="60f58-124">Имя переменной, которое вы указываете в этом макросе, должно совпадать с именем, которое вы использовали в макросе [**трацелоггинг \_ Declare \_ provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="60f58-124">The variable name that you provide to this macro must match the name you used in the [**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) macro in your header file.</span></span> <span data-ttu-id="60f58-125">Этот маркер будет оставаться действительным, пока он находится в области.</span><span class="sxs-lookup"><span data-stu-id="60f58-125">This handle will remain valid as long as it is in scope.</span></span>

### <a name="register-the-provider-handle"></a><span data-ttu-id="60f58-126">Регистрация маркера поставщика</span><span class="sxs-lookup"><span data-stu-id="60f58-126">Register the provider handle</span></span>

<span data-ttu-id="60f58-127">Прежде чем можно будет использовать маркер поставщика для регистрации событий, необходимо вызвать [**трацелоггингрегистер**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) , чтобы зарегистрировать свой маркер поставщика.</span><span class="sxs-lookup"><span data-stu-id="60f58-127">Before you can use the provider handle to log events you must call [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) to register your provider handle.</span></span> <span data-ttu-id="60f58-128">Обычно это делается в Main () или DLLMain (), но может быть выполнено в любое время, пока оно не попытается зарегистрировать событие.</span><span class="sxs-lookup"><span data-stu-id="60f58-128">This is typically done in Main() or DLLMain() but can be done at any time as long as it precedes any attempt to log an event.</span></span> <span data-ttu-id="60f58-129">Если регистрируется событие перед регистрацией обработчика поставщика, ошибка не возникнет, но событие не будет занесено в журнал.</span><span class="sxs-lookup"><span data-stu-id="60f58-129">If you log an event before registering the provider handle, no error will occur but the event will not be logged.</span></span> <span data-ttu-id="60f58-130">Следующий код из приведенного выше примера регистрирует обработчик поставщика.</span><span class="sxs-lookup"><span data-stu-id="60f58-130">The following code from the example above registers the provider handle.</span></span>

```C++
    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
```

### <a name="log-a-tracelogging-event"></a><span data-ttu-id="60f58-131">Регистрация события Трацелоггинг</span><span class="sxs-lookup"><span data-stu-id="60f58-131">Log a Tracelogging event</span></span>

<span data-ttu-id="60f58-132">После регистрации поставщика следующий код записывает в журнал простое событие.</span><span class="sxs-lookup"><span data-stu-id="60f58-132">After the provider is registered, the following code logs a simple event.</span></span>

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

<span data-ttu-id="60f58-133">Макрос [**трацелоггингврите**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) занимает до 99 аргументов и выполняется в виде нескольких инструкций.</span><span class="sxs-lookup"><span data-stu-id="60f58-133">The [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro takes up to ninety-nine arguments and executes as several statements.</span></span> <span data-ttu-id="60f58-134">Это означает, что регистрируемые значения не должны быть временными объектами C++.</span><span class="sxs-lookup"><span data-stu-id="60f58-134">This means that the values being logged should not be C++ temporary objects.</span></span> <span data-ttu-id="60f58-135">Имя события хранится в формате UTF-8.</span><span class="sxs-lookup"><span data-stu-id="60f58-135">The event name is stored in UTF-8 format.</span></span> <span data-ttu-id="60f58-136">Не следует использовать внедренные `null` символы в именах событий и других полях.</span><span class="sxs-lookup"><span data-stu-id="60f58-136">You must not use embedded `null` characters in the event or other field names.</span></span> <span data-ttu-id="60f58-137">Другие ограничения на разрешенные символы отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60f58-137">There are no other limits on permitted characters.</span></span>

<span data-ttu-id="60f58-138">Каждый аргумент, следующий за именем события, должен быть заключен внутри [макроса оболочки трацелоггинг](tracelogging-wrapper-macros.md).</span><span class="sxs-lookup"><span data-stu-id="60f58-138">Each argument following the event name must be wrapped inside of a [TraceLogging Wrapper Macro](tracelogging-wrapper-macros.md).</span></span> <span data-ttu-id="60f58-139">При использовании C++ можно использовать `TraceLoggingValue` макрос оболочки для автоматического определения типа аргумента.</span><span class="sxs-lookup"><span data-stu-id="60f58-139">If you are using C++, you can use the `TraceLoggingValue` wrapper macro to automatically infer the type of the argument.</span></span> <span data-ttu-id="60f58-140">При написании драйвера на языке C необходимо использовать макросы полей для конкретного типа, такие как `TraceLoggingInt32` ,, `TraceLoggingUnicodeString` `TraceLoggingString` и т. д. Макросы-оболочки Трацелоггинг определены в Трацелоггингпровидер. h</span><span class="sxs-lookup"><span data-stu-id="60f58-140">If you are writing your driver in C, you must use type-specific field macros such as `TraceLoggingInt32`, `TraceLoggingUnicodeString`, `TraceLoggingString`, etc. The TraceLogging wrapper macros are defined in TraceLoggingProvider.h</span></span>

<span data-ttu-id="60f58-141">Помимо ведения журнала отдельных событий, события можно группировать по действиям с помощью макросов [**трацелоггингвритеактивити**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) или [**трацелоггингвритестарт**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**трацелоггингвритестоп**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) , находящихся в трацелоггингактивити. h.</span><span class="sxs-lookup"><span data-stu-id="60f58-141">In addition to logging single events you can also group events by activity by using the [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) or [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)/[**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) macros found in TraceLoggingActivity.h.</span></span> <span data-ttu-id="60f58-142">Действия соотносятся к событиям и полезны для сценариев, имеющих начало и конец.</span><span class="sxs-lookup"><span data-stu-id="60f58-142">Activities correlate events and are useful for scenarios that have a beginning and an end.</span></span> <span data-ttu-id="60f58-143">Например, действие можно использовать для измерения сценария, который начинается с момента запуска приложения, включает время, необходимое для отображения экрана-заставки, и завершается, когда исходный экран приложения становится видимым.</span><span class="sxs-lookup"><span data-stu-id="60f58-143">For example, you might use an activity to measure a scenario that starts with the launch of an application, includes the time it takes for the splash screen becomes available, and ends when the initial screen of the application becomes visible.</span></span>

<span data-ttu-id="60f58-144">Действия фиксируют отдельные события и передают другие действия, происходящие между началом и концом этого действия.</span><span class="sxs-lookup"><span data-stu-id="60f58-144">Activities capture single events and nest other activities that occur between the start and end of that activity.</span></span> <span data-ttu-id="60f58-145">Действия имеют область действия для каждого процесса и должны передаваться из потока в поток, чтобы правильно вкладывать многопоточные события.</span><span class="sxs-lookup"><span data-stu-id="60f58-145">Activities have per-process scope and must be passed from thread to thread to properly nest multi-threaded events.</span></span>

<span data-ttu-id="60f58-146">Область действия маркера поставщика строго ограничена модулем (DLL, EXE или SYS), в котором он определен — этот обработчик не должен передаваться в другие DLL-файлы.</span><span class="sxs-lookup"><span data-stu-id="60f58-146">The scope of a provider handle is strictly limited to the module (DLL, EXE, or SYS file) in which it is defined – the handle should not be passed to other DLLs.</span></span> <span data-ttu-id="60f58-147">Если макрос [**трацелоггингврите**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) вызывается в A.DLL с помощью обработчика поставщика, определенного в B.DLL, это может вызвать проблемы.</span><span class="sxs-lookup"><span data-stu-id="60f58-147">If a [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro is invoked in A.DLL using a provider handle defined in B.DLL, it may cause problems.</span></span> <span data-ttu-id="60f58-148">Самый надежный и наиболее эффективный способ удовлетворить это требование — просто напрямую ссылаться на глобальный обработчик поставщика и никогда не передавать его в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="60f58-148">The safest and most efficient way to meet this requirement is to just always directly reference the global provider handle and never pass the provider handle as a parameter.</span></span>

### <a name="unregister-the-provider"></a><span data-ttu-id="60f58-149">Отмена регистрации поставщика</span><span class="sxs-lookup"><span data-stu-id="60f58-149">Unregister the provider</span></span>

<span data-ttu-id="60f58-150">По завершении ведения журнала событий необходимо отменить регистрацию поставщика Трацелоггинг.</span><span class="sxs-lookup"><span data-stu-id="60f58-150">When you are finished logging events you must unregister the TraceLogging provider.</span></span> <span data-ttu-id="60f58-151">Следующий код отменяет регистрацию поставщика.</span><span class="sxs-lookup"><span data-stu-id="60f58-151">The following code unregisters the provider.</span></span>

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a><span data-ttu-id="60f58-152">Совместимость</span><span class="sxs-lookup"><span data-stu-id="60f58-152">Compatibility</span></span>

<span data-ttu-id="60f58-153">В зависимости от конфигурации Трацелоггингпровидер. h может быть обратно совместимой (совместимой с Windows Vista или более поздней версии) или оптимизирована для более поздних версий ОС.</span><span class="sxs-lookup"><span data-stu-id="60f58-153">Depending on its configuration, TraceLoggingProvider.h can be backwards-compatible (compatible with Windows Vista or later), or can be optimized for later OS versions.</span></span> <span data-ttu-id="60f58-154">Трацелоггингпровидер. h использует WINVER (пользовательский режим) и NTDDI_VERSION (режим ядра) для определения того, должен ли он быть совместим с более ранними версиями ОС или оптимизирован для более новых версий ОС.</span><span class="sxs-lookup"><span data-stu-id="60f58-154">TraceLoggingProvider.h uses WINVER (user mode) and NTDDI_VERSION (kernel mode) to determine whether it should be compatible with earlier OS versions or be optimized for newer OS versions.</span></span>

<span data-ttu-id="60f58-155">В пользовательском режиме, если вы включили <Windows. h> перед настройкой WINVER, <Windows. h> устанавливает WINVER в качестве целевой версии ОС по умолчанию для пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="60f58-155">For user-mode, if you include <windows.h> before setting WINVER, <windows.h> sets WINVER to the SDK's default target OS version.</span></span> <span data-ttu-id="60f58-156">Если для WINVER задано значение 0x602 или выше, Трацелоггингпровидер. h оптимизирует свое поведение для Windows 8 (приложение не будет работать в более ранних версиях Windows).</span><span class="sxs-lookup"><span data-stu-id="60f58-156">If WINVER is set to 0x602 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 8 (your app will not run on earlier versions of Windows).</span></span> <span data-ttu-id="60f58-157">Если вы хотите, чтобы программа выполнялась в Vista или Windows 7, обязательно установите для WINVER соответствующее значение, прежде чем включать <Windows. h>.</span><span class="sxs-lookup"><span data-stu-id="60f58-157">If you need your program to run on Vista or Windows 7, be sure to set WINVER to the appropriate value before including <windows.h>.</span></span>

<span data-ttu-id="60f58-158">Аналогичным образом, если включить <WDM. h> перед настройкой NTDDI_VERSION, <WDM. h> устанавливает для NTDDI_VERSION значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="60f58-158">Similarly, if you include <wdm.h> before setting NTDDI_VERSION, <wdm.h> sets NTDDI_VERSION to a default value.</span></span> <span data-ttu-id="60f58-159">Если параметр NTDDI_VERSION имеет значение 0x06040000 или выше, Трацелоггингпровидер. h оптимизирует его поведение для Windows 10 (драйвер не будет работать в более ранних версиях Windows).</span><span class="sxs-lookup"><span data-stu-id="60f58-159">If NTDDI_VERSION is set to 0x06040000 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 10 (your driver will not work on earlier versions of Windows).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="60f58-160">Сводка и дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="60f58-160">Summary and next steps</span></span>

<span data-ttu-id="60f58-161">Сведения о записи и просмотре данных Трацелоггинг с помощью последних внутренних версий средств оценки производительности Windows (WPT) см. в разделе [запись и отображение событий трацелоггинг](tracelogging-record-and-display-tracelogging-events.md).</span><span class="sxs-lookup"><span data-stu-id="60f58-161">To see how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT), see [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md).</span></span>

<span data-ttu-id="60f58-162">Дополнительные примеры C++ Трацелоггинг см. [в статье примеры трацелоггинг в C/c++](tracelogging-c-cpp-tracelogging-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="60f58-162">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for more C++ TraceLogging examples.</span></span>

 

 




