---
title: Сообщение ICM_GETINFO (VFW. h)
description: Сообщение ICM \_ info запрашивает драйвер сжатия видео, чтобы получить описание самого себя в структуре иЦинфо.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- сообщение ICM_GETINFO Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173f510642b807a0e4c4a8c5c84d6d4de2aa7ce55cc0707eccabf5421cf98a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690814"
---
# <a name="icm_getinfo-message"></a>Информационное \_ сообщение ICM

Сообщение **ICM \_ info** запрашивает драйвер сжатия видео, чтобы получить описание самого себя в структуре [**иЦинфо**](/windows/desktop/api/Vfw/ns-vfw-icinfo) .


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpicinfo"></span><span id="LPICINFO"></span>*лпиЦинфо*
</dt> <dd>

Указатель на структуру **иЦинфо** для хранения информации.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Размер **иЦинфо** в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает размер (в байтах) [**иЦинфо**](/windows/desktop/api/Vfw/ns-vfw-icinfo) или нуль в случае возникновения ошибки.

## <a name="remarks"></a>Remarks

Как правило, приложения отправляют это сообщение, чтобы отобразить список установленных компрессоров.

Драйвер должен заполнить все элементы структуры [**иЦинфо**](/windows/desktop/api/Vfw/ns-vfw-icinfo) , за исключением **сздривер**.

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

 

 





