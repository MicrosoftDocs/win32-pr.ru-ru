---
description: Целевой средний уровень громкости звукового файла Windows Media.
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: Атрибут MF_MT_AUDIO_WMADRC_AVGTARGET (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41956e2e9e6f14e969cade3628f1e88bce98796d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349132"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a>\_Атрибут MF \_ Audio \_ вмадрк \_ авгтаржет

Целевой средний уровень громкости звукового файла Windows Media.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к типам звуковых носителей для аудиокодеков Windows Media. Указывает целевой средний уровень громкости содержимого. Декодер может использовать это значение для выполнения динамического управления диапазоном.

Метод [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) добавляет этот атрибут к типу мультимедиа, если заголовок ASF содержит атрибут [**WM/вмадркаверажетаржет**](../wmformat/wm-wmadrcaveragetarget.md) . Этот атрибут описан в документации пакета SDK Windows Media Format.

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

 

 
