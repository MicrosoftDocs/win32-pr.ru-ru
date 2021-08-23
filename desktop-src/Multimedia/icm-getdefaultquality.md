---
title: Сообщение ICM_GETDEFAULTQUALITY (VFW. h)
description: Сообщение ICM \_ жетдефаулткуалити запрашивает драйвер сжатия видео, чтобы предоставить параметр качества по умолчанию. Это сообщение можно отправить явно или с помощью макроса Икжетдефаулткуалити.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- сообщение ICM_GETDEFAULTQUALITY Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9c27527cea53c4b4eca6cf75babef3a41f80732d8ecf7a18528c07d6d9311b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525914"
---
# <a name="icm_getdefaultquality-message"></a>\_Сообщение ICM жетдефаулткуалити

Сообщение **ICM \_ жетдефаулткуалити** запрашивает драйвер сжатия видео, чтобы предоставить параметр качества по умолчанию. Это сообщение можно отправить явно или с помощью макроса [**икжетдефаулткуалити**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*двиквалуе*
</dt> <dd>

Адрес, который будет содержать значение качества по умолчанию. Значения качества находятся в диапазоне от 0 до 10 000.

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

 

 





