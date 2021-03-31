---
title: Сообщение MCIWNDM_NOTIFYMODE (VFW. h)
description: Сообщение МЦИВНДМ \_ нотифимоде уведомляет родительское окно приложения о том, что режим работы устройства mci изменился.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071090"
---
# <a name="mciwndm_notifymode-message"></a>\_Сообщение мЦивндм нотифимоде

Сообщение **мЦивндм \_ нотифимоде** уведомляет родительское окно приложения о том, что режим работы устройства mci изменился.


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Обработайте окно МЦивнд.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*режима*
</dt> <dd>

Целое число, соответствующее режиму MCI.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Вы можете включить уведомления об изменениях режима устройства MCI, указав \_ стиль окна мЦивндф нотифимоде.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





