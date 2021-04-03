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
# <a name="tracelogging-cc-quick-start"></a>Трацелоггинг C/C++ Быстрое начало

В следующем разделе описаны основные шаги, необходимые для добавления Трацелоггинг в собственный код пользовательского режима.

## <a name="prerequisites"></a>Предварительные условия

-   Windows 10
-   Microsoft Visual Studio 2013
-   Для создания поставщика пользовательского режима требуется пакет средств разработки программного обеспечения (SDK) Windows 10.
-   Для создания поставщика в режиме ядра требуется набор драйверов Windows (WDK) для Windows 10.

> [!IMPORTANT]
> Чтобы скомпилировать эти примеры, свяжите advapi32. lib.

### <a name="simpletraceloggingexampleh"></a>Симплетрацелоггинжексампле. h

Этот пример заголовка включает в себя API Трацелоггинг и прямую объявляет маркер поставщика, который будет использоваться для регистрации событий. Любой класс, желающий использовать Трацелоггинг, будет включать этот заголовок и может начать ведение журнала.

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

Файл заголовка содержит Трацелоггингпровидер. h, который определяет собственный API Трацелоггинг. Сначала необходимо включить Windows. h, так как он определяет константы, используемые Трацелоггингпровидер. h.

Файл заголовка Forward объявляет маркер поставщика `g_hMyComponentProvider` , который передается API-интерфейсам трацелоггинг для регистрации событий. Этот маркер должен быть доступен любому коду, который хочет использовать Трацелоггинг.

[**Трацелоггинг \_ ОБЪЯВЛЕНИЕ \_ provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) — это макрос, который создает `extern const TraceLoggingHProvider` маркер, используя предоставленное вами имя, которое в приведенном выше примере имеет значение `g_hMyComponentProvider` . Фактическая переменная обработчика поставщика будет выделена в файле кода.

### <a name="simpletraceloggingexamplecpp"></a>Симплетрацелоггинжексампле. cpp

В следующем примере регистрируется поставщик, записывается событие и отменяется регистрация поставщика.

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

В приведенном выше примере содержится Симплетрацелоггинжексампле. h, содержащий глобальную переменную поставщика, которую ваш код будет использовать для регистрации событий.

Макрос [**трацелоггинг \_ определение \_ поставщика**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) выделяет хранилище и определяет переменную обработчика поставщика. Имя переменной, которое вы указываете в этом макросе, должно совпадать с именем, которое вы использовали в макросе [**трацелоггинг \_ Declare \_ provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) в файле заголовка. Этот маркер будет оставаться действительным, пока он находится в области.

### <a name="register-the-provider-handle"></a>Регистрация маркера поставщика

Прежде чем можно будет использовать маркер поставщика для регистрации событий, необходимо вызвать [**трацелоггингрегистер**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) , чтобы зарегистрировать свой маркер поставщика. Обычно это делается в Main () или DLLMain (), но может быть выполнено в любое время, пока оно не попытается зарегистрировать событие. Если регистрируется событие перед регистрацией обработчика поставщика, ошибка не возникнет, но событие не будет занесено в журнал. Следующий код из приведенного выше примера регистрирует обработчик поставщика.

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

### <a name="log-a-tracelogging-event"></a>Регистрация события Трацелоггинг

После регистрации поставщика следующий код записывает в журнал простое событие.

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

Макрос [**трацелоггингврите**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) занимает до 99 аргументов и выполняется в виде нескольких инструкций. Это означает, что регистрируемые значения не должны быть временными объектами C++. Имя события хранится в формате UTF-8. Не следует использовать внедренные `null` символы в именах событий и других полях. Другие ограничения на разрешенные символы отсутствуют.

Каждый аргумент, следующий за именем события, должен быть заключен внутри [макроса оболочки трацелоггинг](tracelogging-wrapper-macros.md). При использовании C++ можно использовать `TraceLoggingValue` макрос оболочки для автоматического определения типа аргумента. При написании драйвера на языке C необходимо использовать макросы полей для конкретного типа, такие как `TraceLoggingInt32` ,, `TraceLoggingUnicodeString` `TraceLoggingString` и т. д. Макросы-оболочки Трацелоггинг определены в Трацелоггингпровидер. h

Помимо ведения журнала отдельных событий, события можно группировать по действиям с помощью макросов [**трацелоггингвритеактивити**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) или [**трацелоггингвритестарт**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**трацелоггингвритестоп**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) , находящихся в трацелоггингактивити. h. Действия соотносятся к событиям и полезны для сценариев, имеющих начало и конец. Например, действие можно использовать для измерения сценария, который начинается с момента запуска приложения, включает время, необходимое для отображения экрана-заставки, и завершается, когда исходный экран приложения становится видимым.

Действия фиксируют отдельные события и передают другие действия, происходящие между началом и концом этого действия. Действия имеют область действия для каждого процесса и должны передаваться из потока в поток, чтобы правильно вкладывать многопоточные события.

Область действия маркера поставщика строго ограничена модулем (DLL, EXE или SYS), в котором он определен — этот обработчик не должен передаваться в другие DLL-файлы. Если макрос [**трацелоггингврите**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) вызывается в A.DLL с помощью обработчика поставщика, определенного в B.DLL, это может вызвать проблемы. Самый надежный и наиболее эффективный способ удовлетворить это требование — просто напрямую ссылаться на глобальный обработчик поставщика и никогда не передавать его в качестве параметра.

### <a name="unregister-the-provider"></a>Отмена регистрации поставщика

По завершении ведения журнала событий необходимо отменить регистрацию поставщика Трацелоггинг. Следующий код отменяет регистрацию поставщика.

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>Совместимость

В зависимости от конфигурации Трацелоггингпровидер. h может быть обратно совместимой (совместимой с Windows Vista или более поздней версии) или оптимизирована для более поздних версий ОС. Трацелоггингпровидер. h использует WINVER (пользовательский режим) и NTDDI_VERSION (режим ядра) для определения того, должен ли он быть совместим с более ранними версиями ОС или оптимизирован для более новых версий ОС.

В пользовательском режиме, если вы включили <Windows. h> перед настройкой WINVER, <Windows. h> устанавливает WINVER в качестве целевой версии ОС по умолчанию для пакета SDK. Если для WINVER задано значение 0x602 или выше, Трацелоггингпровидер. h оптимизирует свое поведение для Windows 8 (приложение не будет работать в более ранних версиях Windows). Если вы хотите, чтобы программа выполнялась в Vista или Windows 7, обязательно установите для WINVER соответствующее значение, прежде чем включать <Windows. h>.

Аналогичным образом, если включить <WDM. h> перед настройкой NTDDI_VERSION, <WDM. h> устанавливает для NTDDI_VERSION значение по умолчанию. Если параметр NTDDI_VERSION имеет значение 0x06040000 или выше, Трацелоггингпровидер. h оптимизирует его поведение для Windows 10 (драйвер не будет работать в более ранних версиях Windows).

## <a name="summary-and-next-steps"></a>Сводка и дальнейшие действия

Сведения о записи и просмотре данных Трацелоггинг с помощью последних внутренних версий средств оценки производительности Windows (WPT) см. в разделе [запись и отображение событий трацелоггинг](tracelogging-record-and-display-tracelogging-events.md).

Дополнительные примеры C++ Трацелоггинг см. [в статье примеры трацелоггинг в C/c++](tracelogging-c-cpp-tracelogging-examples.md) .

 

 




