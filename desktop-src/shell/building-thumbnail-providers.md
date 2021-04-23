---
description: Начиная с Windows Vista, в большей мере используются эскизы, относящиеся к файлам, чем в предыдущих версиях Windows.
title: Создание обработчиков эскизов
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 218264a9-ed26-4049-a721-232943f6ec53
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05e13f24a2f4d70a58bab904150b1e488f74854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984356"
---
# <a name="building-thumbnail-handlers"></a><span data-ttu-id="420db-103">Создание обработчиков эскизов</span><span class="sxs-lookup"><span data-stu-id="420db-103">Building Thumbnail Handlers</span></span>

<span data-ttu-id="420db-104">Начиная с Windows Vista, в большей мере используются эскизы, относящиеся к файлам, чем в предыдущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="420db-104">As of Windows Vista, greater use is made of file-specific thumbnail images than in earlier versions of Windows.</span></span> <span data-ttu-id="420db-105">Они используются во всех представлениях, в диалоговых окнах и для любого типа файлов, который их предоставляет.</span><span class="sxs-lookup"><span data-stu-id="420db-105">They are used in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="420db-106">Отображение эскиза также изменилось.</span><span class="sxs-lookup"><span data-stu-id="420db-106">Thumbnail display was also changed.</span></span> <span data-ttu-id="420db-107">Доступен непрерывный спектр размеров, выбираемых пользователем, а не дискретные размеры, такие как значки и эскизы.</span><span class="sxs-lookup"><span data-stu-id="420db-107">A continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails.</span></span>

