---
title: Сообщение WM_CAP_SET_SEQUENCE_SETUP (VFW. h)
description: В \_ сообщении о настройке закрепления WM \_ Set \_ Sequence \_ устанавливаются параметры конфигурации, используемые для сбора потоковой передачи. Это сообщение можно отправить явно или с помощью макроса Капкаптуресетсетуп.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- WM_CAP_SET_SEQUENCE_SETUP сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535339"
---
# <a name="wm_cap_set_sequence_setup-message"></a>\_ \_ \_ Сообщение настройки установки последовательностей WM Cap \_

В сообщении о **\_ настройке закрепления WM \_ Set \_ Sequence \_** устанавливаются параметры конфигурации, используемые для сбора потоковой передачи. Это сообщение можно отправить явно или с помощью макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) .


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*
</dt> <dd>

Размер (в байтах) структуры, на которую ссылается **s**.

</dd> <dt>

<span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*пскаппармс*
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

 

 





