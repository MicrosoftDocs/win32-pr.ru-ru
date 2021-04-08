---
title: Сведения о манифесте пакета приложения запроса (C++)
description: Узнайте, как получить сведения из манифеста пакета приложения для приложения Windows с помощью API упаковки.
ms.assetid: A29986F9-C620-48CD-87F8-525DFA076AAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9940f92a4412be7731db2454d68b4429522b63f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069826"
---
# <a name="query-app-package-manifest-info-c"></a>Сведения о манифесте пакета приложения запроса (C++)

Узнайте, как получить сведения из манифеста пакета приложения для приложения Windows с помощью [API упаковки](interfaces.md).

### <a name="create-a-package-manifest-reader"></a>Создание средства чтения манифеста пакета

Чтобы создать средство чтения манифеста пакета, вызовите [**иаппксфактори:: креатепаккажереадер**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagereader) , чтобы создать модуль чтения пакетов. Первый параметр — это входной поток для пакета (Appx-файл). Второй параметр — это выходной параметр, который получает указатель на указатель [**иаппкспаккажереадер**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagereader) . Затем вызовите [**иаппкспаккажереадер:: manifest**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagereader-getmanifest) , чтобы получить средство чтения манифеста. Параметр — это выходной параметр, который получает указатель на указатель [**иаппксманифестреадер**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader) .


```C++
int wmain(
    _In_ int argc,
    _In_reads_(argc) wchar_t** argv)
{
    HRESULT hr = S_OK;
 
    if (argc != 2)
    {
        wprintf(L"Usage: DescribeAppx.exe inputFile\n");
        wprintf(L"       inputFile: Path to the app package to read\n");
        return 2;
    }

    // Specify the appropriate COM threading model
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (SUCCEEDED(hr))
    {
        IAppxPackageReader* packageReader = NULL;
        IAppxManifestReader* manifestReader = NULL;

        // Create a package reader using the file name given in command line
        hr = GetPackageReader(argv[1], &packageReader);

        // Get manifest reader for the package and read from the manifest
        if (SUCCEEDED(hr))
        {
            hr = packageReader->GetManifest(&manifestReader);
        }
        if (SUCCEEDED(hr))
        {
            hr = ReadManifest(manifestReader);
        }
    }
}

//
// Creates an app package reader.
//
// Parameters:
//   inputFileName 
//     Fully qualified name of the app package (.appx file) to be opened.
//   reader 
//     On success, receives the created instance of IAppxPackageReader.
//
HRESULT GetPackageReader(
    _In_ LPCWSTR inputFileName,
    _Outptr_ IAppxPackageReader** reader)
{
    HRESULT hr = S_OK;
    IAppxFactory* appxFactory = NULL;
    IStream* inputStream = NULL;

    // Create a new factory
    hr = CoCreateInstance(
            __uuidof(AppxFactory),
            NULL,
            CLSCTX_INPROC_SERVER,
            __uuidof(IAppxFactory),
            (LPVOID*)(&appxFactory));

    // Create a stream over the input app package
    if (SUCCEEDED(hr))
    {
        hr = SHCreateStreamOnFileEx(
                inputFileName,
                STGM_READ | STGM_SHARE_EXCLUSIVE,
                0, // default file attributes
                FALSE, // do not create new file
                NULL, // no template
                &inputStream);
    }

    // Create a new package reader using the factory.  For 
    // simplicity, we don't verify the digital signature of the package.
    if (SUCCEEDED(hr))
    {
        hr = appxFactory->CreatePackageReader(
                inputStream,
                reader);
    }

    // Clean up allocated resources
    if (inputStream != NULL)
    {
        inputStream->Release();
        inputStream = NULL;
    }
    if (appxFactory != NULL)
    {
        appxFactory->Release();
        appxFactory = NULL;
    }
    return hr;
}
```



### <a name="read-package-identity-info"></a>Чтение сведений об удостоверении пакета

Указание пакета указывается с помощью элемента [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) в манифесте. Используйте [**иаппксманифестреадер:: жетпаккажеид**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getpackageid) , чтобы получить [**иаппксманифестпаккажеид**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestpackageid) для чтения сведений об удостоверении пакета, как показано здесь.

Этот код использует [**иаппксманифестпаккажеид:: жетпаккажефуллнаме**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getpackagefullname) для получения полного имени пакета, [**Иаппксманифестпаккажеид:: Name**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getname) , чтобы получить имя пакета, и [**иаппксманифестпаккажеид::**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getversion) для получения версии пакета.


