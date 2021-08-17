---
title: Сообщение MM_WIM_DATA (Ммсистем. h)
description: Сообщение с \_ данными WIM в \_ формате mm отправляется в окно, когда в входном буфере содержатся аудиоданные-аудиозаписи и буфер возвращается приложению. Сообщение может быть отправлено либо при заполнении буфера, либо после вызова функции Вавеинресет.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- сообщение MM_WIM_DATA Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b209e59032c0da4c875a316008c889cf064ae7d8bc48f5c621125a06582673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065474"
---
# <a name="mm_wim_data-message"></a>MM \_ , \_ сообщение с данными WIM

Сообщение **с \_ \_ данными WIM** в формате mm отправляется в окно, когда в входном буфере содержатся аудиоданные-аудиозаписи и буфер возвращается приложению. Сообщение может быть отправлено либо при заполнении буфера, либо после вызова функции [**вавеинресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*хинпутдев*
</dt> <dd>

Обработано устройство ввода аудио-сигнала, которое получило данные.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*лпввхдр*
</dt> <dd>

Указатель на структуру [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , определяющую буфер, содержащий данные.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Remarks

Возвращенный буфер может быть незаполненным. Чтобы определить число байтов, записанных в возвращенный буфер, используйте элемент **двбитесрекордед** структуры [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , заданную параметром *lParam* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Звуковая волна](waveform-audio.md)
</dt> <dt>

[Сообщения волны](waveform-messages.md)
</dt> </dl>

 

