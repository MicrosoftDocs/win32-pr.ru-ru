---
title: Сообщение WM_CAP_DRIVER_CONNECT (VFW. h)
description: '\_ \_ Сообщение Connect с драйвером WM Cap \_ подключает окно записи к драйверу записи. Это сообщение можно отправить явно или с помощью макроса Капдриверконнект.'
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415345"
---
# <a name="wm_cap_driver_connect-message"></a>\_Сообщение о \_ подключении драйвера WM Cap \_

Сообщение **\_ \_ \_ Connect с драйвером WM Cap** подключает окно записи к драйверу записи. Это сообщение можно отправить явно или с помощью макроса [**капдриверконнект**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) .


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*ииндекс*
</dt> <dd>

Индекс драйвера записи. Индекс может находиться в диапазоне от 0 до 9.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** , если указанный драйвер записи не может быть подключен к окну Capture.

## <a name="remarks"></a>Комментарии

Подключение драйвера записи к окну записи автоматически отключает все ранее подключенные драйверы записи.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> <dt>

[Сообщения видеозаписи](video-capture-messages.md)
</dt> </dl>

 

 





