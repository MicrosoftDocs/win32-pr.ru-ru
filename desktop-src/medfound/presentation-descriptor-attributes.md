---
description: Атрибуты дескриптора представления
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: Атрибуты дескриптора представления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bba97a0e0428bf2ceb91b04c79f69b557876a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543831"
---
# <a name="presentation-descriptor-attributes"></a>Атрибуты дескриптора представления

## <a name="common-presentation-descriptor-attributes"></a>Общие атрибуты дескриптора представления

К любому дескриптору презентации могут применяться следующие атрибуты.



| attribute                                                                          | Описание                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ контекст приложения MF \_ PD**](mf-pd-app-context-attribute.md)                        | Содержит указатель на дескриптор представления из защищенного пути к носителю (PMP).                                                          |
| [**\_ \_ \_ скорость кодирования MF PD \_**](mf-pd-audio-encoding-bitrate-attribute.md) | Указывает скорость кодирования звука для презентации в битах в секунду.                                                                 |
| [\_АУДИОРАЗЪЕМ MF PD \_ Audio \_ исвариаблебитрате](mf-pd-audio-isvariablebitrate.md)              | Указывает, имеют ли звуковые потоки в презентации переменную скорость.                                                               |
| [**\_Длительность MF PD \_**](mf-pd-duration-attribute.md)                               | Указывает длительность презентации в единицах 100-наносекундных.                                                                              |
| [**\_ \_ \_ время последнего изменения \_ MF PD**](mf-pd-last-modified-time-attribute.md)         | Указывает время последнего изменения презентации.                                                                                                |
| [**\_ \_ тип MIME MF \_ PD**](mf-pd-mime-type-attribute.md)                            | Указывает тип MIME содержимого.                                                                                                         |
| [\_ \_ время воспроизведения MF \_ PD \_](mf-pd-playback-boundary-time.md)               | Время, когда должна начаться презентация, относительно начала источника мультимедиа.                                                       |
| [\_ \_ \_ ИД элемента воспроизведения MF \_ PD](mf-pd-playback-element-id.md)                     | Идентификатор элемента списка воспроизведения в презентации.                                                                                     |
| [**\_ \_ контекст пмфост MF \_ PD**](mf-pd-pmphost-context-attribute.md)                | Содержит указатель на прокси-объект для дескриптора представления приложения.                                                           |
| [\_ \_ предпочтительный язык MF PD \_](mf-pd-preferred-language.md)                        | Содержит предпочитаемый язык RFC 1766 для источника мультимедиа.                                                                                   |
| [**MF \_ PD \_ саамский \_ стилелист**](mf-pd-sami-stylelist-attribute.md)                  | Содержит понятное имя поддерживаемых стилей обмена доступными мультимедийными данными (SAMI). Этот атрибут применяется только к файлам SAMI. |
| [**\_ \_ Общий \_ \_ Размер файла для MF PD**](mf-pd-total-file-size-attribute.md)               | Задает общий размер исходного файла в байтах.                                                                                          |
| [**\_ \_ \_ скорость кодирования видео MF \_ PD**](mf-pd-video-encoding-bitrate-attribute.md) | Указывает скорость кодирования видео для презентации в битах в секунду.                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>Атрибуты дескриптора представления для ASF

Следующие атрибуты применяются к дескрипторам представления для файлов ASF.



