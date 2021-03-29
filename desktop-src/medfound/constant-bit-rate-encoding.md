---
description: Кодирование постоянной скорости потока
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Кодирование постоянной скорости потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990839"
---
# <a name="constant-bit-rate-encoding"></a>Кодирование постоянной скорости потока

При кодировании с постоянной скоростью (CBR) кодировщик знает скорость потока примеров выходного носителя и окно буфера (параметры утечки) перед началом сеанса кодирования. Кодировщик использует одинаковое количество битов для кодирования каждой секунды в течение файла, чтобы достичь целевой скорости потока. Это ограничивает изменение размера образцов потока. Кроме того, во время сеанса кодирования скорость потока не совпадает с заданным значением, но остается близкой к целевой скорости.

Кодирование CBR полезно, если вам нужно узнать битрейт или примерную длительность файла, не анализируя весь файл. Это необходимо в сценариях потоковой передачи, когда содержимое мультимедиа должно передаваться с прогнозируемым битрейтом и постоянной пропускной способностью.

Недостаток кодировки CBR заключается в том, что качество закодированного содержимого не будет постоянным. Поскольку часть содержимого сложнее сжимать, части потока CBR будут иметь более низкую качество, чем другие. Например, типичный фильм содержит несколько сцен, которые довольно статичны, и некоторые сцены, которые являются полными действиями. При кодировании фильма с помощью CBR сцены, которые являются статическими и, следовательно, легко кодируются эффективно, будут иметь более высокое качество, чем сцены действий, для которых требуется более высокие размеры выборки, чтобы обеспечить одинаковое качество.

Как правило, вариации в качестве файла CBR более производятся с более низкими скоростями. При более высоких скоростях качество файла с CBR по-прежнему будет отличаться, но проблемы с качеством будут менее заметны для пользователя. При использовании кодировки CBR следует задать высокую пропускную способность так, как это разрешено в сценарии доставки.

-   [Параметры конфигурации CBR](#cbr-configuration-settings)
-   [Параметры неутечек сегментов](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a>Параметры конфигурации CBR

Необходимо настроить кодировщик, указав тип кодировки и различные параметры конкретного потока перед сеансом кодирования.

**Настройка кодировщика для кодирования CBR**

1.  Укажите режим кодирования CBR.

    По умолчанию кодировщик настроен на использование кодировки CBR. Конфигурация кодировщика задается с помощью значений свойств. Эти свойства определены в вмкодекдсп. h. Этот режим можно задать явным образом, задав для свойства [**мфпкэй \_ ВБРЕНАБЛЕД**](mfpkey-vbrenabledproperty.md) значение Variant \_ false. Дополнительные сведения о настройке свойств кодировщиков см. в разделе [Настройка кодировщика](configuring-the-encoder.md).

2.  Выберите скорость кодирования.

    Для кодировки CBR необходимо знание скорости потока, с которой необходимо кодировать поток перед началом сеанса кодирования. Скорость потока во время настройки кодировщика должна быть задана. Для этого во время согласования типа мультимедиа проверьте атрибут " [**\_ \_ \_ Среднее \_ число байт \_ в \_ секунду MF-MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) " (для звуковых потоков) или атрибут " [**\_ \_ Средняя \_ скорость" MF-MT**](mf-mt-avg-bitrate-attribute.md) (для видеопотоков) доступных типов выходных данных и выберите тип выходного носителя с средней скоростью, ближайшей к целевой скорости, которую вы хотите достичь. Дополнительные сведения см. [в разделе Согласование типа носителя в кодировщике](media-type-negotiation-on-the-encoder.md).

В следующем примере кода показана реализация для Сетенкодингпропертиес. Эта функция задает свойства кодирования на уровне потока для CBR и VBR.


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a>Параметры неутечек сегментов

Для кодировки CBR среднее и максимальное значения сегмента утечки для потока одинаковы. Дополнительные сведения об этих параметрах см. [в разделе Модель буфера для сегмента утечки](the-leaky-bucket-buffer-model.md).

Чтобы CBR звуковые потоки, необходимо задать значения сегментов утечки после согласования типа выходного носителя в кодировщике. Кодировщик вычисляет окно буфера внутренне на основе средней скорости, заданной для выходного типа носителя.

Чтобы задать значения сегментов с утечкой, создайте массив значений типа DWORD. в [**мфпкэй \_ асфстреамсинк \_ Исправлено свойство \_ леакибуккет**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) в хранилище свойств приемника мультимедиа. Дополнительные сведения см. [в разделе Установка свойств в приемнике файла](setting-properties-in-the-file-sink.md).

-   Средняя скорость потока: Возвращает среднюю скорость потока из типа выходного носителя, выбранного во время согласования типа носителя. Используйте атрибут [**" \_ \_ \_ Среднее \_ число байтов со \_ \_ звуком MF в секунду**](mf-mt-audio-avg-bytes-per-second-attribute.md) ".
-   Окно буфера. запросите кодировщик для интерфейса [**ивмкодеклеакибуккет**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) , а затем вызовите [**Ивмкодеклеакибуккет:: жетбуфферсизебитс**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (вмкодеЦифацес. h, вмкодекдспууид. lib).
-   Начальный размер буфера: значение 0.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы кодирования ASF](asf-encoding-types.md)
</dt> <dt>

[Учебник. 1. Передача кодирования мультимедиа Windows](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Руководство. запись файла WMA с помощью CBR Encoding](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
