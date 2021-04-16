---
title: Флаги сообщения указателя
description: Значения, используемые в различных макросах указателя (см. макросы).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719202"
---
# <a name="pointer-message-flags"></a>Флаги сообщения указателя

Значения, используемые в различных макросах указателя (см. [макросы](macros.md)).

<dl> <dt>

<span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Указывает поступление нового указателя.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Указывает, что этот указатель остается существующим. Если этот флаг не установлен, он указывает, что указатель имеет левый диапазон обнаружения.

Этот флаг обычно не устанавливается, только если указатель мыши выходит за пределы диапазона обнаружения (**POINTER_FLAG_UPDATE** задан) или если указатель в контакте с областью окна выходит за пределы диапазона обнаружения (**POINTER_FLAG_UP** установлен).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Указывает, что этот указатель находится в контакте с поверхностью дигитайзера. Если этот флаг не установлен, он указывает на наведение указателя мыши.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Указывает основное действие, аналогичное нажатию левой кнопки мыши.

Указатель касания имеет установленный флаг, когда он находится в контакте с поверхностью дигитайзера.

Для указателя пера установлен этот флаг, если он находится в контакте с поверхностью дигитайзера без нажатия кнопок.

Указатель мыши имеет этот флаг, установленный при нажатии левой кнопки мыши.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Указывает вторичное действие, аналогичное нажатию правой кнопки мыши.

Указатель касания не использует этот флаг.

Для указателя пера установлен этот флаг, если он находится в контакте с поверхностью дигитайзера с нажатой кнопкой пера.

Указатель мыши имеет этот флаг, установленный при нажатии правой кнопки мыши.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Аналогично кнопке колесика мыши вниз.

Указатель касания не использует этот флаг.

Указатель пера не использует этот флаг.

Указатель мыши имеет этот флаг, установленный при нажатии кнопки колесика мыши.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Аналог первой расширенной кнопки мыши (XButton1).

Указатель касания не использует этот флаг.

Указатель пера не использует этот флаг.

Указатель мыши имеет этот флаг, установленный при нажатии первой кнопки расширенной мыши (XBUTTON1).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Аналог второй кнопки расширенной мыши (XButton2).

Указатель касания не использует этот флаг.

Указатель пера не использует этот флаг.

Указатель мыши имеет этот флаг, установленный при нажатии второй кнопки расширенной мыши (XBUTTON2).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Указывает, что этот указатель был обозначен как основной указатель. Первичный указатель — это один указатель, который может выполнять действия, отличные от доступных для неосновных указателей. Например, когда основной указатель устанавливает контакт с областью окна, он может предоставить окну возможность активировать, отправив ему WM_POINTERACTIVATE сообщение.

Основной указатель определяется всеми действиями текущего пользователя в системе (мышь, касание, перо и т. д.). Таким образом, основной указатель может не быть связан с вашим приложением. Первый контакт в взаимодействии с несколькими касаниями устанавливается в качестве основного указателя. После идентификации основного указателя все контакты должны быть ликвидированы, прежде чем новый контакт будет идентифицирован как основной указатель. Для приложений, которые не обрабатывают ввод указателя, только события основного указателя переносятся в события мыши.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Достоверность — это предложение от исходного устройства о том, представляет ли указатель предполагаемое или случайное взаимодействие, которое особенно важно для PT_TOUCHных указателей, где случайное взаимодействие (например, с ладонью руки) может активировать ввод. Наличие этого флага означает, что исходное устройство имеет высокую уверенность в том, что эти входные данные являются частью предполагаемого взаимодействия.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Указывает, что указатель отменяется в ненормальном режиме, например, когда система получает недопустимые входные данные для указателя или когда устройство с активными указателями внезапно прерывается. Если приложение, получающее входные данные, находится в определенном месте, оно должно обрабатывать взаимодействие как незавершенное и обратить любое влияние на указатель.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

XBUTTON1 и XBUTTON2 — это дополнительные кнопки, используемые на многих устройствах мыши. Они возвращают те же данные, что и стандартные кнопки мыши.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы](constants.md)
</dt> <dt>

[Макросы](macros.md)
</dt> </dl>

 

 





