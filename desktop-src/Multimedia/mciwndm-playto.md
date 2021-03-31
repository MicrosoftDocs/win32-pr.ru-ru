---
title: Сообщение MCIWNDM_PLAYTO (VFW. h)
description: Сообщение МЦИВНДМ \_ плайто воспроизводит содержимое устройства mci из текущей позиции в указанное конечное расположение или до тех пор, пока другая команда не останавливает воспроизведение.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137066"
---
# <a name="mciwndm_playto-message"></a>\_Сообщение мЦивндм плайто

Сообщение **мЦивндм \_ плайто** ВОСПРОИЗВОДИТ содержимое устройства mci из текущей позиции в указанное конечное расположение или до тех пор, пока другая команда не останавливает воспроизведение. Если указанное конечное расположение находится за пределами конца содержимого, воспроизведение останавливается в конце содержимого. Это сообщение можно отправить явно или с помощью макроса [**мЦивндплайто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Пользование*
</dt> <dd>

Конечное расположение. Единицы для конечного расположения зависят от текущего формата времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Этот макрос определяется с помощью макросов [**мЦивндсик**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) и [**мЦивндплайто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) , который, в свою очередь, использует команду [MCI \_ Seek](mci-seek.md) и сообщение **мЦивндм \_ плайто** .

Можно также указать начальное и конечное расположение для воспроизведения с помощью макроса [**мЦивндплайфромто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[\_Поиск MCI](mci-seek.md)
</dt> <dt>

[**мЦивндплайфромто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**мЦивндплайто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**мЦивндсик**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





