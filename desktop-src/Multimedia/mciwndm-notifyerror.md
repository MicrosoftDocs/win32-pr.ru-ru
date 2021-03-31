---
title: Сообщение MCIWNDM_NOTIFYERROR (VFW. h)
description: Сообщение МЦИВНДМ \_ нотиферрор уведомляет родительское окно приложения о том, что произошла ошибка MCI.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071495"
---
# <a name="mciwndm_notifyerror-message"></a>\_Сообщение мЦивндм нотиферрор

Сообщение **мЦивндм \_ нотиферрор** уведомляет родительское окно приложения о том, что произошла ошибка MCI.


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Обработайте окно МЦивнд.

</dd> <dt>

<span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*Код ошибки*
</dt> <dd>

Числовой код для ошибки MCI.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Вы можете включить уведомление об ошибке MCI, указав \_ стиль окна мЦивндф нотиферрор.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





