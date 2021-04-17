---
title: Сообщение ICM_GETDEFAULTKEYFRAMERATE (VFW. h)
description: Сообщение ICM \_ жетдефаулткэйфрамерате запрашивает драйвер сжатия видео о его стандартном (или предпочтительном) интервале между кадрами. Это сообщение можно отправить явно или с помощью макроса Икжетдефаултэйфрамерате.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415645"
---
# <a name="icm_getdefaultkeyframerate-message"></a>\_Сообщение ICM жетдефаулткэйфрамерате

Сообщение **ICM \_ жетдефаулткэйфрамерате** запрашивает драйвер сжатия видео о его стандартном (или предпочтительном) интервале между кадрами. Это сообщение можно отправить явно или с помощью макроса [**икжетдефаултэйфрамерате**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) .


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*двиквалуе*
</dt> <dd>

Адрес, который будет содержать предпочтительные интервалы между кадрами.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает это сообщение или ИЦЕРР \_ не поддерживается в противном случае.

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

 

 





