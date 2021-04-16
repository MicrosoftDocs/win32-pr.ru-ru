---
description: Просмотр скрытых субтитров
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Просмотр скрытых субтитров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566664"
---
# <a name="viewing-closed-captions"></a>Просмотр скрытых субтитров

Для поддержки субтитров в аналоговом телевизоре фильтр записи предоставляет ПИН-код, который доставляет либо ВБИ, либо закрытые данные субтитров. ПИН-код будет иметь одну из следующих категорий ПИН-кода:

-   ВБИ (закрепить \_ категорию \_ ВБИ). Доставляет поток примеров ВБИ волны. Они передаются в фильтр декодера, который извлекает данные о закрытых субтитрах.
-   ПИН-код копии (закрепить \_ категорию \_ CC). Предоставляет пары байтов закрытых субтитров, извлеченные из данных строки 21.
-   Аппаратное копирование ПИН-кода для создания среза копии (ПИННАМЕ \_ видео \_ CC \_ ).

Чтобы предварительно просмотреть скрытые субтитры, вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) с категорией ВБИ PIN. Если это не удается, вызовите его снова с помощью категории CC.


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



На следующей диаграмме показан типичный граф фильтра для отображения закрытых субтитров.

![Диаграмма предварительного просмотра скрытых субтитров](images/vidcap08.png)

Эта диаграмма использует следующие фильтры для отображения скрытых субтитров:

-   [Преобразователь tee/Sink-to-Sink](tee-sink-to-sink-converter.md). Принимает сведения ВБИ из фильтра записи и разделяет их на отдельные потоки для каждой из служб данных, имеющихся в сигнале. Корпорация Майкрософт предоставляет кодеки ВБИ для скрытых титров, НАБТС и стандартных телетекстов (WST).
-   [Декодер CC](cc-decoder-filter.md). Декодирует данные CC из образцов аудио ВБИ, предоставленных фильтром записи.
-   [Декодер 21 Line](line-21-decoder-filter.md). Преобразует пары байтов копии и рисует текст заголовка на точечные рисунки. Нисходящий фильтр (в данном случае микшер наложения) накладывает на видео растровые изображения.

Метод [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) в построителе графов записи добавляет эти фильтры автоматически. Если фильтр записи имеет ПИН-код CC, а не ВБИ ПИН-код, то ПИН-код CC подключается непосредственно к фильтру декодера Line 21.

> [!Note]  
> Если для подготовки к просмотру используется фильтр формирователя видео (VMR), используйте строку 21 декодер Filter 2. Этот фильтр имеет те же функциональные возможности, что и Line 21 декодер, но идентификатором CLSID является CLSID \_ Line21Decoder2.

 

> [!Note]  
> Фильтр декодера CC был удален в Windows Vista. Новые приложения должны использовать фильтр Вбикодек, который описан в документации по технологиям Microsoft TV.

 

Если устройство записи использует порт видео, фильтр записи может иметь ПИН-код ВБИ ( \_ Категория \_ видеопорт \_ ВБИ). Этот ПИН-код должен быть подключен к фильтру [распределителя ВБИ Surface](vbi-surface-allocator.md) , который выделяет поверхности для хранения захваченных данных ВБИ. Метод [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) добавляет этот фильтр, если он необходим. На следующей схеме показан граф фильтра с распределительной поверхностью ВБИ.

![Диаграмма предварительного просмотра субтитров с распределительной поверхностью ВБИ](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>Включение и отключение заголовков

Для управления отображением субтитров используйте интерфейс [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) в фильтре Line 21. Например, можно отключить отображение субтитров с помощью метода [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) следующим образом:


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



В этом примере используется метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) для размещения интерфейса [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) . Первый параметр для **финдинтерфаце** **&выглядеть \_ \_ только по нисходящей**, который указывает, что нужно искать дальше от фильтра записи (*ПКАП*).

### <a name="capturing-closed-caption-bitmaps"></a>Запись растровых изображений скрытых заголовков

Точечные рисунки заголовков можно записать в файл. Для этого добавьте раздел "запись файлов" графа фильтра, как описано в разделе [запись видео в файл](capturing-video-to-a-file.md). Затем отрисовываете ПИН-код CC или ВБИ в фильтре мультиплексора:


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



Если вы также записываете видео, будет создан файл с двумя отдельными видеопотоками. Видео с субтитрами, наложенными поверх изображения, не записываются.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Субтитры и телетекст](closed-captions-and-teletext.md)
</dt> </dl>

 

 



