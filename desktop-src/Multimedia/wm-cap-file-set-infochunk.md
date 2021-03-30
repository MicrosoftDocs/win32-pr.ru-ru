---
title: Сообщение WM_CAP_FILE_SET_INFOCHUNK (VFW. h)
description: '\_ \_ \_ Сообщение инфочунк Set WM Cap \_ устанавливает и очищает информационные блоки.'
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071150"
---
# <a name="wm_cap_file_set_infochunk-message"></a>\_Сообщение о \_ \_ задании файла \_ ИНФОЧУНК с ограничением WM

Сообщение **\_ \_ \_ \_ инфочунк Set WM Cap** устанавливает и очищает информационные блоки. Фрагменты информации могут быть вставлены в файл AVI во время записи, чтобы внедрять текстовые строки или пользовательские данные. Это сообщение можно отправить явно или с помощью макроса [**капфилесетинфочунк**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*лпинфочунк*
</dt> <dd>

Указатель на структуру [**капинфочунк**](/windows/win32/api/vfw/ns-vfw-capinfochunk) , определяющую создаваемый или удаляемый блок сведений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.

## <a name="remarks"></a>Комментарии

В файл AVI можно добавить несколько блоков зарегистрированных данных. После установки информационного блока он добавляется в последующие файлы записи до тех пор, пока не будет снята запись или не будут удалены все записи фрагментов данных. Чтобы очистить одну запись, укажите фрагмент данных в элементе **фкЦинфоид** и **значение NULL** в элементе **лпдата** структуры [**капинфочунк**](/windows/win32/api/vfw/ns-vfw-capinfochunk) . Чтобы очистить все записи, укажите **значение NULL** в **фкЦинфоид**.

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

 

 





