---
title: Запись и Просмотр событий Трацелоггинг
description: записывайте события трацелоггинг с помощью средства записи производительности Windows (звч) и просматривайте их с помощью анализатора производительности Windows (WPA).
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c77c1a1759988252f57c1ec54dca77cffaa21832878ead6ba8a827df3329fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966548"
---
# <a name="record-and-view-tracelogging-events"></a>Запись и Просмотр событий Трацелоггинг

записывайте события трацелоггинг с помощью средства записи производительности Windows (звч) и просматривайте их с помощью анализатора производительности Windows (WPA).

## <a name="prerequisites"></a>Предварительные требования

-   Windows 10,
-   Windows 10ная версия Windows средства записи производительности (звч) и Windows 10ная версия Windows performance Analyzer (WPA), которая входит в состав комплекта Windows® для оценки и развертывания (Windows ADK).

> [!IMPORTANT]
> трассировки, захваченные с помощью трацелоггинг, должны быть записаны с помощью Windows 10 версии Windows средства записи производительности и просматриваются с помощью Windows 10 версии Windows performance Analyzer. если вы не можете записать или декодировать события, убедитесь, что используется Windows 10ная версия средств.

 

### <a name="1-capture-trace-data-with-wpr"></a>1. запись данных трассировки с помощью ЗВЧ

чтобы записать трассировку Windows Phone, см. раздел capture трацелоггинг events on Windows Phone ниже.

создайте профиль средства записи производительности Windows (впрп), чтобы можно было использовать звч для захвата событий трацелоггинг.

**Создайте. Файл ВПРП**

1.  Используйте следующий пример ВПРП с примером машинного кода в [Трацелоггинг C/C++ быстрое начало](tracelogging-native-quick-start.md) или управляемом примере в [управляемом быстрое начало трацелоггинг](tracelogging-managed-quick-start.md). Если вы регистрируете события из собственного поставщика, замените `TODO` разделы соответствующими значениями для поставщика.

    > \[! Существенно\]  

     

    Если вы используете быстрый запуск Трацелоггинг C/C++, укажите идентификатор GUID поставщика в `Name` атрибуте `<EventProvider>` элемента. Например: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`. Если вы используете быстрое начало работы с управляемыми Трацелоггинг, укажите имя поставщика, которое предшествует " \* " в `Name` атрибуте `<EventProvider />` элемента. Например, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.

    Пример файла ВПРП.

    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <!-- TODO: 
    1. Find and replace "SimpleTraceLoggingProvider" with the name of your provider.
    2. See TODO below to update GUID for your event provider
    -->
    <WindowsPerformanceRecorder Version="1.0" Author="Microsoft Corporation" Copyright="Microsoft Corporation" Company="Microsoft Corporation">
      <Profiles>
        <EventCollector Id="EventCollector_SimpleTraceLoggingProvider" Name="SimpleTraceLoggingProvider">
          <BufferSize Value="64" />
          <Buffers Value="4" />
        </EventCollector>

        <!-- TODO: 
     1. Update Name attribute in EventProvider xml element with your provider GUID, eg: Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833". Or
        if you specify an EventSource C# provider or call TraceLoggingRegister(...) without a GUID, use star (*) before your provider
        name, eg: Name="*MyEventSourceProvider" which will enable your provider appropriately.  
     2. This sample lists one EventProvider xml element and references it in a Profile with EventProviderId xml element. 
        For your component wprp, enable the required number of providers and fix the Profile xml element appropriately
    -->
        <EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="*SimpleTraceLoggingProvider" />
        
        <Profile Id="SimpleTraceLoggingProvider.Verbose.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" LoggingMode="File" DetailLevel="Verbose">
          <Collectors>
            <EventCollectorId Value="EventCollector_SimpleTraceLoggingProvider">
              <EventProviders>
                <!-- TODO:
     1. Fix your EventProviderId with Value same as the Id attribute on EventProvider xml element above
    -->
                <EventProviderId Value="EventProvider_SimpleTraceLoggingProvider" />
              </EventProviders>
            </EventCollectorId>
          </Collectors>
        </Profile>

        <Profile Id="SimpleTraceLoggingProvider.Light.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="File" DetailLevel="Light" />
        <Profile Id="SimpleTraceLoggingProvider.Verbose.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Verbose" />
        <Profile Id="SimpleTraceLoggingProvider.Light.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Light" />

      </Profiles>
    </WindowsPerformanceRecorder>
    
    ```

    

