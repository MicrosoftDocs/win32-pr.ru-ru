---
description: Кодировщик записывает данные изображения в поток. Кодировщики могут сжимать, шифровать и изменять пиксели изображения несколькими способами перед их записью в поток.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Общие сведения о кодировке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f938e184dee7fd9b3e5348365550615ee28de70d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549489"
---
# <a name="encoding-overview"></a>Общие сведения о кодировке

Кодировщик записывает данные изображения в поток. Кодировщики могут сжимать, шифровать и изменять пиксели изображения несколькими способами перед их записью в поток. Использование некоторых кодировщиков приводит к компромиссам (например, JPEG), который меняет цветовую информацию для улучшения сжатия. Другие кодировщики не приводят к таким потерям, например к точечному рисунку (BMP). Так как многие кодеки используют собственные технологии для достижения лучшего сжатия и точности изображений, сведения о кодировании образа являются разработчиком кодека.

Этот раздел включает следующие подразделы:

-   [ивикбитмапенкодер](#iwicbitmapencoder)
-   [ивикбитмапфраминкоде](#iwicbitmapframeencode)
-   [Пример кодировки TIFF](#tiff-encoding-example)
-   [Использование параметров кодировщика](#encoder-options-usage)
-   [Параметры кодировщика](#encoder-options-usage)
-   [Примеры параметров кодировщика](#encoder-options-examples)
-   [Связанные темы](#related-topics)

## <a name="iwicbitmapencoder"></a>ивикбитмапенкодер

[**Ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) является основным интерфейсом для кодирования изображения в целевой формат и используется для сериализации компонентов изображения, таких как Thumbnail ([**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) и Frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), в файл изображения.

Как и когда происходит сериализация, остается разработчиком кодека. Каждый отдельный блок данных в целевом формате файла должен быть задан независимо от порядка, но опять же, это решение разработчика кодека. Однако после вызова метода [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) изменения в образ не должны быть разрешены и поток должен быть закрыт.

## <a name="iwicbitmapframeencode"></a>ивикбитмапфраминкоде

[**Ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) — это интерфейс для кодирования отдельных кадров изображения. Он предоставляет методы для установки отдельных компонентов создания образов кадров, например эскизов и кадров, а также размеров изображений, точек на дюйм и форматов пикселей.

Отдельные кадры могут быть закодированы с помощью метаданных, связанных с кадром, поэтому [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) предоставляет доступ к модулю записи метаданных с помощью метода [**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .

Метод [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) кадра фиксирует все изменения в отдельном кадре и указывает, что изменения в этом кадре больше не должны приниматься.

## <a name="tiff-encoding-example"></a>Пример кодировки TIFF

В следующем примере изображение в формате TIFF кодируется с помощью [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) и [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). Выход TIFF настраивается с помощью [**виктиффкомпрессионоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) , а кадр растрового изображения инициализируется с использованием заданных параметров. После создания образа с помощью [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)кадр фиксируется путем [**фиксации**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) , а образ сохраняется с помощью [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride***/;
    UINT cbBufferSize = uiHeight * cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a>Использование параметров кодировщика

Различные кодировщики для разных форматов должны предоставлять различные параметры кодирования изображения. Компонент Windows Imaging Component (WIC) предоставляет единообразный механизм, позволяющий определить, требуются ли параметры кодировки, не требуя, чтобы приложения работали с несколькими кодировщиками, не зная определенного формата. Это достигается путем предоставления параметра [ипропертибаг](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) для метода [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) и метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .

Фабрика компонентов предоставляет простую точку для создания контейнера свойств параметров кодировщика. Кодеки могут использовать эту службу, если необходимо предоставить простой, интуитивно понятный и неконфликтующий набор параметров кодировщика. Во время создания контейнер свойств Imaging должен быть инициализирован во всех параметрах кодировщика, относящихся к этому кодеку. Для параметров кодировщика из канонического набора диапазон значений будет применен при записи. Для более сложных потребностей кодеки должны написать собственную реализацию контейнера свойств.

Приложению предоставляется набор параметров кодировщика во время создания кадра и перед инициализацией фрейма кодировщика должны быть настроены все значения. Для приложения, управляемого пользовательским интерфейсом, оно может предоставлять стандартный пользовательский интерфейс для канонических параметров кодировщика и расширенное представление для остальных параметров. Изменения могут выполняться по одному за раз с помощью метода Write, и любая ошибка будет передаваться через Иеррорлог. Приложение пользовательского интерфейса всегда должно повторно считаться и отображать все параметры после внесения изменений в случае, если изменение привело к каскадному применению. Приложение должно быть подготовлено к обработке ошибок инициализации кадров для кодеков, которые предоставляют минимальный отчет об ошибках через контейнер свойств.

## <a name="encoder-options"></a>Параметры кодировщика

Приложение может столкнуться со следующим набором параметров кодировщика. Параметры кодировщика соответствуют возможностям кодировщика и базовому формату контейнера, поэтому их характер не зависит от кодека. По возможности новые параметры должны быть нормализованы, чтобы их можно было применить к новым кодекам.



| Имя свойства      | VARTYPE  | Применение                                                                     | Применимые кодеки |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| ImageQuality       | VT \_ R4   | 0 – 1,0                                                                     | JPEG, Хдфото     |
| CompressionQuality | VT \_ R4   | 0 – 1,0                                                                     | TIFF              |
| Lossless           | Логическое значение VT \_ | **true**, **false**                                                       | хдфото           |
| битмаптрансформ    | VT \_ UI1  | [**викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | JPEG              |



 

Имажекуалти в 0,0 означает наименьшую возможную точность и 1,0 означает максимальную достоверность, которая может также означать потери данных в зависимости от кодека.

Компрессионкуалити 0,0 означает, что наименее эффективная доступная схема сжатия, как правило, приводит к быстрой кодировке, но большему результату. Значение 1,0 означает, что самая эффективная схема доступна, обычно занимает больше времени для кодирования, но создает небольшие выходные данные. В зависимости от возможностей кодека этот диапазон может быть сопоставлен с дискретным набором доступных методов сжатия.

Без потерь означает, что кодек кодирует изображение как безотносительное без потери данных изображения. Если включено безпотерь, Имажекуалити игнорируется.

В дополнение к приведенным выше универсальным параметрам кодировщика кодеки, предоставляемые с помощью WIC, поддерживают следующие параметры. Если кодек должен поддерживать параметр, который согласуется с использованием этих кодеков, рекомендуется сделать это.



| Имя свойства           | VARTYPE           | Применение                                                                             | Применимые кодеки |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| InterlaceOption         | Логическое значение VT \_          | Вкл./выкл.                                                                            | PNG               |
| FilterOption            | VT \_ UI1           | [**викпнгфилтероптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | PNG               |
| TiffCompressionMethod   | VT \_ UI1           | [**виктиффкомпрессионоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | TIFF              |
| Luminance               | VT \_ UI4/VT \_ | 64 записей (ДКТ)                                                                  | JPEG              |
| Chrominance             | VT \_ UI4/VT \_ | 64 записей (ДКТ)                                                                  | JPEG              |
| JpegYCrCbSubsampling    | VT \_ UI1           | [**викжпегикркбсубсамплингоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | JPEG              |
| SuppressApp0            | Логическое значение VT \_          |                                                                                   | JPEG              |
| EnableV5Header32bppBGRA | Логическое значение VT \_          | Вкл./выкл.                                                                            | BMP               |



 

Используйте **VT \_ Empty** , чтобы **\* не задавать \*** значение по умолчанию. Если дополнительные свойства заданы, но не поддерживаются, кодировщику следует игнорировать их. Это позволяет приложениям создавать код с меньшей логикой, если требуется возможность, которая может отсутствовать или отсутствовать.

## <a name="encoder-options-examples"></a>Примеры параметров кодировщика

В приведенном выше [примере кодировки TIFF](#tiff-encoding-example) задан параметр кодировщика. Элементу *пстрнаме* структуры PROPBAG2 присваивается соответствующее имя свойства, а для варианта устанавливается соответствующий VarType и требуемое значение — в данном случае является членом перечисления [**виктиффкомпрессионоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) .


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



Чтобы использовать параметры кодировщика по умолчанию, просто инициализируйте кадр точечного рисунка с контейнером свойств, возвращенным при создании кадра.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



Кроме того, можно исключить контейнер свойств, когда не будут рассматриваться параметры кодировщика.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Общие сведения о декодировании](-wic-creating-decoder.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
