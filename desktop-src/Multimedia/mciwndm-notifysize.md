---
title: Сообщение MCIWNDM_NOTIFYSIZE (VFW. h)
description: Сообщение МЦИВНДМ \_ нотифисизе уведомляет родительское окно приложения о том, что размер окна изменился.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- MCIWNDM_NOTIFYSIZE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135667"
---
# <a name="mciwndm_notifysize-message"></a>\_Сообщение мЦивндм нотифисизе

Сообщение **мЦивндм \_ нотифисизе** уведомляет родительское окно приложения о том, что размер окна изменился.


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Обработайте окно МЦивнд.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Вы можете включить уведомления об изменениях в размере окна МЦивнд, указав \_ стиль окна мЦивндф нотифисизе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





