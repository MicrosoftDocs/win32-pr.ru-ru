---
description: Поддерживаемые протоколы
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Поддерживаемые протоколы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cc5e47bddec9e00fbb62e853db5a492172da84
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468031"
---
# <a name="supported-protocols"></a>Поддерживаемые протоколы

Media Foundation поддерживает следующие протоколы:

-   Протокол передачи данных в реальном времени (RTSP)

    Протокол RTSP используется в основном для потоковой передачи мультимедийного содержимого. Он может использовать UDP или TCP в качестве транспортных протоколов. Протокол UDP наиболее эффективен для доставки содержимого, так как затраты на пропускную способность меньше, чем при использовании протоколов TCP. Хотя протокол TCP гарантирует надежную доставку пакетов, протокол TCP не подходит для цифровых мультимедийных потоков, где эффективное использование пропускной способности является более важным, чем случайные потерянные пакеты.

-   Протокол HTTP

    Протокол HTTP использует протокол TCP и используется веб-серверами. Схема "httpd://" указывает, что источник доступен для загрузки с веб-сервера. Протокол HTTP также используется в случае брандмауэров, которые обычно настроены для приема HTTP-запросов и обычно отклоняют другие протоколы потоковой передачи.

Приложение может получать протоколы, поддерживаемые Media Foundation с помощью интерфейса [**имфнетсчемехандлерконфиг**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) . Для этого приложение должно сначала получить количество протоколов, вызвав [**имфнетсчемехандлерконфиг:: жетнумберофсуппортедпротоколс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) , а затем получить тип протокола на основе индекса, вызвав [**Имфнетсчемехандлерконфиг:: GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype). Этот метод возвращает одно из значений, определенных в перечислении [**\_ \_ типа протокола мфнетсаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .

Приложение также может получить схемы, поддерживаемые распознавателем источников, вызвав функцию [**мфжетсуппортедсчемес**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) .

## <a name="protocol-rollover"></a>Смена протокола

Если в приложении в качестве схемы URL-адреса указано "mms://", сопоставитель источника выполняет операцию *смены протокола* . В этом процессе сопоставитель источника определяет оптимальный протокол, используемый сетевым источником для получения содержимого. Как правило, для потоковой передаче мультимедиа протокол RTSP с UDP (РТСПУ) более эффективен, чем HTTP. Однако если содержимое размещено на веб-сервере, лучше выбрать HTTP.

Смена протокола также может возникать, если попытка использования протокола, указанного в схеме URL-адреса, завершается ошибкой. Например, протокол может завершиться ошибкой, если брандмауэр блокирует пакеты UDP. В этом случае сопоставитель источника переключается на HTTP.

Переключение протокола не применяется, если схема URL-адресов содержит конкретный протокол, например "rtspu://". Кроме того, смена не выполняется в случае сбоя проверки подлинности или превышения сервером ограничения на количество клиентских подключений. Рекомендуется, чтобы приложения указали схему "mms://" и позволяли распознавателю источников выбрать оптимальный протокол для сценария.

В следующей таблице приводится порядок переключения.




| Разрешенные схемы | Порядок переключения протоколов | 
|-----------------|-------------------------|
| mms://или rtsp:// | Быстрый кэш включен:<br /><ol><li>Протокол RTSP с TCP (RTSP)<br /></li><li>RTSP с UDP (РТСПУ)<br /></li><li>Потоковая передача HTTP<br /></li><li>Загрузка HTTP (HTTPD)<br /></li></ol>Быстрый кэш отключен:<br /><ol><li>ртспу<br /></li><li>RTSP<br /></li><li>Потоковая передача HTTP<br /></li><li>Загрузка HTTP<br /></li></ol> | 
| rtspu:// | ртспу | 
| rtspt:// | RTSP | 
| https:// | <ol><li>HTTP<br /></li><li>HTTPD<br /></li></ol> | 
| httpd:// | HTTPD | 




 

## <a name="retrieving-the-current-protocol"></a>Получение текущего протокола

После операции переключения протокола сетевой источник может использовать протокол, отличный от указанного приложением в схеме URL-адреса. Результат переключения протокола будет доступен для приложения после того, как источник сети установит подключение к серверу мультимедиа.

Чтобы получить протокол и транспорт, которые используются для получения содержимого, приложение может получить значения свойств [ \_ протокола мфнетсаурце](mfnetsource-protocol-property.md) и свойства [ \_ Transport мфнетсаурце](mfnetsource-transport-property.md) объекта **ипропертисторе** из сетевого источника.

В следующем коде показано, как получить эти значения.


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



В предыдущем примере кода **ипропертисторе:: GetValue** получает \_ значение протокола мфнетсаурце, которое является членом перечисления [**\_ \_ типа протокола мфнетсаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) . Для \_ транспорта мфнетсаурце значение является членом перечисления [**\_ \_ типа транспорта мфнетсаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .

Кроме того, приложение может получить те же значения с помощью \_ службы статистики мфнетсаурце \_ . Чтобы использовать эту службу, приложение может вызвать функцию [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) для получения хранилища свойств из сетевого источника. Это хранилище свойств содержит статистику сети в свойстве [ \_ статистики мфнетсаурце](mfnetsource-statistics-property.md) . Значения протокола и транспорта можно получить, указав \_ идентификатор протокола мфнетсаурце \_ и \_ идентификатор транспорта мфнетсаурце \_ , определенные в перечислении [**\_ \_ идентификаторов мфнетсаурце Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) . В следующем коде показано, как получить значения протокола и транспорта с помощью \_ службы статистики мфнетсаурце \_ .


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a>Включение и отключение протоколов

Приложение может настроить источник сети таким образом, чтобы определенные протоколы пропускались в процессе переключения. Для этого свойства источника сети используются для отключения конкретных протоколов. В следующей таблице показаны свойства и протоколы, которыми они управляют.



| Свойство                                                                    | Описание                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [МФНЕТСАУРЦЕ \_ включить \_ http](mfnetsource-enable-http-property.md)           | Включает или отключает протоколы HTTP и HTTPD.         |
| [МФНЕТСАУРЦЕ \_ Включение \_ RTSP](mfnetsource-enable-rtsp-property.md)           | Включает или отключает РТСПУ и RTSP.        |
| [МФНЕТСАУРЦЕ \_ включить \_ TCP](mfnetsource-enable-tcp-property.md)             | Включает или отключает протокол RTSP.                  |
| [МФНЕТСАУРЦЕ \_ включить \_ UDP](mfnetsource-enable-udp-property.md)             | Включает или отключает РТСПУ.                  |
| [МФНЕТСАУРЦЕ \_ включить \_ скачивание](mfnetsource-enable-download-property.md)   | Включает или отключает HTTPD.                  |
| [МФНЕТСАУРЦЕ \_ включить \_ потоковую передачу](mfnetsource-enable-streaming-property.md) | Включает или отключает РТСПУ, RTSP и HTTP. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




