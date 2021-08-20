---
description: Настройка диспетчера учетных данных
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Настройка диспетчера учетных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3982d3f99cc0d3eb4aab2a0261f0e6b81cdc8a5abb408fc97834950b82b4206f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057948"
---
# <a name="setting-a-credential-manager"></a>Настройка диспетчера учетных данных

Приложение, которое предоставляет учетные данные для сетевого источника, должно выполнять следующие действия.

1.  Реализуйте объект диспетчера учетных данных, который предоставляет интерфейс [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .
2.  Перед созданием сетевого источника создайте новое хранилище свойств.
3.  Задайте свойство [**\_ \_ диспетчера учетных данных мфнетсаурце**](mfnetsource-credential-manager-property.md) в хранилище свойств. Значение свойства является указателем на интерфейс [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .
4.  Передайте указатель на хранилище свойств в сопоставитель источника, как описано в разделе [Настройка источника мультимедиа](configuring-a-media-source.md).

Сетевые источники используют диспетчер учетных данных для получения учетных данных пользователя. Если источнику сети требуются учетные данные для доступа к сетевому ресурсу, он вызывает метод [**имфнеткредентиалманажер:: бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) приложения. Этот вызов запускает асинхронный запрос на получение учетных данных пользователя. Метод **бегинжеткредентиалс** может получить учетные данные из кэша учетных данных или от пользователя. Учетные данные хранятся в *объекте учетных данных*. После завершения операции приложение вызывает интерфейс обратного вызова для уведомления сетевого источника. Сетевой источник вызывает [**имфнеткредентиалманажер:: енджеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) для завершения асинхронной операции.

Так как это асинхронная операция, приложение должно отправить обратный вызов в конце операции. Пошаговые инструкции по написанию асинхронного метода см. в разделе [написание асинхронного метода](writing-an-asynchronous-method.md).

В следующем примере показано, как задать свойство [**\_ \_ диспетчера учетных данных мфнетсаурце**](mfnetsource-credential-manager-property.md) в сетевом источнике.


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Проверка подлинности источника сети](network-source-authentication.md)
</dt> </dl>

 

 



