---
description: В этом разделе описывается создание профиля ASF в Microsoft Media Foundation.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Создание профиля ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ed9553811645b8589de7fb1805f1a307c4bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682376"
---
# <a name="creating-an-asf-profile"></a>Создание профиля ASF

В этом разделе описывается создание профиля ASF в Microsoft Media Foundation.

-   [Создать новый профиль](#create-a-new-profile)
-   [Получение профиля из объекта ASF Контентинфо](#get-the-profile-from-the-asf-contentinfo-object)
-   [Получение профиля из дескриптора презентации](#get-the-profile-from-a-presentation-descriptor)
-   [См. также](#related-topics)

## <a name="create-a-new-profile"></a>Создать новый профиль

Чтобы создать пустой профиль ASF, вызовите функцию [**мфкреатеасфпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) . Эта функция возвращает указатель на интерфейс [**имфасфпрофиле**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) . Приложение может использовать этот интерфейс для добавления потоков в профиль и настройки каждого из потоков. Дополнительные сведения см. в разделе [Создание и настройка потоков ASF](creating-and-configuring-asf-streams.md).

При необходимости приложение может добавлять взаимоисключающие объекты в два или более потоков. См. раздел [Использование взаимного исключения для потоков ASF](using-mutual-exclusion-for-asf-streams.md).

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a>Получение профиля из объекта ASF Контентинфо

Приложение может получить профиль ASF существующего файла ASF из [объекта ASF контентинфо](asf-contentinfo-object.md). Профиль уже настроен и содержит параметры для всех потоков в файле.

Инициализируйте объект Контентинфо, анализируя объект заголовка ASF файла. Это делается с помощью метода [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) . После того как будут считаны все объекты заголовка и заполнена библиотека ASF, будет создан профиль для этого файла. Приложение может получить указатель на этот инициализированный профиль, вызвав [**имфасфконтентинфо::-Profile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).

## <a name="get-the-profile-from-a-presentation-descriptor"></a>Получение профиля из дескриптора презентации

Объект профиля существующего файла ASF можно получить из [дескриптора презентации](presentation-descriptors.md) для файла или из объекта [ASF контентинфо](asf-contentinfo-object.md) . В этом случае профиль уже настроен и содержит параметры для всех потоков в файле. Это может быть полезно, если требуется изменить существующий профиль ASF. Например, может потребоваться повторное Кодирование видеофайла Windows Media с более низкой скоростью.

Чтобы получить профиль из дескриптора презентации, вызовите [**мфкреатеасфпрофилефромпресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor). Эта функция анализирует дескриптор представления и заполняет профиль ASF сведениями о файле мультимедиа. Функция возвращает указатель на интерфейс Имфасфпрофиле. Затем этот интерфейс можно использовать для изменения профиля.

Чтобы получить дескриптор представления, вызовите один из следующих методов:

-   В источнике носителя ASF вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   Из объекта [ASF контентинфо](asf-contentinfo-object.md) вызовите [**Имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Перед вызовом этого метода убедитесь, что объект Контентинфо инициализирован для чтения. Дополнительные сведения см. в разделе "инициализация объекта Контентинфо из существующего файла ASF" [статьи чтение объекта заголовка ASF существующего файла](reading-the-asf-header-object-of-an-existing-file.md). Однако если у вас уже есть инициализированный объект Контентинфо, вы можете получить профиль непосредственно из него. Это описано в подразделе «Получение профиля из объекта Контентинфо» далее в этой статье.

В следующем примере показано, как создать профиль из дескриптора презентации. Функция создает источник мультимедиа для файла, получает дескриптор представления из источника мультимедиа и создает профиль. В этом примере предполагается, что *pszFileName* указывает URL-адрес файла ASF.


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



В этом примере для высвобождения указателей интерфейса используется [саферелеасе](saferelease.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Профиль ASF](asf-profile.md)
</dt> </dl>

 

 



