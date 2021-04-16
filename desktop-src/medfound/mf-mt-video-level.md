---
description: Указывает уровень MPEG-2 или H. 264 в типе видеоматериала. Это псевдоним для \_ уровня MF MT \_ MPEG2 \_ .
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: Атрибут MF_MT_VIDEO_LEVEL (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2c5eb00390df1b5c18cab7e04a5f7449f84fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712913"
---
# <a name="mf_mt_video_level-attribute"></a>\_ \_ Атрибут уровня видео MF MT \_

Указывает уровень MPEG-2 или H. 264 в типе видеоматериала. Это псевдоним для [ \_ \_ \_ уровня MF MT MPEG2](mf-mt-mpeg2-level-attribute.md).

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

**Кодировщики H. 264:**

Поддерживаемые уровни расширены для включения [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).

По умолчанию: Рекомендуемый вариант по умолчанию — выбор минимального уровня для соответствия конфигурации кодирования видео, включая разрешение, частоту кадров и т. д.

Рекомендуемое значение по умолчанию: выберите минимальный уровень для соответствия конфигурации кодирования видео, включая разрешение, частоту кадров и т. д.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                       |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




