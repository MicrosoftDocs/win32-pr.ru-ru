---
description: Указывает уровень MPEG-2 или H. 264 в типе видеоматериала. Это псевдоним для \_ уровня MF MT \_ MPEG2 \_ .
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: Атрибут MF_MT_VIDEO_LEVEL (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40f1ebc6834373e00253f494e3fc76c20c343af17d754c7c4fe642b802d16ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012774"
---
# <a name="mf_mt_video_level-attribute"></a>\_ \_ Атрибут уровня видео MF MT \_

Указывает уровень MPEG-2 или H. 264 в типе видеоматериала. Это псевдоним для [ \_ \_ \_ уровня MF MT MPEG2](mf-mt-mpeg2-level-attribute.md).

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

**Кодировщики H. 264:**

Поддерживаемые уровни расширены для включения [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).

По умолчанию: Рекомендуемый вариант по умолчанию — выбор минимального уровня для соответствия конфигурации кодирования видео, включая разрешение, частоту кадров и т. д.

Рекомендуемое значение по умолчанию: выберите минимальный уровень для соответствия конфигурации кодирования видео, включая разрешение, частоту кадров и т. д.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




