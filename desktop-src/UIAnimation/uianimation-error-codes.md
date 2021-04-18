---
title: Коды ошибок анимации Windows (Winerror. h)
description: При возникновении ошибки анимация Windows возвращает код в виде значения HRESULT. В этом разделе содержится список кодов ошибок, относящихся к анимации Windows. Список общих кодов ошибок COM см. в разделе Коды ошибок COM.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691814"
---
# <a name="windows-animation-error-codes"></a>Коды ошибок анимации Windows

При возникновении ошибки анимация Windows возвращает код в виде значения **HRESULT** . В этом разделе содержится список кодов ошибок, относящихся к анимации Windows. Список общих кодов ошибок COM см. в разделе [коды ошибок COM](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**\_ \_ сбой создания пользовательского интерфейса E \_**
</dt> <dd> <dl> <dt>

0x802A0001
</dt> <dt>



Не удалось создать объект.


</dt> </dl> </dd> <dt>

<span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**\_ \_ вызвано завершение работы пользовательского интерфейса E \_**
</dt> <dd> <dl> <dt>

0x802A0002
</dt> <dt>



Метод [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) был вызван в диспетчере анимации, что привело к завершению работы диспетчера анимации, а также к освобождению всех переменных анимации и раскадровок, которые она создала.

> [!Note]  
> После [**завершения работы**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown)не удается вызвать методы для любого объекта анимации.

 


</dt> </dl> </dd> <dt>

<span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**Недопустимый повторный вход пользовательского интерфейса \_ E \_ \_**
</dt> <dd> <dl> <dt>

0x802A0003
</dt> <dt>



Этот метод не может быть вызван во время обратного вызова этого типа.


</dt> </dl> </dd> <dt>

<span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**\_объект UI \_ E \_ запечатан**
</dt> <dd> <dl> <dt>

0x802A0004
</dt> <dt>



Этот объект запечатан, поэтому это изменение больше не разрешено.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**значение пользовательского интерфейса \_ E \_ \_ не \_ задано**
</dt> <dd> <dl> <dt>

0x802A0005
</dt> <dt>



Запрошенное значение никогда не было задано и поэтому не может быть получено.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**значение пользовательского интерфейса \_ E \_ \_ не \_ определено**
</dt> <dd> <dl> <dt>

0x802A0006
</dt> <dt>



Не удается определить запрошенное значение.


</dt> </dl> </dd> <dt>

<span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**\_ \_ Недопустимый вывод пользовательского интерфейса E \_**
</dt> <dd> <dl> <dt>

0x802A0007
</dt> <dt>



Обратный вызов вернул недопустимый выходной параметр.


</dt> </dl> </dd> <dt>

<span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**\_ \_ ожидалось логическое значение пользовательского интерфейса E \_**
</dt> <dd> <dl> <dt>

0x802A0008
</dt> <dt>



Обратный вызов вернул код успешного выполнения, отличный от S \_ ОК или \_ false.


</dt> </dl> </dd> <dt>

<span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**Пользовательский интерфейс \_ E- \_ другой \_ владелец**
</dt> <dd> <dl> <dt>

0x802A0009
</dt> <dt>



Владельцем параметра, который должен быть владельцем этого объекта, является другой объект.


</dt> </dl> </dd> <dt>

<span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**\_ \_ неоднозначное соответствие пользовательского интерфейса E \_**
</dt> <dd> <dl> <dt>

0x802A000A
</dt> <dt>



Критерию поиска соответствует более одного элемента.


</dt> </dl> </dd> <dt>

<span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**\_переполнение пользовательского интерфейса E \_ FP \_**
</dt> <dd> <dl> <dt>

0x802A000B
</dt> <dt>



Произошло переполнение с плавающей точкой.


</dt> </dl> </dd> <dt>

<span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**Пользовательский интерфейс \_ E \_ неправильный \_ поток**
</dt> <dd> <dl> <dt>

0x802A000C
</dt> <dt>



Этот метод может быть вызван только из потока, в котором был создан объект.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**\_ \_ Активная раскадровка интерфейса E \_**
</dt> <dd> <dl> <dt>

0x802A0101
</dt> <dt>



Раскадровка в данный момент находится в расписании.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**\_раскадровка интерфейса E \_ \_ не \_ воспроизводилась**
</dt> <dd> <dl> <dt>

0x802A0102
</dt> <dt>



Раскадровка не воспроизводится.


</dt> </dl> </dd> <dt>

<span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**\_ \_ начальный \_ ОПОРНЫЙ кадр пользовательского интерфейса E \_ после \_ окончания**
</dt> <dd> <dl> <dt>

0x802A0103
</dt> <dt>



Начальный опорный кадр может находиться после конечного опорного кадра.


</dt> </dl> </dd> <dt>

<span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**\_ \_ конечный \_ ОПОРНЫЙ кадр пользовательского интерфейса E \_ не \_ определен**
</dt> <dd> <dl> <dt>

0x802A0104
</dt> <dt>



При достижении начального опорного кадра может быть невозможно определить время конечного опорного кадра.


</dt> </dl> </dd> <dt>

<span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**\_Перекрытие \_ циклов пользовательского интерфейса E \_**
</dt> <dd> <dl> <dt>

0x802A0105
</dt> <dt>



Две повторяющиеся части раскадровки могут перекрываться.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**Переход пользовательского интерфейса \_ E \_ \_ уже \_ используется**
</dt> <dd> <dl> <dt>

0x802A0106
</dt> <dt>



Переход уже добавлен в другую раскадровку или был добавлен в раскадровку, которая завершила воспроизведение и выпуск.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**Переход пользовательского интерфейса \_ E \_ \_ не \_ в \_ раскадровке**
</dt> <dd> <dl> <dt>

0x802A0107
</dt> <dt>



Переход не был добавлен в раскадровку.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**Переход пользовательского интерфейса \_ E в \_ \_ поeclipse**
</dt> <dd> <dl> <dt>

0x802A0108
</dt> <dt>



Переход может заeclipse начало другого перехода в раскадровке.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**\_время по электронной почты пользовательского интерфейса \_ \_ до \_ последнего \_ обновления**
</dt> <dd> <dl> <dt>

0x802A0109
</dt> <dt>



Указанное время предшествует времени, переданном последнему обновлению.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**\_ \_ клиент таймера пользовательского интерфейса E \_ \_ уже \_ подключен**
</dt> <dd> <dl> <dt>

0x802A010A
</dt> <dt>



Этот клиент уже подключен к таймеру.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista и обновление платформы \[ только для настольных приложений Windows Vista\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Header<br/>                   | <dl> <dt>Winerror. h</dt> </dl>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по анимации Windows](windows-animation-reference.md)
</dt> </dl>

 