2.  Сохраните файл с расширением. Расширение имени файла ВПРП.
3.  Запустите запись с помощью инструкции ЗВЧ в окне командной строки с повышенными привилегиями (Запуск от имени администратора).

    **<path to wpr>\\wpr.exe Женералпрофиле-Start Трацелоггингпровидер. впрп**

    > \[! Советы\]  
    > В общих целях профилирования можно также добавить **– Start женералпрофиле** в командную строку wpr.exe для записи системных событий вместе с событиями от поставщика. Если вы хотите собрать только события, пропустите параметр **-Start женералпрофиле**.

     

4.  Запустите приложение, содержащее события.
5.  Останавливает запись трассировки.

    **<path to wpr>\\wpr.exe — описание Трацекаптурефиле. ETL**

    > \[! Советы\]  
    > Если вы добавили- **Start женералпрофиле** для сбора системных событий, добавьте **wpr.exe** **женералпрофиле** в командную строку выше.

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a>2. запись событий Трацелоггинг в Windows Phone

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  Запустите tracelog, чтобы записать события от поставщика.

    **кмдд tracelog — запустить тест-f c: \\ Test. ETL-GUID \# провидергуид**

2.  Запустите сценарий тестирования для записи событий в журнал.
3.  Останавливает запись трассировки.

    **кмдд tracelog — завершение теста**

4.  Объедините результаты трассировки системы с результатами трассировки.

    **кмдд XPerf — слияние c: \\ Test. ETL c: \\ тестмержед. ETL**

5.  Получите объединенный файл журнала.

    **жетд c: \\ тестмержед. ETL**

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a>3. просмотр данных трацелоггинг с помощью анализатора производительности Windows.

В настоящее время WPA является единственным средством просмотра, которое можно использовать для просмотра файлов трассировки Трацелоггинг (ETL).

1.  Запустите WPA.

    **<path to wpr>\\wpa.exe Трацелоггингресултс. ETL**

2.  Загрузите файл трассировки (ETL), указанный в приведенной выше команде wpa.exe, например Трацелоггингресултс. ETL.
3.  Просмотр событий поставщика. в обозревателе Graph WPA разверните узел **активность системы**.
4.  Дважды щелкните на панели **Общие события** , чтобы просмотреть события на панели **анализ** .

    ![развернуть общие события](images/expandsystemactivity.png)

5.  В области анализ найдите события от поставщика, чтобы убедиться, что Трацелоггинг работает.

    В столбце **имя поставщика** таблицы **Универсальные события** найдите и выберите строку с именем поставщика.

    Если у вас есть несколько поставщиков для сортировки, щелкните заголовок столбца, чтобы выполнить сортировку по имени столбца, что может облегчить поиск поставщика.

    При обнаружении поставщика щелкните правой кнопкой мыши имя и выберите пункт **Фильтр для выбора**.

    ![Фильтр выбора для поставщика](images/filtertoselection.png)

    Событие для Симплетрацелоггингпровидер и его значение появится в нижней области окна анализ. Разверните имя поставщика, чтобы просмотреть события.

    ![Просмотр события из симплетрацелоггингпровидер](images/eventview.png)

    дополнительные сведения об использовании WPA см. в разделе [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).

## <a name="summary-and-next-steps"></a>Сводка и дальнейшие действия

Процесс записи и просмотра событий ETW с использованием ЗВЧ и WPA применяется одинаково хорошо для Трацелоггинг событий.

Дополнительные примеры Трацелоггинг см. [в статье примеры в C/C++ трацелоггинг](tracelogging-c-cpp-tracelogging-examples.md) .

 

 