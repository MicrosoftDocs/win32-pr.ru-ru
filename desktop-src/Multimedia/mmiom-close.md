---
title: Сообщение MMIOM_CLOSE (Ммсистем. h)
description: '\_Сообщение о закрытии ммиом отправляется в процедуру ввода-вывода функцией ммиоклосе, чтобы запросить закрытие файла.'
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- сообщение MMIOM_CLOSE Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a26b8b2ffa80c7c522fa5cdcbfc5da3334e0d2b5e258e090932147bf85438c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065394"
---
# <a name="mmiom_close-message"></a>\_Сообщение о закрытии ммиом

Сообщение **о \_ закрытии ммиом** отправляется в процедуру ввода-вывода функцией [**ммиоклосе**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) , чтобы запросить закрытие файла.


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*лклосефлагс*
</dt> <dd>

Флаги, содержащиеся в параметре **вфлагс** объекта **ммиоклосе**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль, если файл успешно закрыт, или ошибка в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



 

