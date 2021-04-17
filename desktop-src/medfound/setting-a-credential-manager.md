---
description: Настройка диспетчера учетных данных
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Настройка диспетчера учетных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711397"
---
# <a name="setting-a-credential-manager"></a><span data-ttu-id="7b2f3-103">Настройка диспетчера учетных данных</span><span class="sxs-lookup"><span data-stu-id="7b2f3-103">Setting a Credential Manager</span></span>

<span data-ttu-id="7b2f3-104">Приложение, которое предоставляет учетные данные для сетевого источника, должно выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-104">An application that provides credentials to the network source must do the following:</span></span>

1.  <span data-ttu-id="7b2f3-105">Реализуйте объект диспетчера учетных данных, который предоставляет интерфейс [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="7b2f3-105">Implement a credential manager object that exposes the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
2.  <span data-ttu-id="7b2f3-106">Перед созданием сетевого источника создайте новое хранилище свойств.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-106">Before you create the network source, create a new property store.</span></span>
3.  <span data-ttu-id="7b2f3-107">Задайте свойство [**\_ \_ диспетчера учетных данных мфнетсаурце**](mfnetsource-credential-manager-property.md) в хранилище свойств.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-107">Set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the property store.</span></span> <span data-ttu-id="7b2f3-108">Значение свойства является указателем на интерфейс [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="7b2f3-108">The value of the property is a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
4.  <span data-ttu-id="7b2f3-109">Передайте указатель на хранилище свойств в сопоставитель источника, как описано в разделе [Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="7b2f3-109">Pass a pointer to the property store to the source resolver, as described in [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="7b2f3-110">Сетевые источники используют диспетчер учетных данных для получения учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-110">The network sources uses the credential manager to get user credentials.</span></span> <span data-ttu-id="7b2f3-111">Если источнику сети требуются учетные данные для доступа к сетевому ресурсу, он вызывает метод [**имфнеткредентиалманажер:: бегинжеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) приложения.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-111">If the network source requires credentials to access a network resource, it calls the application's [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span> <span data-ttu-id="7b2f3-112">Этот вызов запускает асинхронный запрос на получение учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-112">This call starts an asynchronous request to gets the user's credentials.</span></span> <span data-ttu-id="7b2f3-113">Метод **бегинжеткредентиалс** может получить учетные данные из кэша учетных данных или от пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-113">The **BeginGetCredentials** method can get the credentials either from the credential cache or from the user.</span></span> <span data-ttu-id="7b2f3-114">Учетные данные хранятся в *объекте учетных данных*.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-114">Credentials are stored in a *credential object*.</span></span> <span data-ttu-id="7b2f3-115">После завершения операции приложение вызывает интерфейс обратного вызова для уведомления сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-115">When the operation is complete, the application invokes the callback interface to notify the network source.</span></span> <span data-ttu-id="7b2f3-116">Сетевой источник вызывает [**имфнеткредентиалманажер:: енджеткредентиалс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) для завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-116">The network source calls [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) to complete the asynchronous operation.</span></span>

<span data-ttu-id="7b2f3-117">Так как это асинхронная операция, приложение должно отправить обратный вызов в конце операции.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-117">Because this is an asynchronous operation, the application must dispatch the callback at the end of the operation.</span></span> <span data-ttu-id="7b2f3-118">Пошаговые инструкции по написанию асинхронного метода см. в разделе [написание асинхронного метода](writing-an-asynchronous-method.md).</span><span class="sxs-lookup"><span data-stu-id="7b2f3-118">For step-by-step instructions about writing an asynchronous method, see [Writing an Asynchronous Method](writing-an-asynchronous-method.md).</span></span>

<span data-ttu-id="7b2f3-119">В следующем примере показано, как задать свойство [**\_ \_ диспетчера учетных данных мфнетсаурце**](mfnetsource-credential-manager-property.md) в сетевом источнике.</span><span class="sxs-lookup"><span data-stu-id="7b2f3-119">The following example shows how to set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the network source.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7b2f3-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7b2f3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b2f3-121">Проверка подлинности источника сети</span><span class="sxs-lookup"><span data-stu-id="7b2f3-121">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