<span data-ttu-id="420db-108">Интерфейс [**исумбнаилпровидер**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) предоставляет эскиз более простым, чем старый [**иекстрактимаже**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) или [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span><span class="sxs-lookup"><span data-stu-id="420db-108">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface makes providing a thumbnail more straightforward than the older [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) or [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span></span> <span data-ttu-id="420db-109">Однако обратите внимание, что существующий код, использующий **иекстрактимаже** или **IExtractImage2** , по-прежнему является допустимым и поддерживаемым.</span><span class="sxs-lookup"><span data-stu-id="420db-109">Note, however, that existing code that uses **IExtractImage** or **IExtractImage2** is still valid and supported.</span></span>

## <a name="the-recipethumbnailprovider-sample"></a><span data-ttu-id="420db-110">Пример РеЦипесумбнаилпровидер</span><span class="sxs-lookup"><span data-stu-id="420db-110">The RecipeThumbnailProvider Sample</span></span>

<span data-ttu-id="420db-111">Пример [реЦипесумбнаилпровидер](samples-recipethumbnailprovider.md) вводятся в этом разделе включен в пакет средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="420db-111">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample dissected in this section is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="420db-112">Расположение установки по умолчанию — C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ Samples \\ винуи \\ Shell \\ аппшеллинтегратион \\ реЦипесумбнаилпровидер.</span><span class="sxs-lookup"><span data-stu-id="420db-112">Its default install location is C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppShellIntegration\\RecipeThumbnailProvider.</span></span> <span data-ttu-id="420db-113">Однако здесь также содержится основная часть кода.</span><span class="sxs-lookup"><span data-stu-id="420db-113">However, the bulk of the code is included here as well.</span></span>

<span data-ttu-id="420db-114">В примере [реЦипесумбнаилпровидер](samples-recipethumbnailprovider.md) демонстрируется реализация обработчика эскизов для нового типа файлов, зарегистрированного с расширением. рецепт.</span><span class="sxs-lookup"><span data-stu-id="420db-114">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample demonstrates the implementation of a thumbnail handler for a new file type registered with a .recipe extension.</span></span> <span data-ttu-id="420db-115">В этом примере показано использование различных API-интерфейсов обработчика эскизов для регистрации серверов модели COM для извлечения эскизов для пользовательских типов файлов.</span><span class="sxs-lookup"><span data-stu-id="420db-115">The sample illustrates the use of the different thumbnail handler APIs to register thumbnail extraction Component Object Model (COM) servers for custom file types.</span></span> <span data-ttu-id="420db-116">В этом разделе описывается пример кода, который выделяет варианты написания кода и рекомендации.</span><span class="sxs-lookup"><span data-stu-id="420db-116">This topic walks you through the sample code, highlighting coding choices and guidelines.</span></span>

<span data-ttu-id="420db-117">Обработчик эскиза должен всегда реализовывать [**исумбнаилпровидер**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) в сочетании с одним из следующих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="420db-117">A thumbnail handler must always implement [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) in concert with one of these interfaces:</span></span>

-   [<span data-ttu-id="420db-118">**IInitializeWithStream**</span><span class="sxs-lookup"><span data-stu-id="420db-118">**IInitializeWithStream**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="420db-119">**иинитиализевиситем**</span><span class="sxs-lookup"><span data-stu-id="420db-119">**IInitializeWithItem**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="420db-120">**IInitializeWithFile**</span><span class="sxs-lookup"><span data-stu-id="420db-120">**IInitializeWithFile**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="420db-121">Бывают случаи, когда инициализация с помощью потоков невозможна.</span><span class="sxs-lookup"><span data-stu-id="420db-121">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="420db-122">В сценариях, где обработчик эскизов не реализует [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), он должен отказаться от выполнения в изолированном процессе, когда системный индексатор поместит его по умолчанию при изменении потока.</span><span class="sxs-lookup"><span data-stu-id="420db-122">In scenarios where your thumbnail handler does not implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process where the system indexer places it by default when there is a change to the stream.</span></span> <span data-ttu-id="420db-123">Чтобы отказаться от использования функции изоляции процессов, установите следующее значение реестра.</span><span class="sxs-lookup"><span data-stu-id="420db-123">To opt out of the process isolation feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

<span data-ttu-id="420db-124">Если вы реализуете [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) и выполняете инициализацию на основе потока, ваш обработчик является более безопасным и надежным.</span><span class="sxs-lookup"><span data-stu-id="420db-124">If you implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization, your handler is more secure and reliable.</span></span> <span data-ttu-id="420db-125">Как правило, отключение изоляции процессов предназначено только для устаревших обработчиков; Избегайте отключения этой функции для любого нового кода.</span><span class="sxs-lookup"><span data-stu-id="420db-125">Typically, disabling process isolation is only intended for legacy handlers; avoid disabling this feature for any new code.</span></span> <span data-ttu-id="420db-126">**IInitializeWithStream** должен быть первым выбором интерфейса инициализации везде, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="420db-126">**IInitializeWithStream** should be your first choice of initialization interface whenever possible.</span></span>

<span data-ttu-id="420db-127">Поскольку файл изображения в образце не внедрен в файл. рецепт и не является частью его файлового потока, в примере используется [**иинитиализевиситем**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) .</span><span class="sxs-lookup"><span data-stu-id="420db-127">Because the image file in the sample is not embedded in the .recipe file and is not a part of its file stream, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) is used in the sample.</span></span> <span data-ttu-id="420db-128">Реализация метода [**иинитиализевиситем:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) просто передает свои параметры закрытым переменным класса.</span><span class="sxs-lookup"><span data-stu-id="420db-128">The implementation of the [**IInitializeWithItem::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) method simply passes its parameters to private class variables.</span></span>

<span data-ttu-id="420db-129">[**Исумбнаилпровидер**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) имеет только один метод — «-[**эскиз**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)», который вызывается с самым большим требуемым размером изображения (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="420db-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) has only one method—[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)—that is called with the largest desired size of the image, in pixels.</span></span> <span data-ttu-id="420db-130">Хотя параметр называется *CX*, его значение используется как максимальный размер измерений x и y изображения.</span><span class="sxs-lookup"><span data-stu-id="420db-130">Although the parameter is named *cx*, its value is used as the maximum size of both the x and y dimensions of the image.</span></span> <span data-ttu-id="420db-131">Если полученный эскиз не является квадратным, то длинная ось будет ограничена *CX* , а пропорции исходного изображения сохраняются.</span><span class="sxs-lookup"><span data-stu-id="420db-131">If the retrieved thumbnail is not square, then the longer axis is limited by *cx* and the aspect ratio of the original image is preserved.</span></span>

<span data-ttu-id="420db-132">При возвращении параметр- [**эскиза**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) предоставляет маркер полученного изображения.</span><span class="sxs-lookup"><span data-stu-id="420db-132">When it returns, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) provides a handle to the retrieved image.</span></span> <span data-ttu-id="420db-133">Он также предоставляет значение, указывающее формат цвета изображения и наличие допустимых данных альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="420db-133">It also provides a value that indicates the color format of the image and whether it has valid alpha information.</span></span>

<span data-ttu-id="420db-134">Реализация метода thumbnail в примере начинается с вызова закрытого **\_ GetBase64EncodedImageString** .</span><span class="sxs-lookup"><span data-stu-id="420db-134">The GetThumbnail implementation in the sample begins with a call to the private **\_GetBase64EncodedImageString** method.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



<span data-ttu-id="420db-135">Тип файла. рецепт — это просто XML-файл, зарегистрированный как уникальное расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="420db-135">The .recipe file type is simply an XML file registered as a unique file name extension.</span></span> <span data-ttu-id="420db-136">Он содержит элемент с именем **Picture** , предоставляющий относительный путь и имя файла изображения, которое будет использоваться в качестве эскиза для данного файла рецепта.</span><span class="sxs-lookup"><span data-stu-id="420db-136">It includes an element called **Picture** that provides the relative path and file name of the image to use as the thumbnail for this particular .recipe file.</span></span> <span data-ttu-id="420db-137">Элемент **Picture** состоит из **исходного** атрибута, который задает изображение в кодировке Base 64 и необязательный атрибут **size** .</span><span class="sxs-lookup"><span data-stu-id="420db-137">The **Picture** element consists of the **Source** attribute that specifies a base 64 encoded image, and an optional **Size** attribute.</span></span>

<span data-ttu-id="420db-138">**Размер** имеет два значения: Малый и крупный.</span><span class="sxs-lookup"><span data-stu-id="420db-138">**Size** has two values, Small and Large.</span></span> <span data-ttu-id="420db-139">Это позволяет предоставлять несколько узлов **изображений** с отдельными изображениями.</span><span class="sxs-lookup"><span data-stu-id="420db-139">This allows you to provide multiple **Picture** nodes with separate images.</span></span> <span data-ttu-id="420db-140">Полученное изображение затем зависит от значения максимального размера (*CX*), указанного при вызове функции- [**эскиза**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span><span class="sxs-lookup"><span data-stu-id="420db-140">The image retrieved then depends on the maximum size value (*cx*) provided in the call to [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span></span> <span data-ttu-id="420db-141">Так как Windows никогда не изменяет размер изображения, размер которого превышает максимальный, для различных разрешений можно предоставить разные образы.</span><span class="sxs-lookup"><span data-stu-id="420db-141">Because Windows never sizes the image any larger than its maximum size, different images can be provided for different resolutions.</span></span> <span data-ttu-id="420db-142">Однако для простоты в этом примере атрибут **size** опускается и предоставляется только одно изображение для всех ситуаций.</span><span class="sxs-lookup"><span data-stu-id="420db-142">However, for simplicity, the sample omits the **Size** attribute and provides only one image for all situations.</span></span>

<span data-ttu-id="420db-143">Метод **\_ GetBase64EncodedImageString** , реализация которого показана здесь, использует api-интерфейсы модель DOM XML (DOM) для получения узла **изображения** .</span><span class="sxs-lookup"><span data-stu-id="420db-143">The **\_GetBase64EncodedImageString** method, whose implementation is shown here, uses XML Document Object Model (DOM) APIs to retrieve the **Picture** node.</span></span> <span data-ttu-id="420db-144">Из этого узла он извлекает изображение из **исходных** данных атрибута.</span><span class="sxs-lookup"><span data-stu-id="420db-144">From that node it extracts the image from the **Source** attribute data.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetBase64EncodedImageString(UINT /* cx */, 
                                                           PWSTR *ppszResult)
{
    *ppszResult = NULL;

    IXMLDOMDocument *pXMLDoc;
    HRESULT hr = _LoadXMLDocument(&pXMLDoc);
    if (SUCCEEDED(hr))
    {
        BSTR bstrQuery = SysAllocString(L"Recipe/Attachments/Picture");
        hr = bstrQuery ? S_OK : E_OUTOFMEMORY;
        if (SUCCEEDED(hr))
        {
            IXMLDOMNode *pXMLNode;
            hr = pXMLDoc->selectSingleNode(bstrQuery, &pXMLNode);
            if (SUCCEEDED(hr))
            {
                IXMLDOMElement *pXMLElement;
                hr = pXMLNode->QueryInterface(&pXMLElement);
                if (SUCCEEDED(hr))
                {
                    BSTR bstrAttribute = SysAllocString(L"Source");
                    hr = bstrAttribute ? S_OK : E_OUTOFMEMORY;
                    if (SUCCEEDED(hr))
                    {
                        VARIANT varValue;
                        hr = pXMLElement->getAttribute(bstrAttribute, &varValue);
                        if (SUCCEEDED(hr))
                        {
                            if ((varValue.vt == VT_BSTR) && varValue.bstrVal && varValue.bstrVal[0])
                            {
                                hr = SHStrDupW(varValue.bstrVal, ppszResult);
                            }
                            else
                            {
                                hr = E_FAIL;
                            }
                            VariantClear(&varValue);
                        }
                        SysFreeString(bstrAttribute);
                    }
                    pXMLElement->Release();
                }
                pXMLNode->Release();
            }
            SysFreeString(bstrQuery);
        }
        pXMLDoc->Release();
    }
    return hr;
}
```



<span data-ttu-id="420db-145">[**Затем передает**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) извлеченную строку в **\_ жетстреамфромстринг**.</span><span class="sxs-lookup"><span data-stu-id="420db-145">[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) then passes the retrieved string to **\_GetStreamFromString**.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
```



<span data-ttu-id="420db-146">Метод **\_ жетстреамфромстринг** , для которого показана реализация, которая преобразует закодированное изображение в поток.</span><span class="sxs-lookup"><span data-stu-id="420db-146">The **\_GetStreamFromString** method, whose implementation is shown here, which converts the encoded image to a stream.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetStreamFromString(PCWSTR pszImageName, 
                                                   IStream **ppImageStream)
{
    HRESULT hr = E_FAIL;

    DWORD dwDecodedImageSize = 0;
    DWORD dwSkipChars        = 0;
    DWORD dwActualFormat     = 0;

    // Base64-decode the string
    BOOL fSuccess = CryptStringToBinaryW(pszImageName, 
                                         NULL, 
                                         CRYPT_STRING_BASE64,
                                         NULL, 
                                         &dwDecodedImageSize, 
                                         &dwSkipChars, 
                                         &dwActualFormat);
    if (fSuccess)
    {
        BYTE *pbDecodedImage = (BYTE*)LocalAlloc(LPTR, dwDecodedImageSize);
        if (pbDecodedImage)
        {
            fSuccess = CryptStringToBinaryW(pszImageName, 
                                            lstrlenW(pszImageName), 
                                            CRYPT_STRING_BASE64,
                                            pbDecodedImage, 
                                            &dwDecodedImageSize, 
                                            &dwSkipChars, 
                                            &dwActualFormat);
            if (fSuccess)
            {
                *ppImageStream = SHCreateMemStream(pbDecodedImage, 
                                                   dwDecodedImageSize);
                if (*ppImageStream != NULL)
                {
                    hr = S_OK;
                }
            }
            LocalFree(pbDecodedImage);
        }
    }
    return hr;
}
```



<span data-ttu-id="420db-147">**А затем** использует интерфейсы API компонента Windows Imaging Component (WIC) для извлечения растрового изображения из потока и получения маркера для этого точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="420db-147">**GetThumbnail** then uses Windows Imaging Component (WIC) APIs to extract a bitmap from the stream and get a handle to that bitmap.</span></span> <span data-ttu-id="420db-148">Альфа-информация задана, компонент WIC правильно завершает работу, и метод завершается успешно.</span><span class="sxs-lookup"><span data-stu-id="420db-148">The alpha information is set, WIC is properly exited, and the method terminates successfully.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
        if (SUCCEEDED(hr))
        {
            hr = WICCreate32BitsPerPixelHBITMAP(pImageStream, 
                                                cx, 
                                                phbmp, 
                                                pdwAlpha);;

            pImageStream->Release();
        }
        CoTaskMemFree(pszBase64EncodedImageString);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="420db-149">См. также</span><span class="sxs-lookup"><span data-stu-id="420db-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="420db-150">Обработчики эскизов</span><span class="sxs-lookup"><span data-stu-id="420db-150">Thumbnail Handlers</span></span>](thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="420db-151">Рекомендации по обработке эскизов</span><span class="sxs-lookup"><span data-stu-id="420db-151">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> <dt>

[<span data-ttu-id="420db-152">**IID \_ ППВ \_ args**</span><span class="sxs-lookup"><span data-stu-id="420db-152">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
