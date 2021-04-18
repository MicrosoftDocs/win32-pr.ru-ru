---
description: Выравнивание блокировки (в байтах) для типа звукового носителя. Выравнивание блока — это минимальная атомарная единица данных для звукового формата.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: Атрибут MF_MT_AUDIO_BLOCK_ALIGNMENT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702495"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a>\_ \_ \_ Атрибут выравнивания звукового блока MF MT \_

Выравнивание блокировки (в байтах) для типа звукового носителя. Выравнивание блока — это минимальная атомарная единица данных для звукового формата.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Для звуковых форматов PCM выравнивание блока равно числу звуковых каналов, умноженному на число байтов на каждый образец звука.

Этот атрибут соответствует элементу **нблоккалигн** структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .

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

 

 
