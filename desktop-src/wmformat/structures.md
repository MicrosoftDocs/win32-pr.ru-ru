---
title: Структуры пакета SDK для формата Windows Media
description: Структуры пакета SDK для формата Windows Media
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- Windows Media Format SDK, структуры
- Расширенный системный формат (ASF), структуры
- ASF (Расширенный системный формат), структуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f730ba3cbc5bd8bbec2a9f01c72df1fe46f0b64
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691742"
---
# <a name="windows-media-format-sdk-structures"></a>Структуры пакета SDK для формата Windows Media

Пакет SDK для формата Windows Media реализует следующие структуры.



| Структура                                                                                | Описание                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ОПЛ копирования \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | Содержит сведения об уровне защиты выходных данных, которые применяются к действию копирования в лицензии DRM.                                                                               |
| [**\_ \_ данные состояния лицензии \_ DRM**](drm-license-state-data.md)                              | Содержит сведения о [*лицензиях*](wmformat-glossary.md) указанного права на управление [*цифровыми правами*](wmformat-glossary.md) . |
| [**\_минимальные \_ \_ уровни защиты выходных \_ данных DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | Содержит минимальные уровни защиты выходных данных, необходимые лицензии DRM для воспроизведения содержимого в различных форматах.                                                                      |
| [**\_ \_ идентификаторы выходных данных ОПЛ DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | Содержит массив идентификаторов технологии DRM. Эта структура используется для определения групп технологий в других структурах DRM.                                            |
| [**DRM \_ Play \_ ОПЛ**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | Содержит сведения об уровне защиты выходных данных, которые применяются к действию Play в лицензии DRM.                                                                               |
| [**\_идентификатор содержимого списка воспроизведения DRM \_ \_**](drm-playlist-content-id.md)                            | Содержит сведения о содержимом, которое будет скопировано на компакт-диск в процессе записи списка воспроизведения.                                                                                 |
| [**\_VAL16 DRM**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | Сохраняет 128-разрядное значение, используемое в качестве идентификатора устройства.                                                                                                                       |
| [**\_ \_ Защита вывода видео \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | Содержит идентификатор технологии защиты видео и данные конфигурации, необходимые для этой технологии.                                                             |
| [**\_ \_ \_ идентификаторы защиты вывода видео DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | Содержит массив структур **\_ \_ \_ защиты вывода видео DRM** .                                                                                                          |
| [**вавеформатекс**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | Определяет формат данных звуковой волны.                                                                                                                                |
| [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | Определяет формат данных звуковой волны для форматов, имеющих более двух каналов.                                                                                      |
| [**WM \_ address \_ акцессентри**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | Указывает запись в списке доступа к IP-адресу.                                                                                                                          |
| [**\_Свойства клиента \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | Записывает сведения о клиенте.                                                                                                                                     |
| [**\_Свойства клиента WM, \_ \_ например**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | Записывает расширенные сведения о клиенте.                                                                                                                            |
| [**\_Получение \_ данных лицензии \_ WM**](wm-get-license-data.md)                                    | Содержит сведения о лицензии DRM.                                                                                                                                 |
| [**\_состояние ИНДИВИДУАЛИЗИРУЙТЕ \_ WM**](wm-individualize-status.md)                             | Записывает состояние процесса [*индивидуализации*](wmformat-glossary.md) .                                                                |
| [**\_пара сегментов с утечкой WM \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | Описывает требования к буферизации для файла переменной-битовой скорости (VBR).                                                                                                  |
| [**\_ \_ данные состояния лицензии \_ WM**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | Инкапсулирует структуру [**данных о \_ \_ состоянии лицензии \_ DRM**](drm-license-state-data.md) , которая описывает данные состояния лицензии DRM.                                              |
| [**\_тип мультимедиа \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | Описывает пример носителя.                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | Описывает поток видео MPEG-2.                                                                                                                                         |
| [**\_изображение WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | Содержит данные для атрибута "сложные метаданные" [**WM/Picture**](wmpicture.md) .                                                                                     |
| [**\_ \_ диапазон номеров портов \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | Описывает диапазон номеров портов, используемых интерфейсом **ивмреадернетворкконфиг** .                                                                                     |
| [**\_CLIENTINFO читатель \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | Описывает средство чтения клиента (проигрыватель), обращающееся к потоку мультимедиа.                                                                                                          |
| [**\_Статистика модуля чтения WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | Описывает производительность операции чтения.                                                                                                                         |
| [**вмскриптформат**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | Определяет формат потока скрипта.                                                                                                                                    |
| [**\_ \_ запись приоритета потока WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | Содержит номер потока и указывает, является ли доставка этого потока обязательной.                                                                                      |
| [**\_ \_ сведения о ТИПЕ потока WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | Содержит данные для атрибута сложных метаданных [**WM/стреамтипеинфо**](wm-streamtypeinfo.md) .                                                                      |
| [**\_синхронизированыные \_ слова WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | Содержит данные для атрибута [**\_ синхронизированы метаданных WM/песен**](wm-lyrics-synchronised.md) .                                                           |
| [**\_Пользовательский \_ текст WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | Содержит данные для атрибута "сложные метаданные" [**WM/Text**](wm-text.md) .                                                                                          |
| [**\_ \_ URL-адрес пользователя WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | Содержит данные для атрибута сложных метаданных [**WM/усервебурл**](wm-userweburl.md) .                                                                              |
| [**\_Статистика модуля записи WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | Описывает производительность операции записи.                                                                                                                         |
| [**\_Статистика модуля записи WM \_ \_ ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | Содержит статистику расширенной записи.                                                                                                                                      |
| [**\_ \_ ключ содержимого импорта \_ WMDRM**](wmdrm-import-content-key.md)                          | Содержит ключ содержимого, используемый при импорте защищенного содержимого.                                                                                                                |
| [**\_ \_ Структура инициализации импорта \_ WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | Содержит зашифрованный ключ сеанса и ключ содержимого, используемые при импорте защищенного содержимого.                                                                                      |
| [**\_ \_ ключ сеанса импорта \_ WMDRM**](wmdrm-import-session-key.md)                          | Содержит ключ сеанса для импорта защищенного содержимого.                                                                                                                    |
| [**\_сегмент буфера \_ ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | Содержит сведения, необходимые для указания сегмента в пакете.                                                                                                      |
| [**\_ \_ данные расширения ВМТ \_ колорспацеинфо**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | Содержит данные для \_ \_ расширения модуля обработки данных WM сампликстенсионгуид колорспацеинфо.                                                                                    |
| [**\_ \_ блок данных ВМТ \_ филесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | Содержит сведения о пакете.                                                                                                                                      |
| [**\_фрагмент полезных данных ВМТ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | Содержит сведения, необходимые для извлечения фрагмента полезных данных из пакета.                                                                                           |
| [**\_ \_ данные расширения времени ВМТ времени \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | Содержит один код времени SMPTE и связанную с ним информацию.                                                                                                                |
| [**\_Пример ВИДЕОИМАЖЕ \_ ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | Содержит сведения о примере видеоизображения.                                                                                                                          |
| [**\_запись водяного знака ВМТ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | Содержит сведения о системе водяных знаков.                                                                                                                         |
| [**ВМТный \_ \_ Формат потока**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | Содержит сведения о веб-потоке.                                                                                                                                  |
| [**\_заголовок ВМТ для \_ примера \_ потока**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | Содержит сведения о заголовке для примеров веб-потока.                                                                                                                       |
| [**вмвидеоинфохеадер**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | Описывает растровое изображение и сведения о цвете для изображения видео.                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | Описывает битовую карту и цвет изображения видео, включая [*чересстрочную развертку*](wmformat-glossary.md), защиту от копирования и пропорции.       |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Справочник по программированию**](programming-reference.md)
</dt> </dl>

 

 
