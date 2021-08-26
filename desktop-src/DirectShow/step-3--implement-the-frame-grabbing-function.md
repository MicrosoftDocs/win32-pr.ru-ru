---
description: Шаг 3. Реализация функции Frame-Grabbing
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Шаг 3. Реализация функции Frame-Grabbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75410c48765e9437cd328a220ccbecf2c207bdaae5242a9e41060bc13fa02eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904102"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a>Шаг 3. Реализация функции Frame-Grabbing

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

В этом разделе описан шаг 3 из [фрагмента плаката](grabbing-a-poster-frame.md).

Следующим шагом является реализация функции GetNext, которая использует средство обнаружения мультимедиа для получения афиши. Внутри этой функции выполните следующие действия.

1.  Создайте средство обнаружения мультимедиа.
2.  Укажите файл мультимедиа.
3.  Проверьте каждый поток в файле. Если это поток видео, получите собственные размеры видео.
4.  Получите рамку афиши, указав время поиска и целевое измерение.

Создайте объект детектора мультимедиа, вызвав [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



Укажите имя файла с помощью метода [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) . Этот метод принимает параметр **BSTR** .


```C++
hr = pDet->put_Filename(bstrFilename);
```



Получение числа потоков и цикл по каждому потоку, который проверяет тип носителя. Метод [**имедиадет:: Get \_ аутпутстреамс**](imediadet-get-outputstreams.md) извлекает количество потоков, а метод [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md) указывает, какой поток следует проверить. Завершите цикл в первом видеопотоке.


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



Если поток видео не найден, функция завершает работу.

В приведенном выше коде метод [**имедиадет:: Get \_ стреамтипе**](imediadet-get-streamtype.md) ВОЗВРАЩАЕТ только основной GUID типа. Это удобно, если не нужно проверять полный тип носителя. Однако для получения измерений видео необходимо проверить блок формата, чтобы в нем требовался полный тип носителя. Это можно получить, вызвав метод [**имедиадет:: Get \_ стреаммедиатипе**](imediadet-get-streammediatype.md) , который заполняет структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Средство обнаружения мультимедиа преобразует все видеопотоки в несжатый формат с помощью блока формата [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



Метод [**Get \_ стреаммедиатипе**](imediadet-get-streammediatype.md) выделяет блок формата, который вызывающий объект должен освободить. В этом примере используется функция [**фримедиатипе**](freemediatype.md) из библиотеки базовых классов.

Теперь все готово для получения рамки афиши. Сначала вызовите метод [**имедиадет:: жетбитмапбитс**](imediadet-getbitmapbits.md) с **пустым** указателем для буфера:


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



Этот вызов возвращает необходимый размер буфера в параметре *лсизе* . Первый параметр задает время потока для поиска; в этом примере используется нулевое значение времени. Для ширины и высоты в этом примере используются собственные измерения видео, полученные ранее. Если указать другие значения, то средство обнаружения мультимедиа растягивает точечный рисунок для соответствия.

Если метод выполнен, выделите буфер и снова вызовите [**жетбитмапбитс**](imediadet-getbitmapbits.md) :


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



Ниже приведена полная функция с более лучшей обработкой ошибок.


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



Далее: [Шаг 4. Рисование точечного рисунка в клиентской области](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Зафрагментировать рамку афиши](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
