---
title: Сообщение MCIWNDM_PLAYFROM (VFW. h)
description: Сообщение МЦИВНДМ \_ плайфром воспроизводит содержимое устройства mci из указанного расположения в конец содержимого или до тех пор, пока другая команда не останавливает воспроизведение. Это сообщение можно отправить явно или с помощью макроса МЦивндплайфром.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- MCIWNDM_PLAYFROM сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988307"
---
# <a name="mciwndm_playfrom-message"></a>\_Сообщение мЦивндм плайфром

Сообщение **мЦивндм \_ плайфром** ВОСПРОИЗВОДИТ содержимое устройства mci из указанного расположения в конец содержимого или до тех пор, пока другая команда не останавливает воспроизведение. Это сообщение можно отправить явно или с помощью макроса [**мЦивндплайфром**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*лпос*
</dt> <dd>

Начальное расположение. Единицы начального расположения зависят от текущего формата времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Можно также указать начальное и конечное расположение для воспроизведения с помощью макроса [**мЦивндплайфромто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндплайфром**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[**мЦивндплайфромто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





