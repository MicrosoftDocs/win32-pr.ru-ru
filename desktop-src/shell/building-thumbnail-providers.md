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
# <a name="building-thumbnail-handlers"></a>Создание обработчиков эскизов

Начиная с Windows Vista, в большей мере используются эскизы, относящиеся к файлам, чем в предыдущих версиях Windows. Они используются во всех представлениях, в диалоговых окнах и для любого типа файлов, который их предоставляет. Отображение эскиза также изменилось. Доступен непрерывный спектр размеров, выбираемых пользователем, а не дискретные размеры, такие как значки и эскизы.

Интерфейс [**исумбнаилпровидер**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) предоставляет эскиз более простым, чем старый [**иекстрактимаже**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) или [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2). Однако обратите внимание, что существующий код, использующий **иекстрактимаже** или **IExtractImage2** , по-прежнему является допустимым и поддерживаемым.

## <a name="the-recipethumbnailprovider-sample"></a>Пример РеЦипесумбнаилпровидер

Пример [реЦипесумбнаилпровидер](samples-recipethumbnailprovider.md) вводятся в этом разделе включен в пакет средств разработки программного обеспечения (SDK) для Windows. Расположение установки по умолчанию — C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ Samples \\ винуи \\ Shell \\ аппшеллинтегратион \\ реЦипесумбнаилпровидер. Однако здесь также содержится основная часть кода.

В примере [реЦипесумбнаилпровидер](samples-recipethumbnailprovider.md) демонстрируется реализация обработчика эскизов для нового типа файлов, зарегистрированного с расширением. рецепт. В этом примере показано использование различных API-интерфейсов обработчика эскизов для регистрации серверов модели COM для извлечения эскизов для пользовательских типов файлов. В этом разделе описывается пример кода, который выделяет варианты написания кода и рекомендации.

Обработчик эскиза должен всегда реализовывать [**исумбнаилпровидер**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) в сочетании с одним из следующих интерфейсов:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**иинитиализевиситем**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

Бывают случаи, когда инициализация с помощью потоков невозможна. В сценариях, где обработчик эскизов не реализует [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), он должен отказаться от выполнения в изолированном процессе, когда системный индексатор поместит его по умолчанию при изменении потока. Чтобы отказаться от использования функции изоляции процессов, установите следующее значение реестра.

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

Если вы реализуете [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) и выполняете инициализацию на основе потока, ваш обработчик является более безопасным и надежным. Как правило, отключение изоляции процессов предназначено только для устаревших обработчиков; Избегайте отключения этой функции для любого нового кода. **IInitializeWithStream** должен быть первым выбором интерфейса инициализации везде, где это возможно.

Поскольку файл изображения в образце не внедрен в файл. рецепт и не является частью его файлового потока, в примере используется [**иинитиализевиситем**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) . Реализация метода [**иинитиализевиситем:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) просто передает свои параметры закрытым переменным класса.

[**Исумбнаилпровидер**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) имеет только один метод — «-[**эскиз**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)», который вызывается с самым большим требуемым размером изображения (в пикселях). Хотя параметр называется *CX*, его значение используется как максимальный размер измерений x и y изображения. Если полученный эскиз не является квадратным, то длинная ось будет ограничена *CX* , а пропорции исходного изображения сохраняются.

При возвращении параметр- [**эскиза**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) предоставляет маркер полученного изображения. Он также предоставляет значение, указывающее формат цвета изображения и наличие допустимых данных альфа-канала.

Реализация метода thumbnail в примере начинается с вызова закрытого **\_ GetBase64EncodedImageString** .


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



Тип файла. рецепт — это просто XML-файл, зарегистрированный как уникальное расширение имени файла. Он содержит элемент с именем **Picture** , предоставляющий относительный путь и имя файла изображения, которое будет использоваться в качестве эскиза для данного файла рецепта. Элемент **Picture** состоит из **исходного** атрибута, который задает изображение в кодировке Base 64 и необязательный атрибут **size** .

**Размер** имеет два значения: Малый и крупный. Это позволяет предоставлять несколько узлов **изображений** с отдельными изображениями. Полученное изображение затем зависит от значения максимального размера (*CX*), указанного при вызове функции- [**эскиза**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail). Так как Windows никогда не изменяет размер изображения, размер которого превышает максимальный, для различных разрешений можно предоставить разные образы. Однако для простоты в этом примере атрибут **size** опускается и предоставляется только одно изображение для всех ситуаций.

Метод **\_ GetBase64EncodedImageString** , реализация которого показана здесь, использует api-интерфейсы модель DOM XML (DOM) для получения узла **изображения** . Из этого узла он извлекает изображение из **исходных** данных атрибута.


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



[**Затем передает**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) извлеченную строку в **\_ жетстреамфромстринг**.


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



Метод **\_ жетстреамфромстринг** , для которого показана реализация, которая преобразует закодированное изображение в поток.


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



**А затем** использует интерфейсы API компонента Windows Imaging Component (WIC) для извлечения растрового изображения из потока и получения маркера для этого точечного рисунка. Альфа-информация задана, компонент WIC правильно завершает работу, и метод завершается успешно.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Обработчики эскизов](thumbnail-providers.md)
</dt> <dt>

[Рекомендации по обработке эскизов](thumbnail-provider-guidelines.md)
</dt> <dt>

[**IID \_ ППВ \_ args**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
