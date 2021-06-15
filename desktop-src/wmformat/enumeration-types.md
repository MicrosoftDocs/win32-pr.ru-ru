---
title: Типы перечисления пакета SDK Windows Media Format
description: Сведения о типах перечислений, реализуемых пакетом SDK для формата Windows Media, например DRM_HTTP_STATUS и DRM_LICENSE_STATE_CATEGORY.
ms.assetid: cd28f608-25ba-44a7-868b-b1cd4dfcfa45
keywords:
- Windows Media Format SDK, типы перечислений
- Расширенный системный формат (ASF), типы перечислений
- ASF (Расширенный системный формат), типы перечислений
- типы перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a6fcb6d433079cce9d570a7eb6e28f31691985
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068000"
---
# <a name="windows-media-format-sdk-enumeration-types"></a>Типы перечисления пакета SDK Windows Media Format

Пакет SDK для формата Windows Media реализует следующие типы перечислений.



| Тип перечисления                                                               | Описание                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_состояние HTTP \_ DRM**](drm-http-status.md)                                   | Определяет диапазон состояний для запроса DRM.                                                                                     |
| [**\_ \_ Категория состояния лицензии \_ DRM**](drm-license-state-category.md)            | Определяет категории для строк лицензии DRM.                                                                                  |
| [**\_состояние ИНДИВИДУАЛИЗАЦИИ DRM \_**](drm-individualization-status.md)         | Определяет допустимые состояния для индивидуальной защиты DRM.                                                                              |
| [**\_Параметры УРЛКРЕДПОЛИЦИ \_ нетсаурце**](/previous-versions/windows/desktop/api/wmsinternaladminnetsource/ne-wmsinternaladminnetsource-netsource_urlcredpolicy_settings) | Определяет возможные параметры политики безопасности, которые могут существовать на клиентском компьютере.                                                   |
| [**WM \_ аетипе**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wm_aetype)                                                | Указывает разрешения для записи в списке доступа к IP-адресу.                                                             |
| [**\_ \_ тип данных ВМТ attr**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype)                               | Определяет диапазон базовых типов данных. Эти значения используются для обнаружения типа данных, возвращаемых различными методами в этом пакете SDK. |
| [**ВМТ \_ attr \_ IMAGETYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_imagetype)                             | Определяет диапазон типов изображений, которые могут храниться в заголовке ASF-файла.                                                         |
| [**\_ \_ тип сведений о КОДЕка ВМТ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_codec_info_type)                          | Определяет диапазон размеров данных, используемых кодеком.                                                                                   |
| [**\_Флаги учетных данных ВМТ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_credential_flags)                         | Определяет флаги, которые могут использоваться при получении учетных данных.                                                                   |
| [**ВМТ \_ дрмла \_ Trust**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust)                                   | Определяет состояние доверия для URL-адреса приобретения лицензии DRM.                                                                        |
| [**\_режим ФИЛЕСИНК \_ ВМТ**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_filesink_mode)                               | Определяет типы входных данных, принимаемые приемником файла.                                                                            |
| [**\_тип изображения \_ ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_image_type)                                     | Определяет возможные типы изображений, используемые для баннерных объявлений.                                                                            |
| [**\_Тип индекса \_ ВМТ**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_index_type)                                     | Определяет объект, с которым может быть связан индекс, основанный на времени.                                                              |
| [**\_тип индексатора \_ ВМТ**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_indexer_type)                                 | Определяет типы индексирования, поддерживаемые индексатором.                                                                          |
| [**\_протокол ВМТ NET \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_net_protocol)                                 | Определяет типы протоколов, которые поддерживаются приемником сети.                                                                   |
| [**\_ \_ режим класса ВМТ \_ мусикспич**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_musicspeech_class_mode)            | Определяет режимы сжатия, доступные для голосового кодека Windows Media Audio 9.                                                |
| [**\_Формат смещения \_ ВМТ**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_offset_format)                               | Определяет типы смещений, используемых в этом пакете SDK.                                                                                   |
| [**\_режим воспроизведения \_ ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_play_mode)                                       | Определяет параметры воспроизведения модуля чтения.                                                                                      |
| [**\_Параметры прокси-сервера ВМТ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_proxy_settings)                             | Определяет параметры прокси-сервера сети для использования с объектом Reader.                                                                 |
| [**\_права ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights)                                              | Определяет права, которые могут быть указаны в лицензии DRM.                                                                       |
| [**\_состояние ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)                                              | Определяет диапазон флагов состояния.                                                                                                 |
| [**\_Формат хранения \_ ВМТ**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format)                             | Определяет типы файлов, которыми можно управлять с помощью этого пакета SDK.                                                                    |
| [**\_Выбор потока \_ ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection)                         | Определяет состояние потока.                                                                                                  |
| [**\_тип транспорта \_ ВМТ**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_transport_type)                             | Определяет типы транспорта, поддерживаемые этим пакетом SDK.                                                                               |
| [**\_версия ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version)                                            | Определяет номера версий пакета SDK Windows Media Format.                                                                     |
| [**\_тип записи водяного знака ВМТ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_watermark_entry_type)                | Определяет типы поддерживаемых водяных знаков.                                                                                       |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Справочник по программированию**](programming-reference.md)
</dt> </dl>

 

 




