---
title: Сообщение MM_MIM_LONGDATA (Ммсистем. h)
description: сообщение MM \_ MIM \_ лонгдата отправляется в окно, когда получено сообщение об истечении времени получения из системы MIDI или если буфер заполнен данными, исключающий систему.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- сообщение MM_MIM_LONGDATA Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4748381500f42a5dc4f2bceae8ad862a64f237c9d5024e4b0b7cc96a694e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065524"
---
# <a name="mm_mim_longdata-message"></a>MM \_ MIM \_ сообщение лонгдата

сообщение **MM \_ MIM \_ лонгдата** отправляется в окно, когда получено сообщение об истечении времени получения из системы MIDI или если буфер заполнен данными, исключающий систему.


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*
</dt> <dd>

Обработчик для входного устройства MIDI, получившего данные.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*
</dt> <dd>

Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую буфер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Remarks

Возвращенный буфер может быть незаполненным. Чтобы определить число байтов, записанных в возвращенный буфер, используйте элемент **двбитесрекордед** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , на который указывает *лпмидихдр*.

Нет отметки времени, доступной для этого сообщения. Для входных данных с отметкой времени необходимо использовать сообщения, отправленные в функции обратного вызова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Цифровой интерфейс музыкальных инструментов (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