```C++
//
// Reads a subset of the manifest Identity element.
//
//
HRESULT ReadManifestPackageId(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestPackageId* packageId = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetPackageId(&packageId);
    if (SUCCEEDED(hr))
    {
        LPWSTR packageFullName = NULL;
        LPWSTR packageName = NULL;
        UINT64 packageVersion = 0;

        hr = packageId->GetPackageFullName(&packageFullName);

        if (SUCCEEDED(hr))
        {
            hr = packageId->GetName(&packageName);
        }
        if (SUCCEEDED(hr))
        {
            hr = packageId->GetVersion(&packageVersion);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package full name: %s\n", packageFullName);
            wprintf(L"Package name: %s\n", packageName);
            wprintf(L"Package version: ");

            // Convert version number from 64-bit integer to dot-quad form
            for (int bitPosition = 0x30; bitPosition >= 0; bitPosition -= 0x10)
            {
                UINT64 versionWord = (packageVersion >> bitPosition) & 0xFFFF;
                wprintf(L"%llu.", versionWord);
            }
            wprintf(L"\n");
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(packageFullName);
        CoTaskMemFree(packageName);
    }

    // Clean up allocated resources
    if (packageId != NULL)
    {
        packageId->Release();
        packageId = NULL;
    }
     
    return hr;
}
```



### <a name="read-metadata-that-describes-the-package-to-users"></a>Чтение метаданных, описывающих пакет для пользователей

Свойства задаются с помощью элемента [**Properties**](/uwp/schemas/appxpackage/appxmanifestschema/element-properties) в манифесте. Используйте [**иаппксманифестреадер:: Properties**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getproperties) , чтобы получить [**иаппксманифестпропертиес**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestproperties) для чтения этого узла, как показано ниже.

Этот код использует [**иаппксманифестпропертиес:: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestproperties-getstringvalue) для получения отображаемого имени и описания пакета.


```C++
//
// Reads a subset of the manifest Properties element.
//
//
HRESULT ReadManifestProperties(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestProperties* properties = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetProperties(&properties);
    if (SUCCEEDED(hr))
    {
        LPWSTR displayName = NULL;
        LPWSTR description = NULL;

        hr = properties->GetStringValue(L"DisplayName", &displayName);

        if (SUCCEEDED(hr))
        {
            hr = properties->GetStringValue(L"Description", &description);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package display name: %s\n", displayName);
            wprintf(L"Package description:  %s\n", description);
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(displayName);
        CoTaskMemFree(description);
    }
    // Clean up allocated resources
    if (properties != NULL)
    {
        properties->Release();
        properties = NULL;
    }

    return hr;
}
```



### <a name="read-metadata-about-the-apps-included-in-the-package"></a>Чтение метаданных о приложениях, входящих в пакет

Приложения указываются с помощью элемента [**Applications**](/uwp/schemas/appxpackage/appxmanifestschema/element-applications) в манифесте. Используйте [**иаппксманифестреадер::**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getapplications) иаппксманифестаппликатионсенумератор, чтобы получить [](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator) для чтения этого узла. Используйте [**иаппксманифестаппликатионсенумератор:: OnCurrent**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-getcurrent) и [**Иаппксманифестаппликатионсенумератор:: MoveNext**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext) , чтобы получить [**иаппксманифестаппликатион**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplication) для каждого приложения в пакете.

Этот код использует [**иаппксманифестаппликатион:: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplication-getstringvalue) для получения отображаемого имени для каждого приложения.


```C++
//
// Reads a subset of the manifest Applications element.
//
//
HRESULT ReadManifestApplications(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;
    BOOL hasCurrent = FALSE;
    UINT32 applicationsCount = 0;

    IAppxManifestApplicationsEnumerator* applications = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetApplications(&applications);
    if (SUCCEEDED(hr))
    {
        hr = applications->GetHasCurrent(&hasCurrent);

        while (SUCCEEDED(hr) && hasCurrent)
        {
            IAppxManifestApplication* application = NULL;
            LPWSTR applicationName = NULL;

            hr = applications->GetCurrent(&application);
            if (SUCCEEDED(hr))
            {
                application->GetStringValue(L"DisplayName", &applicationName);
            }
            if (SUCCEEDED(hr))
            {
                applicationsCount++;
                wprintf(L"App #%u: %s\n", applicationsCount, applicationName);
            }

            if (SUCCEEDED(hr))
            {
                hr = applications->MoveNext(&hasCurrent);
            }
            if (application != NULL)
            {
                application->Release();
                application = NULL;
            }
            CoTaskMemFree(applicationName);
        }

        wprintf(L"Count of apps in the package: %u\n", applicationsCount);
    }

    // Clean up allocated resources
    if (applications != NULL)
    {
        applications->Release();
        applications = NULL;
    }

    return hr;
}
```



### <a name="clean-up-the-package-manifest-reader"></a>Очистка средства чтения манифеста пакета

Перед возвратом из `wmain` функции вызовите метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) , чтобы очистить средство чтения манифеста пакета и вызвать функцию [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) .


```C++
// Clean up allocated resources
if (manifestReader != NULL)
{
    manifestReader->Release();
    manifestReader = NULL;
}
if (packageReader != NULL)
{
    packageReader->Release();
    packageReader = NULL;
}

CoUninitialize();
```



## <a name="related-topics"></a>См. также

<dl> <dt>

**Примеры**
</dt> <dt>

[Пример пакета приложения запроса и манифеста приложения](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx)
</dt> <dt>

**Ссылки**
</dt> <dt>

[**иаппксманифестреадер**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader)
</dt> </dl>

 

 