---
title: Сообщение WM_CAP_DRIVER_CONNECT (VFW. h)
description: '\_ \_ Сообщение Connect с драйвером WM Cap \_ подключает окно записи к драйверу записи. Это сообщение можно отправить явно или с помощью макроса Капдриверконнект.'
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- сообщение WM_CAP_DRIVER_CONNECT Windows мультимедиа
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
ms.openlocfilehash: c8b0e54d496302488db653505321778bcd22546bd2ed9b2180aa0e15cb6969f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622633"
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

## <a name="remarks"></a>Remarks

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

 

 





