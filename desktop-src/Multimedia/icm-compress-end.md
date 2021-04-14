---
title: Сообщение ICM_COMPRESS_END (VFW. h)
description: '\_ \_ Сообщение о завершении сжатия ICM уведомляет драйвер сжатия видео о завершении сжатия и свободных ресурсах, выделенных для сжатия. Это сообщение можно отправить явно или с помощью макроса Иккомпрессенд.'
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489900"
---
# <a name="icm_compress_end-message"></a>\_ \_ Завершающее сообщение сжатия ICM

Сообщение **о \_ \_ завершении сжатия ICM** уведомляет драйвер сжатия видео о завершении сжатия и свободных ресурсах, выделенных для сжатия. Это сообщение можно отправить явно или с помощью макроса [**иккомпрессенд**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

ВКМ сохраняет параметры последнего сообщения о [**\_ \_ начале сжатия ICM**](icm-compress-begin.md) . **ICM \_ \_Begin** и сжатие ICM не вложены в **\_ \_ конец** . Если драйвер получает коэффициент **\_ сжатия ICM \_** , прежде чем сжатие будет остановлено с **\_ \_ окончанием сжатия ICM**, необходимо перезапустить сжатие с новыми параметрами.

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

 

 





