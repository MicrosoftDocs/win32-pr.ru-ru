---
title: Сообщение ICM_DECOMPRESS_END (VFW. h)
description: '\_ \_ Сообщение об ОКОНЧАНИи распаковки ICM уведомляет драйвер распаковки о завершении распаковки и освобождения ресурсов, выделенных для распаковки. Это сообщение можно отправить явно или с помощью макроса Икдекомпрессенд.'
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- сообщение ICM_DECOMPRESS_END Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c877afac3db0e4cf4d7c476ca3806d2acd15bdf72764549b2958490574a4f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691164"
---
# <a name="icm_decompress_end-message"></a>\_Завершающее сообщение РАЗуплотнения ICM \_

Сообщение **об \_ \_ окончании распаковки ICM** уведомляет драйвер распаковки о завершении распаковки и освобождения ресурсов, выделенных для распаковки. Это сообщение можно отправить явно или с помощью макроса [**икдекомпрессенд**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Драйвер должен освободить все ресурсы, выделенные для [**сообщения \_ \_ Begin reуплотнения ICM**](icm-decompress-begin.md) .

[**ICM \_ Конец СЖАТИЯ \_ Begin**](icm-decompress-begin.md) и **ICM \_ unуплотнение \_** не вложены. Если драйвер Получает подсистему **\_ распаковки ICM \_ Begin** до остановки распаковки **с \_ \_ окончанием распаковки ICM**, необходимо перезапустить распаковку с новыми параметрами.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер сжатия видео](video-compression-manager.md)
</dt> <dt>

[Сообщения о сжатии видео](video-compression-messages.md)
</dt> </dl>

 

 





