---
description: Задание свойств сжатия видео
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Задание свойств сжатия видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3f1d73d27acb99e5a197ec4501411669278a6fd5c7b857875141d8831c7173f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583284"
---
# <a name="setting-video-compression-properties"></a>Задание свойств сжатия видео

Фильтры сжатия видео могут поддерживать интерфейс [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) на выходных контактах. Этот интерфейс используется для задания свойств сжатия, таких как частота ключевых кадров, число прогнозируемых кадров (P) на опорный кадр и относительное качество сжатия.

Сначала вызовите метод [**ибасефилтер:: енумпинс**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , чтобы найти ПИН-код вывода фильтра, и запросите ПИН-код для интерфейса. Некоторые фильтры могут вообще не поддерживать интерфейс. Другие могут предоставлять интерфейс, но не поддерживают все свойства сжатия. Чтобы определить, какие свойства поддерживаются, вызовите [**иамвидеокомпрессион:: info**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Этот метод возвращает несколько фрагментов информации:

-   Набор флагов возможностей
-   Строка описательной строки и номера версии
-   Значения по умолчанию для частоты ключевых кадров, P-частоты кадров и качества (если поддерживается)

Метод имеет следующий синтаксис:


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



Параметры *псзверсион* и *псздеск* — это буферы расширенных символов, которые получают строку версии и строку описания. Параметры *кбверсион* и *кбдеск* получают требуемые размеры буфера в байтах (не в символах). Параметры *лкэйфраме*, *лпфраме* и *дблкуалити* получают значения по умолчанию для частоты ключевых кадров, P частоты кадров и качества. Качество выражается в виде числа с плавающей запятой от 0,0 до 1,0. Параметр *лкап* получает битовую операцию **или** для флагов возможностей, которые определяются перечисляемым типом [**компрессионкапс**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) .

Любой из этих параметров может иметь **значение NULL**, в этом случае метод игнорирует этот параметр. Например, чтобы выделить буферы для строк версии и описания, сначала вызовите метод со **значением NULL** в первом и третьем параметрах. Используйте возвращаемые значения для *кбверсион* и *кбдеск* , чтобы выделить буферы, а затем снова вызовите метод:


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



Значение *лкап* указывает, какие из других методов **иамвидеокомпрессион** поддерживаются фильтром. Например, если *лкап* содержит \_ флаг компрессионкапс канкэйфраме, можно вызвать [**иамвидеокомпрессион:: Get \_ кэйфрамерате**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) , чтобы получить частоту ключевых кадров и [**иамвидеокомпрессион::p UT \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) , чтобы установить частоту ключевых кадров. Отрицательное значение указывает, что фильтр будет использовать значение по умолчанию, полученное из [**иамвидеокомпрессион::-info**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Пример:


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



В следующем примере кода предпринимается попытка найти интерфейс **иамвидеокомпрессион** на выходном ПИН-коде. Если он будет выполнен, он извлекает значения по умолчанию и фактические данные для свойств сжатия:


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> Если для построения графа используется интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , можно получить интерфейс **иамвидеокомпрессион** , вызвав [**ICaptureGraphBuilder2:: Финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)вместо **ибасефилтер:: енумпинс**. Метод **финдинтерфаце** — это вспомогательный метод, который ищет в графе фильтры и ПИН-коды для указанного интерфейса.

 

 

 



