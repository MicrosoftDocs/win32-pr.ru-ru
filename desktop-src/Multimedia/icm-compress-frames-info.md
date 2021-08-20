---
title: Сообщение ICM_COMPRESS_FRAMES_INFO (VFW. h)
description: '\_ \_ \_ Информационное сообщение ICM сжимать кадры уведомляет драйвер сжатия, чтобы задать параметры для ожидающего сжатия.'
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- сообщение ICM_COMPRESS_FRAMES_INFO Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2382a930b0ce12e212adf78ddaf3c7e1b3300e47597b4671d0eae223cb536f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140915"
---
# <a name="icm_compress_frames_info-message"></a>\_ \_ Сообщение о сжатии кадров ICM \_

**\_ \_ \_ Информационное сообщение ICM сжимать кадры** уведомляет драйвер сжатия, чтобы задать параметры для ожидающего сжатия.


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="icf"></span><span id="ICF"></span>*к*
</dt> <dd>

Указатель на структуру [**иккомпрессфрамес**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) . Элементы **GetData** и **путдата** этой структуры не используются с этим сообщением.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Размер [**иккомпрессфрамес**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes)в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Программа сжатия может использовать это сообщение для определения объема пространства, выделяемого для каждого кадра при сжатии.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Диспетчер сжатия видео](video-compression-manager.md)
</dt> <dt>

[Сообщения о сжатии видео](video-compression-messages.md)
</dt> </dl>

 

 





