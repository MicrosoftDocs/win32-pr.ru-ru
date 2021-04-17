---
title: Сообщение WM_CAP_GET_MCI_DEVICE (VFW. h)
description: В сообщении о получении крепления WM получается \_ \_ \_ \_ имя устройства MCI, установленное ранее с помощью \_ \_ \_ сообщения устройства mci Set с закреплениями WM \_ . Это сообщение можно отправить явно или с помощью макроса КапжетмЦидевиценаме.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488964"
---
# <a name="wm_cap_get_mci_device-message"></a>\_Закрепление \_ WM \_ Получение \_ сообщения устройства mci

В сообщении о **\_ \_ получении \_ крепления \_ WM** получается имя устройства MCI, установленное ранее с помощью сообщения [**\_ \_ \_ \_ Устройства MCI Set с закреплениями WM**](wm-cap-set-mci-device.md) . Это сообщение можно отправить явно или с помощью макроса [**капжетмЦидевиценаме**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) .


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*
</dt> <dd>

Длина в байтах буфера, на который ссылается параметр **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая содержит имя устройства MCI.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

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

 

 





