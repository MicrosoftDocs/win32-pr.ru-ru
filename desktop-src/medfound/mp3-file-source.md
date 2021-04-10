---
description: Источник файлов в формате MP3 анализирует MP3-файлы.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Источник MP3-файла
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155343"
---
# <a name="mp3-file-source"></a>Источник MP3-файла

Источник файлов в формате MP3 анализирует MP3-файлы.

Источник файлов в формате MP3 выводит буферы, содержащие звуковые кадры MPEG-1. Он не расшифровывает звук.

## <a name="file-extensions-and-mime-types"></a>Расширения файлов и типы MIME

Источник файлов в формате MP3 — это источник мультимедиа по умолчанию для следующего расширения имени файла:

-   .mp3

Он также является источником мультимедиа по умолчанию для следующих типов MIME.

-   аудио/MPEG
-   аудио/x-MP3
-   аудио/x-MPEG

## <a name="media-types"></a>Типы носителей

Тип носителя, предлагаемый источником файлов в формате MP3, содержит следующие атрибуты.



| attribute                                                                                    | Описание                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md)                                    | Равно **мфмедиатипе \_ Audio**.                                                                                                                   |
| [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)                                           | Равно **мфаудиоформат \_ MP3** или **мфаудиоформат \_ MPEG**.                                                                                        |
| [**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Среднее число байтов в секунду.                                                                                                                |
| [**\_ \_ Выравнивание звукового \_ блока MF MT \_**](mf-mt-audio-block-alignment-attribute.md)             | Равно 1.                                                                                                                                        |
| [**\_ \_ каналы аудиосигнала MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                   | Число аудиоканалов.                                                                                                                          |
| [**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**](mf-mt-audio-samples-per-second-attribute.md)      | Количество звуковых выборок в секунду.                                                                                                                |
| [**\_ \_ данные пользователя MF \_ MT**](mf-mt-user-data-attribute.md)                                      | Содержит часть структуры [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) , которая отображается после элемента **вфкс** структуры. |



 

## <a name="interfaces"></a>Интерфейсы

Источник файлов в формате MP3 предоставляет следующие интерфейсы через [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):

-   [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

Кроме того, он предоставляет доступ к следующим интерфейсам через [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Service GUID</th>
<th>Интерфейс</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MF_METADATA_PROVIDER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>имфметадатапровидер</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_PROPERTY_HANDLER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>ипропертисторе</strong></a>
<blockquote>
[!Note]<br />
См. раздел <a href="shell-metadata-providers.md">поставщики метаданных оболочки</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>имфратеконтрол</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>имфратесуппорт</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                        |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                           |
| DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Источники и приемники мультимедиа](media-sources-and-sinks.md)
</dt> <dt>

[Источники мультимедиа](media-sources.md)
</dt> <dt>

[Сопоставитель источников](source-resolver.md)
</dt> <dt>

[Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
