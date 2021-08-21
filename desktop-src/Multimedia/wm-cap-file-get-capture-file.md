---
title: Сообщение WM_CAP_FILE_GET_CAPTURE_FILE (VFW. h)
description: '\_ \_ \_ Сообщение о получении файла записи с закреплением WM \_ \_ возвращает имя текущего файла записи. Это сообщение можно отправить явно или с помощью макроса Капфилежеткаптурефиле.'
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- сообщение WM_CAP_FILE_GET_CAPTURE_FILE Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462f919458078129f6756782c2fde5322b3cd814c3108cb0ba8ee24e2f54c022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135322"
---
# <a name="wm_cap_file_get_capture_file-message"></a>\_Сообщение о \_ \_ получении \_ файла записи \_ закрепления WM

Сообщение **о \_ \_ \_ получении \_ \_ файла записи с закреплением WM** возвращает имя текущего файла записи. Это сообщение можно отправить явно или с помощью макроса [**капфилежеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) .


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*
</dt> <dd>

Размер (в байтах) определяемого приложением буфера, на который ссылается параметр **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Указатель на определенный приложением буфер, используемый для возврата имени файла записи в виде строки, завершающейся нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Remarks

Имя файла для отслеживания по умолчанию — C: \\CAPTURE.AVI.

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

 

 





