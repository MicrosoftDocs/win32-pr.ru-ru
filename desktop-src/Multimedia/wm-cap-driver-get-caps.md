---
title: Сообщение WM_CAP_DRIVER_GET_CAPS (VFW. h)
description: '\_Сообщение о получении политики авторизации устройств WM Cap \_ \_ \_ возвращает аппаратные возможности драйвера записи, подключенного в настоящее время к окну записи. Это сообщение можно отправить явно или с помощью макроса Капдривержеткапс.'
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- сообщение WM_CAP_DRIVER_GET_CAPS Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aecc863234cddf64bece47896015fd01e97093d227951aef69363136e55cabe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687084"
---
# <a name="wm_cap_driver_get_caps-message"></a>\_Сообщение о \_ \_ получении \_ политик крепления WM

Сообщение **о \_ \_ \_ получении \_ политики авторизации устройств WM Cap** возвращает аппаратные возможности драйвера записи, подключенного в настоящее время к окну записи. Это сообщение можно отправить явно или с помощью макроса [**капдривержеткапс**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) .


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*
</dt> <dd>

Размер (в байтах) структуры, на которую ссылается **s**.

</dd> <dt>

<span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*пскапс*
</dt> <dd>

Указатель на структуру [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) , в которой должны содержаться аппаратные возможности.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.

## <a name="remarks"></a>Remarks

Возможности, возвращаемые в [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) , являются постоянными для данного драйвера записи. Приложения должны получить эту информацию один раз при первом подключении драйвера записи к окну записи.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> <dt>

[Сообщения видеозаписи](video-capture-messages.md)
</dt> </dl>

 

 





