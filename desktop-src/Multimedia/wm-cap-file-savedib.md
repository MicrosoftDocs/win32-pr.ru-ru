---
title: Сообщение WM_CAP_FILE_SAVEDIB (VFW. h)
description: '\_Сообщение саведиб с закреплением WM \_ \_ копирует текущий кадр в DIB-файл. Это сообщение можно отправить явно или с помощью макроса Капфилесаведиб.'
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492951"
---
# <a name="wm_cap_file_savedib-message"></a>\_ \_ \_ Сообщение саведиба WM Cap File

Сообщение **\_ \_ \_ саведиб с закреплением WM** копирует текущий кадр в DIB-файл. Это сообщение можно отправить явно или с помощью макроса [**капфилесаведиб**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) .


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая содержит имя конечного файла DIB.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.

## <a name="remarks"></a>Комментарии

Если драйвер записи передает кадры в сжатом формате, этот вызов пытается распаковать кадр перед записью файла.

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

 

 





