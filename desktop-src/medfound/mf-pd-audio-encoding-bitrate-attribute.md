---
description: Указывает скорость кодирования звука для презентации в битах в секунду. Этот атрибут применяется к дескрипторам представления.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: Атрибут MF_PD_AUDIO_ENCODING_BITRATE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041e92eb71621d1f42d2b800557d204215bbca40f346a2afa4627863fc1a2206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102881"
---
# <a name="mf_pd_audio_encoding_bitrate-attribute"></a>\_Атрибут скорости \_ звуковой \_ кодировки MF PD \_

Указывает скорость кодирования звука для презентации в битах в секунду. Этот атрибут применяется к дескрипторам представления.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Атрибут является необязательным. Некоторые форматы имеют более сложные схемы кодирования, которые не могут быть обобщены с помощью этого атрибута. Для файлов формата ASF следующие атрибуты вместе описывают скорость кодирования:

-   [**MF \_ PD \_ ASF \_ филепропертиес \_ Максимальная \_ скорость**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**\_ \_ \_ \_ Средняя \_ \_ скорость данных (MF SD ASF екстстрмпроп)**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ екстстрмпроп \_ Максимальная \_ скорость передачи данных \_**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ стреамбитратес \_ скорость**](mf-sd-asf-streambitrates-bitrate-attribute.md)

Сторонние форматы могут использовать другие настраиваемые атрибуты.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
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

 

 




