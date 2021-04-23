---
title: Создание пакета приложения (C++)
description: Узнайте, как создать пакет приложения для приложения Windows с помощью API упаковки.
ms.assetid: FD677D75-50D5-4228-891F-73B5F40679B0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1808ebf57d4c7125f5509db68e22b78ce949f7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "105700840"
---
# <a name="how-to-create-an-app-package-c"></a><span data-ttu-id="8ea80-103">Создание пакета приложения (C++)</span><span class="sxs-lookup"><span data-stu-id="8ea80-103">How to create an app package (C++)</span></span>

<span data-ttu-id="8ea80-104">Узнайте, как создать пакет приложения для приложения Windows с помощью [API упаковки](interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="8ea80-104">Learn how to create an app package for a Windows app using the [packaging API](interfaces.md).</span></span>

<span data-ttu-id="8ea80-105">Если вы хотите создать пакет для классических приложений вручную, можно также использовать средство MakeAppx.exe, использующее [API упаковки](interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="8ea80-105">If you want to create a desktop app package manually, you can also use the MakeAppx.exe tool which utilizes the [packaging API](interfaces.md).</span></span> <span data-ttu-id="8ea80-106">Дополнительные сведения см. в разделе [упаковщик приложений (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea80-106">See [App packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) for more information.</span></span>

<span data-ttu-id="8ea80-107">Если вы используете Visual Studio, для упаковки приложения рекомендуется использовать мастер упаковки Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8ea80-107">If you are using Visual Studio, it's recommended that you use the Visual Studio packaging wizard to package your app.</span></span> <span data-ttu-id="8ea80-108">Дополнительные сведения см. [в статье Упаковка приложения UWP с помощью Visual Studio](/windows/msix/package/packaging-uwp-apps).</span><span class="sxs-lookup"><span data-stu-id="8ea80-108">For more details, see [Package a UWP app using Visual Studio](/windows/msix/package/packaging-uwp-apps).</span></span>

## <a name="instructions"></a><span data-ttu-id="8ea80-109">Инструкции</span><span class="sxs-lookup"><span data-stu-id="8ea80-109">Instructions</span></span>

### <a name="step-1-create-a-package-writer"></a><span data-ttu-id="8ea80-110">Шаг 1. Создание модуля записи пакета</span><span class="sxs-lookup"><span data-stu-id="8ea80-110">Step 1: Create a package writer</span></span>

<span data-ttu-id="8ea80-111">Чтобы создать модуль записи пакета, вызовите метод [**иаппксфактори:: креатепаккажевритер**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagewriter) .</span><span class="sxs-lookup"><span data-stu-id="8ea80-111">To create a package writer, call the [**IAppxFactory::CreatePackageWriter**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagewriter) method.</span></span> <span data-ttu-id="8ea80-112">Первый параметр — это выходной поток, в который будет записан пакет.</span><span class="sxs-lookup"><span data-stu-id="8ea80-112">The first parameter is an output stream where the package will be written.</span></span> <span data-ttu-id="8ea80-113">Второй параметр — это указатель на структуру [**\_ \_ параметров пакета APPX**](/windows/desktop/api/AppxPackaging/ns-appxpackaging-appx_package_settings) , указывающий параметры пакета.</span><span class="sxs-lookup"><span data-stu-id="8ea80-113">The second parameter is a pointer to an [**APPX\_PACKAGE\_SETTINGS**](/windows/desktop/api/AppxPackaging/ns-appxpackaging-appx_package_settings) structure that specifies package settings.</span></span> <span data-ttu-id="8ea80-114">Третий параметр — это выходной параметр, который получает указатель на указатель [**иаппкспаккажевритер**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagewriter) .</span><span class="sxs-lookup"><span data-stu-id="8ea80-114">The third parameter is an output parameter that receives a pointer to an [**IAppxPackageWriter**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagewriter) pointer.</span></span>


```C++
#include <windows.h>
#include <shlwapi.h>
#include <AppxPackaging.h>

// We store the produced package under this file name.
const LPCWSTR OutputPackagePath = L"HelloWorld.appx";

int wmain()
{
    HRESULT hr = S_OK;

    // Specify the appropriate COM threading model
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (SUCCEEDED(hr))
    {
        // Create a package writer
        IAppxPackageWriter* packageWriter = NULL;

        hr = GetPackageWriter(OutputPackagePath, &packageWriter);
    }
}

//
// Creates an app package writer with default settings.
//
// Parameters:
//   outputFileName  
//     Fully qualified name of the app package (.appx file) to be created.
//   writer 
//     On success, receives the created instance of IAppxPackageWriter.
//
HRESULT GetPackageWriter(
    _In_ LPCWSTR outputFileName,
    _Outptr_ IAppxPackageWriter** writer)
{
    const LPCWSTR Sha256AlgorithmUri = L"https://www.w3.org/2001/04/xmlenc#sha256"; 
    HRESULT hr = S_OK;
    IStream* outputStream = NULL;
    IUri* hashMethod = NULL;
    APPX_PACKAGE_SETTINGS packageSettings = {0};
    IAppxFactory* appxFactory = NULL;

    // Create a stream over the output file for the package 
    hr = SHCreateStreamOnFileEx(
            outputFileName,
            STGM_CREATE | STGM_WRITE | STGM_SHARE_EXCLUSIVE,
            0,     // default file attributes
            TRUE,  // create file if it does not exist
            NULL,  // no template
            &outputStream);

    // Create default package writer settings, including hash algorithm URI
    // and Zip format.
    if (SUCCEEDED(hr))
    {        hr = CreateUri(
                Sha256AlgorithmUri,
                Uri_CREATE_CANONICALIZE,
                0, // reserved parameter
                &hashMethod);
    }

    if (SUCCEEDED(hr))
    {
        packageSettings.forceZip32 = TRUE;
        packageSettings.hashMethod = hashMethod;
    }

    // Create a new Appx factory
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(
                __uuidof(AppxFactory),
                NULL,
                CLSCTX_INPROC_SERVER,
                __uuidof(IAppxFactory),
                (LPVOID*)(&appxFactory));
    }

    // Create a new package writer using the factory
    if (SUCCEEDED(hr))
    {
        hr = appxFactory->CreatePackageWriter(
                outputStream,
                &packageSettings,
                writer);
    }

    // Clean up allocated resources
    if (appxFactory != NULL)
    {
        appxFactory->Release();
        appxFactory = NULL;
    }
    if (hashMethod != NULL)
    {
        hashMethod->Release();
        hashMethod = NULL;
    }
    if (outputStream != NULL)
    {
        outputStream->Release();
        outputStream = NULL;
    }
    return hr;
}
```



### <a name="step-2-add-the-payload-files-for-your-app-to-the-package"></a><span data-ttu-id="8ea80-115">Шаг 2. Добавление файлов полезных данных для приложения в пакет</span><span class="sxs-lookup"><span data-stu-id="8ea80-115">Step 2: Add the payload files for your app to the package</span></span>

<span data-ttu-id="8ea80-116">Вызовите метод [**иаппкспаккажевритер:: аддпайлоадфиле**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-addpayloadfile) , чтобы добавить файлы в пакет.</span><span class="sxs-lookup"><span data-stu-id="8ea80-116">Call the [**IAppxPackageWriter::AddPayloadFile**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-addpayloadfile) method to add files to the package.</span></span> <span data-ttu-id="8ea80-117">Первый параметр — это относительный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="8ea80-117">The first parameter is the relative path of the file.</span></span> <span data-ttu-id="8ea80-118">Второй параметр указывает тип содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="8ea80-118">The second parameter indicates the content type of the file.</span></span> <span data-ttu-id="8ea80-119">Третий параметр задает параметры из перечисления параметров [**\_ \_ сжатия APPX**](/windows/desktop/api/AppxPackaging/ne-appxpackaging-appx_compression_option) .</span><span class="sxs-lookup"><span data-stu-id="8ea80-119">The third parameter specifies options from the [**APPX\_COMPRESSION\_OPTION**](/windows/desktop/api/AppxPackaging/ne-appxpackaging-appx_compression_option) enumeration.</span></span> <span data-ttu-id="8ea80-120">Четвертый параметр — это входной поток для файла.</span><span class="sxs-lookup"><span data-stu-id="8ea80-120">The fourth parameter is the input stream for the file.</span></span>


```C++
// Path where all input files are stored
const LPCWSTR DataPath = L"Data\\";

// Add all payload files to the package writer
for (int i = 0; SUCCEEDED(hr) && (i < PayloadFilesCount); i++)
{
    IStream* fileStream = NULL;

    hr = GetFileStream(DataPath, PayloadFilesName[i], &fileStream);

    if (SUCCEEDED(hr))
    {
        packageWriter->AddPayloadFile(
            PayloadFilesName[i],
            PayloadFilesContentType[i],
            PayloadFilesCompression[i],
            fileStream);
        }

        if (fileStream != NULL)
        {
            fileStream->Release();
            fileStream = NULL;
        }
    }
}
```



<span data-ttu-id="8ea80-121">В предыдущем коде используются определения переменных и `GetFileStream` вспомогательная функция.</span><span class="sxs-lookup"><span data-stu-id="8ea80-121">The previous code uses these variable definitions and `GetFileStream` helper function.</span></span>


```C++
#include <strsafe.h>
#include <shlwapi.h>

// The produced app package's content consists of these files, with
// corresponding content types and compression options.
const int PayloadFilesCount = 4;
const LPCWSTR PayloadFilesName[PayloadFilesCount] = {
    L"AppTile.png",
    L"Default.html",
    L"images\\smiley.jpg",
    L"Error.html",
};
const LPCWSTR PayloadFilesContentType[PayloadFilesCount] = {
    L"image/png",
    L"text/html",
    L"image/jpeg",
    L"text/html",
};
const APPX_COMPRESSION_OPTION PayloadFilesCompression[PayloadFilesCount] = {
    APPX_COMPRESSION_OPTION_NONE,
    APPX_COMPRESSION_OPTION_NORMAL,
    APPX_COMPRESSION_OPTION_NONE,
    APPX_COMPRESSION_OPTION_NORMAL,
};

//
// Creates a readable IStream over the specified file. For simplicity, we assume that the fully 
// qualified file name is 100 characters or less. Your code should 
// handle longer names, and allocate the buffer dynamically.
//
// Parameters:
//   path 
//      Path of the folder that contains the file to be opened; must end with a '\'
//   fileName 
//      Name, of the file to be opened, not including the path
//   stream 
//      On success, receives the created instance of IStream
//
HRESULT GetFileStream(
    _In_ LPCWSTR path,
    _In_ LPCWSTR fileName,
    _Outptr_ IStream** stream)
{
    HRESULT hr = S_OK;
    const int MaxFileNameLength = 100;
    WCHAR fullFileName[MaxFileNameLength + 1];

    // Create full file name by concatenating path and fileName
    hr = StringCchCopyW(fullFileName, MaxFileNameLength, path);
    if (SUCCEEDED(hr))
    {
        hr = StringCchCat(fullFileName, MaxFileNameLength, fileName);
    }

    // Create stream for reading the file
    if (SUCCEEDED(hr))
    {
        hr = SHCreateStreamOnFileEx(
                fullFileName,
                STGM_READ | STGM_SHARE_EXCLUSIVE,
                0,      // default file attributes
                FALSE,  // don't create new file
                NULL,   // no template
                stream);
    }
    return hr;
}
```



### <a name="step-3-add-the-package-manifest-to-the-package"></a><span data-ttu-id="8ea80-122">Шаг 3. Добавление манифеста пакета в пакет</span><span class="sxs-lookup"><span data-stu-id="8ea80-122">Step 3: Add the package manifest to the package</span></span>

<span data-ttu-id="8ea80-123">Каждый пакет должен иметь манифест пакета.</span><span class="sxs-lookup"><span data-stu-id="8ea80-123">Every package must have a package manifest.</span></span> <span data-ttu-id="8ea80-124">Чтобы добавить в пакет манифест пакета, создайте входной поток для файла, а затем вызовите метод [**иаппкспаккажевритер:: Close**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-close) для записи манифеста в конце пакета и закройте поток вывода для модуля записи пакета.</span><span class="sxs-lookup"><span data-stu-id="8ea80-124">To add the package manifest to the package, create an input stream for the file, then call the [**IAppxPackageWriter::Close**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-close) method to write the manifest at the end of the package and close the output stream for package writer.</span></span>

<span data-ttu-id="8ea80-125">Этот код использует `GetFileStream` вспомогательную функцию, показанную на предыдущем шаге, для создания потока для манифеста пакета.</span><span class="sxs-lookup"><span data-stu-id="8ea80-125">This code uses the `GetFileStream` helper function shown in the previous step to create the stream for the package manifest.</span></span>


```C++
// We read the app package's manifest from this file
const LPCWSTR ManifestFileName = L"AppxManifest.xml";

IStream* manifestStream = NULL;

hr = GetFileStream(DataPath, ManifestFileName, &manifestStream);

if (SUCCEEDED(hr))
{
    hr = packageWriter->Close(manifestStream);
}

if (manifestStream != NULL)
{
    manifestStream->Release();
    manifestStream = NULL;
}
```



### <a name="step-4-clean-up-the-package-writer"></a><span data-ttu-id="8ea80-126">Шаг 4. Очистка модуля записи пакета</span><span class="sxs-lookup"><span data-stu-id="8ea80-126">Step 4: Clean up the package writer</span></span>

<span data-ttu-id="8ea80-127">Перед возвратом из `wmain` функции вызовите метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) , чтобы очистить модуль записи пакета и вызвать функцию [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="8ea80-127">Before returning from the `wmain` function, call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method to clean up the package writer and call the [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


```C++
if (packageWriter != NULL)
{
    packageWriter->Release();
    packageWriter = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="8ea80-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8ea80-128">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8ea80-129">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="8ea80-129">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="8ea80-130">Пример создания пакета приложения</span><span class="sxs-lookup"><span data-stu-id="8ea80-130">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="8ea80-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8ea80-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8ea80-132">**иаппкспаккажевритер**</span><span class="sxs-lookup"><span data-stu-id="8ea80-132">**IAppxPackageWriter**</span></span>](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagewriter)
</dt> </dl>

 

 