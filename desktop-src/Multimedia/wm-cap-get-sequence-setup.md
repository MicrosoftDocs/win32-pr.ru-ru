---
title: Сообщение WM_CAP_GET_SEQUENCE_SETUP (VFW. h)
description: Сообщение о \_ настройке "получение последовательности" WM Cap \_ \_ \_ получает текущие параметры параметров сбора потоковой передачи. Это сообщение можно отправить явно или с помощью макроса Капкаптурежетсетуп.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- WM_CAP_GET_SEQUENCE_SETUP сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988172"
---
# <a name="wm_cap_get_sequence_setup-message"></a>\_Сообщение о \_ \_ настройке получения последовательностей WM Cap \_

Сообщение **о \_ \_ \_ \_ настройке "получение последовательности" WM Cap** получает текущие параметры параметров сбора потоковой передачи. Это сообщение можно отправить явно или с помощью макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) .


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*
</dt> <dd>

Размер (в байтах) структуры, на которую ссылается **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*#d0*
</dt> <dd>

Указатель на структуру [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Сведения о параметрах, используемых для управления потоковой передачей, см. в разделе Структура [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .

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

 

 





