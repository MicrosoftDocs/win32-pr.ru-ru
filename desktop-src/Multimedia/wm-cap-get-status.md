---
title: Сообщение WM_CAP_GET_STATUS (VFW. h)
description: '\_ \_ \_ Сообщение о состоянии крепления WM получает состояние окна сбора данных. Это сообщение можно отправить явно или с помощью макроса Капжетстатус.'
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- сообщение WM_CAP_GET_STATUS Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805befc3f83c79b157e040004dcf382dccaf07b240b3b846892b8fb035f826ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135160"
---
# <a name="wm_cap_get_status-message"></a>\_ \_ Получение \_ сообщения о состоянии крепления WM

Сообщение **\_ \_ \_ о состоянии крепления WM** получает состояние окна сбора данных. Это сообщение можно отправить явно или с помощью макроса [**капжетстатус**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) .


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*
</dt> <dd>

Размер (в байтах) структуры, на которую ссылается **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*#d0*
</dt> <dd>

Указатель на структуру [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.

## <a name="remarks"></a>Remarks

Структура [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus) содержит текущее состояние окна сбора данных. Поскольку это состояние является динамическим и изменяется в ответ на различные сообщения, приложение должно инициализировать эту структуру после отправки сообщения [**\_ видеоформат WM \_ DLG \_**](wm-cap-dlg-videoformat.md) (или с помощью макроса [**капдлгвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ) и всякий раз, когда необходимо включить пункты меню или определить фактическое состояние окна.

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

 

 





