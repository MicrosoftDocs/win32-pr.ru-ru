---
title: Сообщение WM_CAP_SET_MCI_DEVICE (VFW. h)
description: В \_ \_ сообщении об установке устройства mci с закреплениями WM \_ \_ указывается имя видеоустройства MCI, которое будет использоваться для записи данных. Это сообщение можно отправить явно или с помощью макроса КапсетмЦидевиценаме.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801192"
---
# <a name="wm_cap_set_mci_device-message"></a>\_ \_ \_ \_ Сообщение об установке устройства mci с закреплениями WM

В сообщении об **\_ \_ установке \_ \_ Устройства MCI с закреплениями WM** указывается имя видеоустройства MCI, которое будет использоваться для записи данных. Это сообщение можно отправить явно или с помощью макроса [**капсетмЦидевиценаме**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) .


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Указатель на строку с завершающим нулем, содержащую имя устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Это сообщение сохраняет имя устройства MCI во внутренней структуре. Он не открывает устройство и не обращается к нему. Имя устройства по умолчанию — **null**.

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

 

 





