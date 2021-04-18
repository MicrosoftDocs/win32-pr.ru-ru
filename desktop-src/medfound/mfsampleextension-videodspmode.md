---
description: Указывает, применено ли видео стабилизации к видеокадру.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: Атрибут MFSampleExtension_VideoDSPMode (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719466"
---
# <a name="mfsampleextension_videodspmode-attribute"></a>Мфсампликстенсион \_ видеодспмоде, атрибут

Указывает, применено ли видео стабилизации к видеокадру.

## <a name="data-type"></a>Тип данных

**Мфвидеодспмоде** хранится как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Комментарии

[**Стабилизация видео MFT**](video-stabilization-mft.md) задает этот атрибут в выходных образцах, которые он создает. Значение атрибута является значением перечисления [**мфвидеодспмоде**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) . Если значение равно **мфвидеодспмоде \_ стабилизации**, это означает, что MFT применил Image стабилизации к кадру.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> <dt>

[**Стабилизация видео MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




