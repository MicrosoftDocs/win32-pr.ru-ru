---
title: Сообщение ICM_GETBUFFERSWANTED (VFW. h)
description: В \_ сообщении ICM жетбуфферсвантед запрашивается драйвер для количества выделяемых буферов. Это сообщение можно отправить явно или с помощью макроса Икжетбуфферсвантед.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- сообщение ICM_GETBUFFERSWANTED Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bd5fae6e9f008649366cf922ef117f5b6f7560a7764c4f8d81552a255de48a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495874"
---
# <a name="icm_getbufferswanted-message"></a>\_Сообщение ICM жетбуфферсвантед

В сообщении **ICM \_ жетбуфферсвантед** запрашивается драйвер для количества выделяемых буферов. Это сообщение можно отправить явно или с помощью макроса [**икжетбуфферсвантед**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) .


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*лпдвбуфферс*
</dt> <dd>

Адрес, который будет содержать число выборок, необходимых драйверу для эффективной визуализации данных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК, если \_ в противном случае успешно или ИЦЕРР не поддерживается.

## <a name="remarks"></a>Remarks

Это сообщение используется драйверами, которые используют оборудование для визуализации данных и хотят обеспечить минимальную задержку, вызванную ожиданием прибытия буферов. Например, если драйвер управляет платой распаковки видео, которая может содержать 10 кадров видео, это сообщение может вернуть 10. Это означает, что приложения попытаются остаться в 10 кадрах до конца фрейма, который им необходим.

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

 

 





