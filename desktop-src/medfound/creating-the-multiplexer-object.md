---
description: Создание объекта мультиплексора
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Создание объекта мультиплексора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262810"
---
# <a name="creating-the-multiplexer-object"></a>Создание объекта мультиплексора

Мультиплексор ASF — это объект слоя Вмконтаинер, который работает с [объектом данных ASF](asf-file-structure.md) и дает приложению возможность создавать пакеты данных ASF для потоков мультимедиа.

Объект мультиплексора предоставляет интерфейс [**имфасфмултиплексер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) . Чтобы создать мультиплексор, вызовите [**мфкреатеасфмултиплексер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer). Эта функция возвращает указатель на пустой объект. Если приложение записывает новый ASF-файл, приложение должно инициализировать мультиплексор с помощью объекта Контентинфо. Для этого вызовите метод [**имфасфмултиплексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize). Указанный объект Контентинфо представляет объект заголовка ASF нового файла. Сведения о создании и инициализации объекта Контентинфо для нового файла см. [в разделе Инициализация объекта Контентинфо нового ASF-файла](initializing-the-contentinfo-object-of-a-new-asf-file.md).

Метод [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) анализирует объект контентинфо, чтобы получить сведения о конфигурации потока, такие как число потоков, размер пакета, предпроход. Кроме того, мультиплексору также могут потребоваться параметры сегмента утечки и единицы расширения полезных данных. Эти сведения необходимы для создания пакетов данных, соответствующих требованиям, определенным в объекте заголовка ASF. Метод **Initialize** настраивает мультиплексор на основе типа носителя и параметров конфигурации потоков. Например, если поток настроен на наличие расширений полезных данных (см. раздел [Создание и настройка потоков ASF](creating-and-configuring-asf-streams.md)), а затем мультиплексор настроен на добавление этих значений к созданным пакетам данных.

Метод [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) также получает маркер для начального объекта данных, который был создан во время создания объекта контентинфо для записи. При создании пакета данных мультиплексор добавляет пакеты в объект данных и соответствующим образом обновляет его. После того как мультиплексор создаст все пакеты данных, он обновляет указанный объект Контентинфо, чтобы были обновлены определенные значения, например количество пакетов данных.

В следующем примере кода показано, как создать мультиплексор и инициализировать его с помощью объекта Контентинфо.


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



Сведения о функции, используемой в законченном приложении, см. в разделе [учебник. копирование потоков ASF из одного файла в другой](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a>Параметры инициализации мультиплексора и утечек сегментов

Метод [**имфасфмултиплексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) настраивает мультиплексор для определения потока данных контейнера утечки. Чтобы настроить эти параметры, убедитесь, что для указанного объекта Контентинфо установлены следующие значения свойств. Дополнительные сведения об установке этих свойств см. [в разделе Задание свойств в объекте контентинфо](setting-properties-in-the-contentinfo-object.md).

-   [**Мфпкэй \_ Свойство автоматической \_ настройки \_ скорости асфмедиасинк**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) : указывает, нужно ли мультиплексору автоматически настраивать скорость потока данных, чтобы обеспечить его в контейнере утечки. Этот параметр может быть изменен приложением путем вызова [**имфасфмултиплексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) и передачи флага **\_ \_ авторегулировки скорости \_ для мультиплексора мфасф** .

-   [**Мфпкэй \_ \_Базовое свойство \_ сендтиме асфмедиасинк**](mfpkey-asfmediasink-base-sendtime-property.md) : время отправки указывает, когда будут освобождены полезные данные в сегменте утечки. Время отправки должно быть больше или равно времени презентации, поскольку полезные данные должны иметь время для получения назначения до времени презентации.

    Это значение свойства является первым временем отправки. Мультиплексор использует это значение для вычисления последующего времени отправки, чтобы обеспечить непрерывную передачу данных через контейнер. Если для мультиплексора установлен флаг **\_ авторегулировки скорости мфасф мультиплексора \_ \_** , то мультиплексор будет корректировать скорость потока, чтобы полезные данные отправлялись, когда окно буфера близко к заполнению. Если флаг не установлен, мультиплексор не сможет создать пакеты данных из-за переполнения полосы пропускания.

Мультиплексор получает сведения о конфигурации потока из профиля ASF, связанного с объектом Контентинфо, указанным в методе [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) . Сведения о конфигурации потока включают параметры контейнера с утечкой. Это значение требуется мультиплексору для создания пакетов данных.

Чтобы указать параметры контейнера с утечкой, установите значения в атрибуте [**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) в объекте конфигурации потока, который представляет поток в профиле. Чтобы использовать значение окна буфера, используемое кодировщиком, вызовите [**ивмкодеклеакибуккет:: жетбуфферсизебитс**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md). Фактическое значение окна буфера известно только после установки типа выходного носителя кодировщика. Сведения о настройке типа выходных данных мультимедиа см. в разделе [Согласование типа носителя в кодировщике](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Значения сегментов утечки, используемые кодировщиком, могут отличаться в объекте Контентинфо, предоставленном профилем ASF, который использовался для создания мультиплексора.

 

Метод [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) обновляет объект контентинфо, чтобы правильные значения отражались в окончательном ОБЪЕКТЕ заголовка ASF.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Мультиплексор ASF](asf-multiplexer.md)
</dt> <dt>

[Создание новых пакетов данных ASF](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
