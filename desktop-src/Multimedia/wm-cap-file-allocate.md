---
title: Сообщение WM_CAP_FILE_ALLOCATE (VFW. h)
description: '\_ \_ \_ Сообщение о выделении файла закрепления WM создает (предварительно выделяет) файл записи указанного размера. Это сообщение можно отправить явно или с помощью макроса Капфилеаллок.'
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- WM_CAP_FILE_ALLOCATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489747"
---
# <a name="wm_cap_file_allocate-message"></a>\_Сообщение о \_ выделении файла крепления WM \_

Сообщение **о \_ \_ \_ выделении файла закрепления WM** создает (предварительно выделяет) файл записи указанного размера. Это сообщение можно отправить явно или с помощью макроса [**капфилеаллок**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) .


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*двсизе*
</dt> <dd>

Размер (в байтах) для создания файла записи.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.

## <a name="remarks"></a>Комментарии

Производительность захвата потоковой передачи значительно повышается за счет предварительного выделения файла записи, достаточного для хранения всего видеоклипа и дефрагментации файла записи перед записью клипа.

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

 

 





