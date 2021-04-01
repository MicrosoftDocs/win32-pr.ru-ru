---
description: Атрибуты дескриптора потока
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Атрибуты дескриптора потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811531"
---
# <a name="stream-descriptor-attributes"></a>Атрибуты дескриптора потока

## <a name="common-stream-descriptor-attributes"></a>Общие атрибуты дескриптора потока

К дескрипторам потоков применяются следующие атрибуты.



| attribute                                                   | Описание                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**\_язык MF SD \_**](mf-sd-language-attribute.md)        | Указывает язык для потока.                                                  |
| [MF \_ SD \_ взаимно \_ исключающее](mf-sd-mutually-exclusive.md) | Указывает, является ли поток взаимоисключающим с другими потоками того же типа. |
| [**MF \_ - \_ защищенный SD**](mf-sd-protected-attribute.md)      | Указывает, содержит ли поток защищенное содержимое.                                |
| [\_имя SD- \_ потока \_ MF](mf-sd-stream-name.md)               | Содержит имя потока.                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>ASF-Specific атрибуты дескриптора потока

Следующие атрибуты применяются к дескрипторам потоков для файлов ASF.



| attribute                                                                                                                | Описание                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ ASF \_ екстстрмпроп \_ AVG- \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | Указывает средний размер буфера, необходимый для потока в ASF-файле, в байтах.            |
| [**\_ \_ \_ \_ Средняя \_ \_ скорость данных (MF SD ASF екстстрмпроп)**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | Указывает среднюю скорость потока данных в файле ASF в битах в секунду.        |
| [**\_ \_ \_ индекс екстстрмпроп для \_ идентификатора языка \_ \_ MF SD ASF**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | Указывает язык, используемый потоком в ASF-файле.                                    |
| [**MF \_ SD \_ ASF \_ екстстрмпроп \_ Max \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | Указывает максимальный размер буфера, необходимый для потока в ASF-файле, в байтах.            |
| [**MF \_ SD \_ ASF \_ екстстрмпроп \_ Максимальная \_ скорость передачи данных \_**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | Указывает максимальную скорость передачи данных в потоке в ASF-файле, в битах в секунду         |
| [**\_ \_ \_ \_ \_ шаблон сосогласования устройства MF SD ASF \_**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | Указывает шаблон соответствия устройства для потока в ASF-файле в битах в секунду. |
| [**MF \_ SD \_ ASF \_ стреамбитратес \_ скорость**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | Указывает среднюю скорость потока в файле ASF в битах в секунду.             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>Пересаамский атрибуты дескриптора исходного потока носителя

Следующий атрибут применяется к дескриптору потока для источника на носителе SAMI.



| attribute                                                       | Описание                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**\_язык MF SD \_ Sami \_**](mf-sd-sami-language-attribute.md) | Содержит имя языка для синхронизированного доступного обмена мультимедиа (SAMI), определенное для потока. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



