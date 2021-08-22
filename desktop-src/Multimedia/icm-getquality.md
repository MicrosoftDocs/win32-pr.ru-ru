---
title: Сообщение ICM_GETQUALITY (VFW. h)
description: Сообщение ICM \_ Quality запрашивает драйвер сжатия видео, чтобы вернуть текущий параметр качества.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- сообщение ICM_GETQUALITY Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cef214fe36c713e63659fcbd4dde2021c8d410b36ea9f5525ed54c76c5c4b6a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495864"
---
# <a name="icm_getquality-message"></a>Сообщение ICM с \_ качеством

Сообщение **ICM \_ Quality** запрашивает драйвер сжатия видео, чтобы вернуть текущий параметр качества.


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*двиквалуе*
</dt> <dd>

Адрес, который будет содержать текущее значение качества. Значения качества находятся в диапазоне от 0 до 10 000.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает это сообщение или ИЦЕРР \_ не поддерживается в противном случае.

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

 

 





