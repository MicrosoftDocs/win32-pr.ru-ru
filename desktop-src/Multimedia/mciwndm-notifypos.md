---
title: Сообщение MCIWNDM_NOTIFYPOS (VFW. h)
description: Сообщение МЦИВНДМ \_ нотифипос уведомляет родительское окно приложения о том, что его расположение изменилось.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989157"
---
# <a name="mciwndm_notifypos-message"></a>\_Сообщение мЦивндм нотифипос

Сообщение **мЦивндм \_ нотифипос** уведомляет родительское окно приложения о том, что его расположение изменилось.


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Обработайте окно МЦивнд.

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*POS*
</dt> <dd>

Описывает новую точку.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Вы можете включить уведомления об изменениях в положении окна МЦивнд, указав \_ стиль окна мЦивндф нотифипос.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





