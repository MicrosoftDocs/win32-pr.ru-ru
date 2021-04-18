---
description: Quality-Based кодирование переменной скорости
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Quality-Based кодирование переменной скорости
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692585"
---
# <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based кодирование переменной скорости

В отличие от [кодирования с постоянной скоростью потока](constant-bit-rate-encoding.md) (CBR), когда кодировщик стремится поддерживать определенную скорость потока закодированного носителя, в режиме переменной скорости (VBR) кодировщик стремится достичь наилучшего возможного качества закодированного носителя. Основное различие между CBR и VBR — размер используемого окна буфера. Потоки с кодированием VBR обычно имеют большие окна буфера по сравнению с потоками, закодированными CBR.

Качество закодированного содержимого определяется объемом данных, потерянных при сжатии содержимого. На потери данных в процессе сжатия влияют многие факторы. но, как правило, чем сложнее исходные данные, тем выше степень сжатия, тем больше сведений теряется в процессе сжатия.

В режиме VBR на основе качества не следует определять скорость потока или окно буфера, которое должен выполнять кодировщик. Вместо этого следует указать уровень качества для потока цифрового мультимедиа, а не скорость. Кодировщик сжимает содержимое, чтобы все выборки были сравнимы по качеству. Это гарантирует, что качество будет согласовано на протяжении всего времени воспроизведения независимо от требований к буферу результирующего потока.

Для кодирования VBR на основе качества обычно создаются большие сжатые потоки. Как правило, этот тип кодирования хорошо подходит для локального воспроизведения или для сетевых подключений с высокой пропускной способностью (или для загрузки и воспроизведения). Например, можно написать приложение для копирования песен из компакт-диска в файлы ASF на компьютере. Использование кодирования VBR на основе качества гарантирует, что все песни будут иметь одинаковое качество. В таких случаях последовательное качество обеспечит лучшую работу пользователей.

Недостатком кодирования VBR на основе качества является то, что на самом деле нет способа получить сведения о размере или пропускной способности закодированного носителя перед сеансом кодирования, так как кодировщик использует один проход кодирования. Это может сделать файлы в кодировке с поддержкой VBR в случаях, когда ограничена память или пропускная способность, например воспроизведение содержимого на портативных проигрывателях мультимедиа или потоковая передача по сети с низкой пропускной способностью.

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a>Настройка кодировщика для кодирования Quality-Based VBR

Конфигурация кодировщика задается с помощью значений свойств. Эти свойства определены в вмкодекдсп. h. Перед согласованием типа выходного носителя необходимо установить свойства конфигурации в кодировщике. Дополнительные сведения о настройке свойств кодировщика см. в разделе [Настройка кодировщика](configuring-the-encoder.md).

В следующем списке перечислены свойства, которые необходимо задать для этого типа кодирования.

-   Укажите режим кодирования VBR, задав для свойства **мфпкэй \_ ВБРЕНАБЛЕД** значение Variant \_ true.
-   Присвойте параметру **\_ пассесусед мфпкэй** значение 1, так как в этом режиме используется один проход кодирования.
-   Задайте требуемый уровень качества (от 0 до 100), задав **мфпкэй \_ требуемое свойство \_ вбркуалити** . На основе качества VBR содержимое не кодируется в какие-либо предопределенные параметры буфера. Этот уровень качества, который будет поддерживаться для всего потока, независимо от требований к битовой скорости.
-   Для видеопотоков задайте для параметра средняя скорость потока значение ненулевого значения в атрибуте с [**\_ \_ средним \_ значением скорости MF MT**](mf-mt-avg-bitrate-attribute.md) для типа выходного носителя кодировщика. Точная скорость потока обновляется после завершения сеанса кодирования.

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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы кодирования ASF](asf-encoding-types.md)
</dt> </dl>

 

 



