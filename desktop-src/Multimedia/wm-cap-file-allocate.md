---
title: Сообщение WM_CAP_FILE_ALLOCATE (VFW. h)
description: '\_ \_ \_ Сообщение о выделении файла закрепления WM создает (предварительно выделяет) файл записи указанного размера. Это сообщение можно отправить явно или с помощью макроса Капфилеаллок.'
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- сообщение WM_CAP_FILE_ALLOCATE Windows мультимедиа
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
ms.openlocfilehash: e76f0e88642d7d28771090b0690191eb4e4e72f5749dc74a9e42d90bfea87812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781404"
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

## <a name="remarks"></a>Remarks

Производительность захвата потоковой передачи значительно повышается за счет предварительного выделения файла записи, достаточного для хранения всего видеоклипа и дефрагментации файла записи перед записью клипа.

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

 

 





