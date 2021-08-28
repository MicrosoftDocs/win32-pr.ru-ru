---
title: Сообщение WM_CAP_FILE_SET_CAPTURE_FILE (VFW. h)
description: '\_ \_ \_ Сообщение файла записи набора закрепления WM задает \_ \_ имя файла, используемого для записи видео. Это сообщение можно отправить явно или с помощью макроса Капфилесеткаптурефиле.'
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- сообщение WM_CAP_FILE_SET_CAPTURE_FILE Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9435a7f0790c8ffe88f6b7ea6228bb2f442b23f5dcb15e2722e59b75c671588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687024"
---
# <a name="wm_cap_file_set_capture_file-message"></a>\_Сообщение о \_ \_ наборе файлов \_ фиксации \_ WM Cap

Сообщение **\_ \_ \_ \_ \_ файла записи набора закрепления WM задает** имя файла, используемого для записи видео. Это сообщение можно отправить явно или с помощью макроса [**капфилесеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) .


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая содержит имя файла записи для использования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** , если имя файла является недопустимым, или если выполняется потоковая передача или захват одного кадра.

## <a name="remarks"></a>Remarks

Это сообщение сохраняет имя файла во внутренней структуре. Он не создает, не выделяет или не открывает указанный файл. Имя файла для отслеживания по умолчанию — C: \\CAPTURE.AVI.

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

 

 





