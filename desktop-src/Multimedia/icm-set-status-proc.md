---
title: Сообщение ICM_SET_STATUS_PROC (VFW. h)
description: Сообщение о \_ состоянии установки ICM \_ \_ предоставляет функцию обратного вызова состояния с состоянием длительной операции.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- сообщение ICM_SET_STATUS_PROC Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02019bb6375aa18fd37ba34d2603839b37291d58822858b0b9cabc01e47d7b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678344"
---
# <a name="icm_set_status_proc-message"></a>\_ \_ Сообщение о состоянии установки ICM \_

Сообщение **о \_ \_ состоянии установки \_ ICM** предоставляет функцию обратного вызова состояния с состоянием длительной операции.


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*иксетстатуспрок*
</dt> <dd>

Указатель на структуру [**иксетстатуспрок**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Размер **иксетстатуспрок** в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Поддержка этого сообщения является необязательной, но настоятельно рекомендуется, если сжатие или распаковка занимает больше времени, чем приблизительно в одну десятую секунды.

Приложение может периодически отправить это сообщение в функцию обратного вызова состояния во время длительных операций.

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

 

 





