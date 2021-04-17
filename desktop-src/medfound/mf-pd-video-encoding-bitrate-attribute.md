---
description: Указывает скорость кодирования видео для презентации в битах в секунду. Этот атрибут применяется к дескрипторам представления.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: Атрибут MF_PD_VIDEO_ENCODING_BITRATE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477d0954b4db8fa11c1540153c096e42f6d255b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703143"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a>\_Атрибут скорости \_ кодирования для записи MF PD \_ \_

Указывает скорость кодирования видео для презентации в битах в секунду. Этот атрибут применяется к дескрипторам представления.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут является необязательным. Некоторые форматы имеют более сложные схемы кодирования, которые не могут быть обобщены с помощью этого атрибута. Для файлов формата ASF следующие атрибуты вместе описывают скорость кодирования:

-   [**MF \_ PD \_ ASF \_ филепропертиес \_ Максимальная \_ скорость**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**\_ \_ \_ \_ Средняя \_ \_ скорость данных (MF SD ASF екстстрмпроп)**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ екстстрмпроп \_ Максимальная \_ скорость передачи данных \_**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ стреамбитратес \_ скорость**](mf-sd-asf-streambitrates-bitrate-attribute.md)

Сторонние форматы могут использовать другие настраиваемые атрибуты.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