| attribute                                                                                                             | Описание                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**MF \_ PD \_ ASF \_ кодеклист**](mf-pd-asf-codeclist-attribute.md)                                                       | Содержит сведения о кодеках, используемых для кодирования содержимого в файле ASF.                     |
| [**MF \_ PD \_ ASF \_ контентенкриптион \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | Указывает идентификатор ключа для зашифрованного файла ASF.                                              |
| [**\_ \_ \_ \_ \_ URL-адрес лицензии MF PD ASF контентенкриптион**](mf-pd-asf-contentencryption-license-url-attribute.md)             | Указывает URL-адрес для получения лицензии на зашифрованный файл ASF.                                     |
| [**\_ \_ \_ \_ секретные данные MF PD ASF контентенкриптион \_**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | Содержит секретные данные для зашифрованного файла ASF.                                                      |
| [**\_ \_ \_ тип контентенкриптион MF PD \_ ASF**](mf-pd-asf-contentencryption-type-attribute.md)                            | Указывает тип механизма защиты, используемого в файле ASF.                                      |
| [**MF \_ PD \_ ASF \_ контентенкриптионекс \_ \_ данные шифрования**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | Содержит данные шифрования для файла ASF.                                                            |
| [**\_ \_ \_ Длина данных ASF (MF PD) \_**](mf-pd-asf-data-length-attribute.md)                                                  | Задает размер (в байтах) раздела данных в файле ASF.                                    |
| [**\_ \_ \_ \_ Начальное \_ смещение данных в формате MF PD ASF**](mf-pd-asf-data-start-offset-attribute.md)                                     | Указывает смещение в байтах от начала файла ASF до начала первого пакета данных. |
| [**\_ \_ \_ \_ время создания филепропертиес MF PD \_ ASF**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | Указывает дату и время первоначального создания ASF.                                  |
| [**MF \_ PD \_ ASF \_ филепропертиес \_ File \_ ID**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | Указывает идентификатор файла ASF.                                                        |
| [**\_ \_ \_ Флаги филепропертиес MF PD ASF \_**](mf-pd-asf-fileproperties-flags-attribute.md)                                | Содержит различные флаги из заголовка ASF.                                                     |
| [**MF \_ PD \_ ASF \_ филепропертиес \_ Максимальная \_ скорость**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | Указывает максимальную скорость мгновенного разряда (в битах в секунду) для файла ASF.                   |
| [**\_пакет MF PD \_ ASF \_ филепропертиес \_ максимальный \_ \_ Размер пакета**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | Указывает максимальный размер пакета (в байтах) для файла ASF                                         |
| [**MF \_ PD \_ ASF \_ филепропертиес \_ , \_ Минимальный \_ Размер пакета**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | Указывает минимальный размер пакета (в байтах) для файла ASF.                                        |
| [**\_пакеты MF PD \_ ASF \_ филепропертиес \_**](mf-pd-asf-fileproperties-packets-attribute.md)                            | Указывает число пакетов в разделе данных файла ASF.                                  |
| [**\_ \_ \_ длительность воспроизведения MF филепропертиес \_ ASF \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | Указывает время, необходимое для воспроизведения ASF-файла в единицах с 100 нс.                              |
| [**\_ФИЛЕПРОПЕРТИЕС MF \_ \_ \_**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | Указывает время, в течение которого данные помещаются в буфер, прежде чем начнется воспроизведение файла ASF (в миллисекундах).    |
| [**\_период отправки MF PD \_ ASF \_ филепропертиес \_ \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | Указывает время, необходимое для отправки ASF-файла в единицах с 100 нс.                              |
| [**MF \_ PD \_ ASF \_ \_ содержит \_ аудио**](mf-pd-asf-info-has-audio-attribute.md)                                           | Указывает, содержит ли ASF файл по крайней мере один звуковой поток.                                    |
| [**MF \_ PD \_ ASF \_ \_ содержит \_ не \_ аудио \_ видео**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | Указывает, содержит ли ASF-файл любые незвуковые потоки, не являющиеся видеопотоками.                             |
| [**\_канал MF \_ PD \_ ASF \_ содержит \_ видео**](mf-pd-asf-info-has-video-attribute.md)                                           | Указывает, содержит ли ASF файл по крайней мере один видеопоток.                                    |
| [**MF \_ PD \_ ASF \_ ланглист**](mf-pd-asf-langlist-attribute.md)                                                         | Указывает список языков, используемых в файле ASF.                                                 |
| [MF \_ PD \_ ASF \_ ланглист \_ легациордер](mf-pd-asf-langlist-legacyorder.md)                                              | Содержит список языков RFC 1766, используемых в текущей презентации.                              |
| [**\_маркер MF PD \_ ASF \_**](mf-pd-asf-marker-attribute.md)                                                             | Задает маркеры в файле ASF.                                                                |
| [**MF \_ PD \_ \_ метаданные ASF \_ — \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | Указывает, использует ли ASF-файл кодирование с переменной скоростью (VBR).                                 |
| [**MF \_ PD \_ . \_ \_ \_ пары контейнеров с утечкой метаданных ASF \_**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | Описывает требования к буферизации для ASF-файла VBR.                                             |
| [**MF \_ PD \_ ASF \_ метаданные \_ V8 \_ буфферавераже**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | Указывает средний размер буфера, необходимый для файла в формате VBR.                                         |
| [**MF \_ PD \_ ASF \_ метаданные \_ V8 \_ вбрпеак**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | Указывает максимальную скорость потока в ASF-файле VBR.                                          |
| [**\_Скрипт MF PD \_ ASF \_**](mf-pd-asf-script-attribute.md)                                                             | Задает команды сценария в файле ASF.                                                        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Дескрипторы представления](presentation-descriptors.md)
</dt> <dt>

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



