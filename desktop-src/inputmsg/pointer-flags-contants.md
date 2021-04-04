---
title: Флаги указателя
description: Значения, которые могут отображаться в поле Поинтерфлагс структуры POINTER_INFO.
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802897"
---
# <a name="pointer-flags"></a>Флаги указателя

Значения, которые могут отображаться в поле **поинтерфлагс** структуры [**POINTER_INFO**](/previous-versions/windows/desktop/api) .

<dl> <dt>

<span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Значение по умолчанию


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Указывает поступление нового указателя.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Указывает, что этот указатель остается существующим. Если этот флаг не установлен, он указывает, что указатель имеет левый диапазон обнаружения.

Этот флаг обычно не устанавливается, только если указатель мыши выходит за пределы диапазона обнаружения (**POINTER_FLAG_UPDATE** задан) или если указатель в контакте с областью окна выходит за пределы диапазона обнаружения (**POINTER_FLAG_UP** установлен).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Указывает, что этот указатель находится в контакте с поверхностью дигитайзера. Если этот флаг не установлен, он указывает на наведение указателя мыши.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Указывает основное действие, аналогичное нажатию левой кнопки мыши.

Указатель касания имеет установленный флаг, когда он находится в контакте с поверхностью дигитайзера.

Для указателя пера установлен этот флаг, если он находится в контакте с поверхностью дигитайзера без нажатия кнопок.

Указатель мыши имеет этот флаг, установленный при нажатии левой кнопки мыши.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Указывает вторичное действие, аналогичное нажатию правой кнопки мыши.

Указатель касания не использует этот флаг.

Для указателя пера установлен этот флаг, если он находится в контакте с поверхностью дигитайзера с нажатой кнопкой пера.

Указатель мыши имеет этот флаг, установленный при нажатии правой кнопки мыши.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Аналогично кнопке колесика мыши вниз.

Указатель касания не использует этот флаг.

Указатель пера не использует этот флаг.

Указатель мыши имеет этот флаг, установленный при нажатии кнопки колесика мыши.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Аналог первой расширенной кнопки мыши (XButton1).

Указатель касания не использует этот флаг.

Указатель пера не использует этот флаг.

Указатель мыши имеет этот флаг, установленный при нажатии первой кнопки расширенной мыши (XBUTTON1).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Аналог второй кнопки расширенной мыши (XButton2).

Указатель касания не использует этот флаг.

Указатель пера не использует этот флаг.

Указатель мыши имеет этот флаг, установленный при нажатии второй кнопки расширенной мыши (XBUTTON2).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Указывает, что этот указатель был обозначен как основной указатель. Первичный указатель — это один указатель, который может выполнять действия, отличные от доступных для неосновных указателей. Например, когда основной указатель устанавливает контакт с областью окна, он может предоставить окну возможность активировать, отправив ему [**WM_POINTERACTIVATE**](wm-pointeractivate.md) сообщение.

Основной указатель определяется всеми действиями текущего пользователя в системе (мышь, касание, перо и т. д.). Таким образом, основной указатель может не быть связан с вашим приложением. Первый контакт в взаимодействии с несколькими касаниями устанавливается в качестве основного указателя. После идентификации основного указателя все контакты должны быть ликвидированы, прежде чем новый контакт будет идентифицирован как основной указатель. Для приложений, которые не обрабатывают ввод указателя, только события основного указателя переносятся в события мыши.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x000004000
</dt> <dt>



Достоверность — это предложение от исходного устройства о том, представляет ли указатель предполагаемое или случайное взаимодействие, которое особенно важно для PT_TOUCHных указателей, где случайное взаимодействие (например, с ладонью руки) может активировать ввод. Наличие этого флага означает, что исходное устройство имеет высокую уверенность в том, что эти входные данные являются частью предполагаемого взаимодействия.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x000008000
</dt> <dt>



Указывает, что указатель отменяется в ненормальном режиме, например, когда система получает недопустимые входные данные для указателя или когда устройство с активными указателями внезапно прерывается. Если приложение, получающее входные данные, находится в определенном месте, оно должно обрабатывать взаимодействие как незавершенное и обратить любое влияние на указатель.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Указывает, что этот указатель перешел в Нештатное состояние; то есть он сделал контакт с поверхностью дигитайзера.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Указывает, что это простое обновление, которое не включает изменение состояния указателя.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Указывает, что этот указатель перешел в состояние Up. Это значит, что контакт с поверхностью дигитайзера закончился.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Указывает входные данные, связанные с колесом-указателем. Для указателей мыши это эквивалентно действию колесика прокрутки мыши ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Указывает входные данные, связанные с указателем h-Wheel. Для указателей мыши это эквивалентно действию колеса горизонтальной прокрутки мыши ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Указывает, что этот указатель был захвачен (связан с) другим элементом, а исходный элемент потерял захват (см. [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Указывает, что этот указатель имеет связанное преобразование.


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

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**POINTER_BUTTON_CHANGE_TYPE**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

