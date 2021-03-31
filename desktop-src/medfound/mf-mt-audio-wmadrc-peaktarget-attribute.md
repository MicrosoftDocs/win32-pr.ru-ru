---
description: Целевой пиковый уровень громкости звукового файла Windows Media.
ms.assetid: 73f4e763-dcb7-48cd-ab80-37635d973da0
title: Атрибут MF_MT_AUDIO_WMADRC_PEAKTARGET (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48391adfaa19dcc00ea4d7a30b909b4573f67222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999173"
---
# <a name="mf_mt_audio_wmadrc_peaktarget-attribute"></a>\_Атрибут MF \_ Audio \_ вмадрк \_ пеактаржет

Целевой пиковый уровень громкости звукового файла Windows Media.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к типам звуковых носителей для аудиокодеков Windows Media. Он указывает целевой пиковый уровень содержимого. Декодер может использовать это значение для выполнения динамического управления диапазоном.

Метод [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) добавляет этот атрибут к типу мультимедиа, если заголовок ASF содержит атрибут [**WM/вмадркпеактаржет**](../wmformat/wm-wmadrcpeaktarget.md) . Этот атрибут описан в документации пакета SDK Windows Media Format.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 
