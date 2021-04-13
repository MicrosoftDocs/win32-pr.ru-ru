---
title: Сообщение WM_CAP_DRIVER_GET_NAME (VFW. h)
description: '\_ \_ \_ Сообщение Get Name драйвера WM Cap \_ возвращает имя драйвера записи, подключенного к окну Capture (захват). Это сообщение можно отправить явно или с помощью макроса Капдривержетнаме.'
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489750"
---
# <a name="wm_cap_driver_get_name-message"></a>\_Сообщение о \_ \_ получении \_ имени драйвера WM Cap

Сообщение **\_ \_ \_ Get \_ Name драйвера WM Cap** возвращает имя драйвера записи, подключенного к окну Capture (захват). Это сообщение можно отправить явно или с помощью макроса [**капдривержетнаме**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) .


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*
</dt> <dd>

Размер (в байтах) буфера, на который ссылается параметр **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Указатель на определенный приложением буфер, используемый для возврата имени устройства в виде строки, завершающейся нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.

## <a name="remarks"></a>Комментарии

Имя — это текстовая строка, полученная из области ресурсов драйвера. Для этой строки приложения должны выделить примерно 80 байт. Если драйвер не содержит ресурс имени, возвращается полный путь к драйверу, указанному в реестре или в файле SYSTEM.INI.

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

 

 





