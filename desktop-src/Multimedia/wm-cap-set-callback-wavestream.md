---
title: Сообщение WM_CAP_SET_CALLBACK_WAVESTREAM (VFW. h)
description: '\_ \_ \_ Сообщение вавестреам для обратного вызова Set крепления WM \_ устанавливает функцию обратного вызова в приложении.'
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- сообщение WM_CAP_SET_CALLBACK_WAVESTREAM Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e4a8ef585a3ceb35aa07fe4e31c5819ce3e56d20b0bfd2d6c5f588fc25c335b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622523"
---
# <a name="wm_cap_set_callback_wavestream-message"></a>\_Сообщение о \_ \_ вавестреам обратного вызова Set крепления WM \_

Сообщение **\_ вавестреам для \_ \_ обратного \_ вызова Set крепления WM** устанавливает функцию обратного вызова в приложении. Авикап вызывает эту процедуру при захвате потоковой передачи, когда новый звуковой буфер станет доступным. Это сообщение можно отправить явно или с помощью макроса [**капсеткаллбакконвавестреам**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*фппрок*
</dt> <dd>

Указатель на функцию обратного вызова потока Wave типа [**капвавестреамкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback). Укажите **значение NULL** для этого параметра, чтобы отключить ранее установленную функцию обратного вызова потока Wave.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** , если выполняется захват потоковой передачи или однокадровый сеанс записи.

## <a name="remarks"></a>Remarks

Окно записи вызывает процедуру перед записью звукового буфера на диск. Это позволяет приложениям изменять аудио буфер при необходимости.

Если используется функция обратного вызова волнового потока, ее необходимо установить перед запуском сеанса записи, и она должна оставаться включенной в течение сеанса. Его можно отключить после завершения потоковой записи.

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

 

 





