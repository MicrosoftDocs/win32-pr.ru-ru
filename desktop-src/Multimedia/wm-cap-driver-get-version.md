---
title: Сообщение WM_CAP_DRIVER_GET_VERSION (VFW. h)
description: '\_ \_ \_ Сообщение о получении версии драйвера WM Cap \_ возвращает сведения о версии драйвера записи, подключенного к окну записи. Это сообщение можно отправить явно или с помощью макроса Капдривержетверсион.'
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661967"
---
# <a name="wm_cap_driver_get_version-message"></a>\_Сообщение о \_ \_ получении \_ версии драйвера WM Cap

Сообщение **о \_ \_ \_ получении \_ версии драйвера WM Cap** возвращает сведения о версии драйвера записи, подключенного к окну записи. Это сообщение можно отправить явно или с помощью макроса [**капдривержетверсион**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) .


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*
</dt> <dd>

Размер (в байтах) определяемого приложением буфера, на который ссылается **сзвер**.

</dd> <dt>

<span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*сзвер*
</dt> <dd>

Указатель на определенный приложением буфер, используемый для возврата сведений о версии в виде строки, завершающейся нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.

## <a name="remarks"></a>Комментарии

Сведения о версии — это текстовая строка, полученная из области ресурсов драйвера. Для этой строки приложения должны выделить примерно 40 байт. Если сведения о версии недоступны, возвращается **пустая** строка.

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

 

 





