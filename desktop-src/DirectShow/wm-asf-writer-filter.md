---
description: Фильтр модуля записи WM ASF
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: Фильтр модуля записи WM ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672996124c88632228fff3a84525c9d47f2276b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155303"
---
# <a name="wm-asf-writer-filter-directshow"></a>Фильтр модуля записи WM ASF (DirectShow)

Модуль записи WM ASF является фильтром оболочки для объекта модуля записи, поставляемого с пакетом SDK Windows Media™ Format. Фильтр принимает переменное число входных потоков и создает файл расширенного формата системы (ASF). Фильтр обрабатывает все сжатие и мультиплексирование (хотя механизм сжатия можно обойти). Модуль записи WM ASF можно использовать в различных сценариях, включая видеозапись цифрового видео (DV), повторное сжатие звука и преобразование Audio-Video файлов мультимедиа с чередованием (AVI) или MPEG для потоковой передачи в сети. Этот фильтр предоставляет единственный способ создания файлов Microsoft® Windows Media™ аудио и Windows Media Video в Microsoft DirectShow.

Дополнительные сведения см. [в разделе Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md).



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Иамфилтермискфлагс**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**иконфигасфвритер**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **испеЦифипропертипажес** Кроме того, фильтр предоставляет следующие интерфейсы пакета SDK Windows Media Format: **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**<br/> |
| Типы носителей входных закрепления                    | Зависит от профиля ASF. Обычно несжатые аудио и видео типы, хотя фильтр принимает сжатые типы, если они соответствуют профилю ASF.                                                                                                                                                                                                                                                                                                                                             |
| Интерфейсы входных закрепления                     | [**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвмбуфферпасс**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** Кроме того, ПИН-код предоставляет следующий интерфейс пакета SDK Windows Media Format: **IWMStreamConfig2** (через **IServiceProvider**).<br/>                                                                                                                                                                                 |
| Типы носителей для выходного ПИН-кода                   | Не применяется                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Интерфейсы выходного ПИН-кода                    | Не применяется                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Фильтровать CLSID                             | \_ВМАСФВРИТЕР CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID страницы свойств                      | \_АСФВРИТЕРПРОПЕРТИЕС CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Исполняемый объект                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Заслуживают](merit.md)                       | \_ \_ не \_ использовать                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Категория фильтра](filter-categories.md) | Не указано                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Комментарии

Для этого фильтра требуется пакет средств разработки программного обеспечения (SDK) Windows Media Format и его зависимые компоненты.

Количество входных ПИН-кодов в фильтре в зависимости от профиля или идентификатора профиля потока ASF.

Входные сигналы поддерживают один метод из интерфейса **иамстреамконфиг** : [**иамстреамконфиг::-Format**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Все остальные методы возвращают E \_ нотимпл. Вызовите метод **OnFormat** , чтобы запросить формат сжатия целевого объекта ПИН-кода, который определяется текущим профилем ASF. Чтобы задать профиль, используйте интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) .

Можно использовать интерфейс **IServiceProvider** фильтра для получения указателя на интерфейс **IWMWriterAdvanced2** , который определен в пакете SDK формата Windows Media. Вы можете использовать интерфейс **IWMWriterAdvanced2** для управления воспроизведением видео при чередовании исходного видео. Чтобы задать режим разчередования, вызовите метод **IWMWriterAdvanced2:: сетинпутсеттинг**. Для параметра *двинпутнум* используйте Отсчитываемый от нуля индекс входного ПИН-кода, перечисленный интерфейсом [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .

В следующем примере показано, как запросить этот интерфейс:


```C++
// Assume that pAsfWriter is a valid IBaseFilter pointer.
IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = pAsfWriter->QueryInterface(
    IID_IServiceProvider, 
    (void**)&pProvider
    );
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(
        IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, 
        (void**)&pWMWA2
        );
    pProvider->Release();
    if (SUCCEEDED(hr))
    {
        // Use pWMWA2. (Not shown.)
        pWMWA2->Release();
    }
}
```



Приложения не должны использовать методы **ивмвритерадванцед** , наследуемые интерфейсом **IWMWriterAdvanced2** . Вызов любых этих методов может интерере с операцией фильтра.

Единственный режим записи в файл, поддерживаемый этим фильтром, — это \_ \_ Перезапись файла. См. раздел [**IFileSinkFilter2:: onmode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

Когда среда выполнения пакета SDK Windows Media Format отправляет \_ сообщения о состоянии ВМТ в фильтр модуля записи WM ASF, фильтр пересылает их в виде событий [**\_ \_ событий EC ВМТ**](ec-wmt-event.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 




