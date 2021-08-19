---
title: Команда MCI_GETDEVCAPS (Ммсистем. h)
description: Команда MCI \_ жетдевкапс получает статические сведения об устройстве.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- команда MCI_GETDEVCAPS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7798f72405209f9834c3b67f84e57508c58ffc6153bce860b91f089005648905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803960"
---
# <a name="mci_getdevcaps-command"></a>\_Команда MCI жетдевкапс

Команда MCI \_ жетдевкапс получает статические сведения об устройстве. Все устройства распознают эту команду. Параметры и флаги, доступные для этой команды, зависят от выбранного устройства. Сведения возвращаются в элементе **двретурн** структуры, определенной параметром *лпкапспармс*.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*
</dt> <dd>

Идентификатор устройства MCI, который должен получить командное сообщение.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ . Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*лпкапспармс*
</dt> <dd>

Указатель на структуру [**\_ \_ пармс MCI жетдевкапс**](mci-getdevcaps-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Следующие дополнительные стандартные и специальные флаги применяются ко всем устройствам, поддерживающим MCI \_ жетдевкапс:

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>\_ \_ составное устройство MCI жетдевкапс \_
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство использует хранилище данных, которое необходимо явно открыть и закрыть. в противном случае устанавливается значение **false** .

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>\_ \_ тип устройства mci \_ жетдевкапс
</dt> <dd>

Для элемента **двретурн** задается одно из значений, перечисленных в списке [типы устройств MCI](mci-device-types.md).

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ жетдевкапс \_ имеет \_ аудио
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство имеет звуковые выходные данные; в противном случае устанавливается значение **false** .

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ жетдевкапс \_ имеет \_ видео
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство имеет выходные данные видео; в противном случае устанавливается значение **false** . Например, члену присваивается **значение true** для устройств, поддерживающих набор команд видеодиск.

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>\_элемент ЖЕТДЕВКАПС \_ MCI
</dt> <dd>

Указывает, что элемент **двитем** структуры [**\_ \_ пармс жетдевкапс**](mci-getdevcaps-parms.md) содержит одну из следующих констант:

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>\_ЖЕТДЕВКАПС MCI \_ может \_ извлечь
</dt> <dd>

Член **двретурн** имеет значение **true** , если устройство может извлечь носитель; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>\_ \_ может играть жетдевкапс \_ MCI
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может воспроизвести носитель; в противном случае для него задается значение **false**. Если на устройстве указано **значение true**, это означает, что устройство поддерживает команды [ \_ приостановки](mci-pause.md) и [ \_ остановки](mci-stop.md) MCI, а также команду [MCI \_ Play](mci-play.md) .

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ жетдевкапс \_ может \_ записывать
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство поддерживает запись; в противном случае для него задается значение **false**. Если на устройстве указано **значение true**, это означает, что устройство поддерживает \_ команды приостановки и остановки MCI, а \_ также команду [MCI \_ Record](mci-record.md) .

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>\_ЖЕТДЕВКАПС MCI \_ может \_ сохранить
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может сохранить файл; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ жетдевкапс \_ использует \_ файлы
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройству требуется имя файла; в противном случае устанавливается значение **false** . Файлы используются только для составных устройств.

</dd> </dl>

Следующие флаги можно указать в элементе **Двитем** [**MCI \_ жетдевкапс \_ пармс**](mci-getdevcaps-parms.md) для типа устройства **дигиталвидео** :

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ ДГВ \_ жетдевкапс \_ может \_ заморозить
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может заморозить кадры; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>\_жетдевкапс ДГВ \_ MCI \_ может \_ блокировать
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может блокироваться; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>\_ДГВ MCI \_ жетдевкапс \_ может \_ обратить
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может воспроизводиться в обратную; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>\_ДГВ MCI \_ жетдевкапс \_ может выполнять \_ str \_
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может растягивать входные данные; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>\_жетдевкапс ДГВ \_ MCI \_ может \_ растянуть
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может растянуть изображение; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>\_ДГВ MCI \_ жетдевкапс \_ может \_ тестировать
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может выполнять тесты; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ ДГВ \_ жетдевкапс \_ \_ по-прежнему
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может отображать изображения по-прежнему. в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>\_ДГВ \_ жетдевкапс ( \_ Максимальное число \_ окон MCI)
</dt> <dd>

Для элемента **двретурн** задается максимальное число окон, которое устройство может одновременно обрабатывало.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>\_ \_ \_ Максимальная \_ Частота жетдевкапс MCI ДГВ
</dt> <dd>

Элемент **двретурн** задает максимальную скорость воспроизведения для устройства в кадрах в секунду.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>\_ \_ \_ Минимальная \_ Частота жетдевкапс MCI ДГВ
</dt> <dd>

Для элемента **двретурн** устанавливается минимальная скорость воспроизведения для устройства, в кадрах в секунду.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>\_ \_ палитры MCI ДГВ жетдевкапс \_
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может возвращать маркер палитры; в противном случае для него задается значение **false**.

</dd> </dl>

Следующие флаги можно указать в элементе **Двитем** [**MCI \_ жетдевкапс \_ пармс**](mci-getdevcaps-parms.md) для типа устройства **видеомагнитофона** :

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>\_ \_ \_ Частота приращения часов жетдевкапс MCI \_
</dt> <dd>

Для элемента **двретурн** задается число приращений в секунду.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может \_ определить \_ длину
</dt> <dd>

Член **двретурн** имеет значение **true** , если устройство может определить длину носителя; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может \_ заморозить
</dt> <dd>

Член **двретурн** имеет значение **true** , если устройство может заморозить выходное изображение; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может \_ отслеживать \_ источники
</dt> <dd>

Член **двретурн** имеет значение **true** , если устройство может отслеживать источники. в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может \_ выполнить предпробную выгрузку
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство поддерживает предустановку; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может быть \_ предварительной версией
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство поддерживает предварительный просмотр; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может быть \_ обратным
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может воспроизводить в обратную, в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может \_ протестировать
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство поддерживает тестирование; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>видеомагнитофон MCI \_ \_ жетдевкапс \_ имеет \_ Часы
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство поддерживает внешние часы; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>код \_ видеомагнитофона MCI \_ жетдевкапс \_ имеет \_ код времени
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство имеет функцию времени в виде времени или если эта возможность неизвестна. в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ число \_ \_ меток
</dt> <dd>

Для элемента **двретурн** задается число меток (99).

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>\_ \_ \_ точность поиска жетдевкапс видеомагнитофона \_ MCI
</dt> <dd>

Для элемента **двретурн** задана точность поиска устройства.

</dd> </dl>

Следующие флаги можно указать в элементе **Двитем** [**MCI \_ жетдевкапс \_ пармс**](mci-getdevcaps-parms.md) для типа устройства **оверлея** :

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ овли \_ жетдевкапс \_ может \_ заморозить
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может заморозить образ; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>\_жетдевкапс ОВЛИ \_ MCI \_ может \_ растянуть
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если устройство может растянуть изображение для заполнения рамки; в противном случае для него задается значение **false**.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>\_овли \_ жетдевкапс ( \_ Максимальное число \_ окон MCI)
</dt> <dd>

Для элемента **двретурн** задается максимальное число окон, которое устройство может одновременно обрабатывало.

</dd> </dl>

Следующие флаги можно указать в элементе **Двитем** [**MCI \_ жетдевкапс \_ пармс**](mci-getdevcaps-parms.md) для типа устройства **видеодиск** :

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>\_VD MCI \_ жетдевкапс \_ может \_ обратить
</dt> <dd>

Элемент **двретурн** имеет значение **true** , если проигрыватель видеодиск может воспроизводиться в обратную, в противном случае для него задается значение **false**. Некоторые игроки могут воспроизводить CLV диски в обратную, а также на Кав дисках.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ VD \_ жетдевкапс \_ Кав
</dt> <dd>

При объединении с другими элементами указывает, что возвращаемые сведения применяются к Кав формата видеодискс. Это значение по умолчанию, если видеодиск не вставлен.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ жетдевкапс \_ CLV
</dt> <dd>

При объединении с другими элементами указывает, что возвращаемые сведения применяются к CLV формата видеодискс.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>\_ \_ \_ частота FAST жетдевкапс MCI \_ VD
</dt> <dd>

Для элемента **двретурн** задана стандартная частота быстрого воспроизведения в кадрах за секунду.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>\_ \_ \_ нормальная ставка mCi VD жетдевкапс \_
</dt> <dd>

Для элемента **двретурн** задана нормальная скорость воспроизведения в кадрах за секунду.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>скорость работы MCI \_ VD \_ жетдевкапс \_ \_
</dt> <dd>

Для элемента **двретурн** задана Стандартная скорость воспроизведения кадров в секунду.

</dd> </dl>

Следующие флаги можно указать в элементе **Двитем** [**MCI \_ жетдевкапс \_ пармс**](mci-getdevcaps-parms.md) для типа устройства **вавеаудио** :

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>\_ \_ \_ входные данные MCI Wave жетдевкапс
</dt> <dd>

Для элемента **двретурн** задается общее количество входных устройств аудио (запись).

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>\_ \_ выходные данные жетдевкапса MCI Wave \_
</dt> <dd>

Для элемента **двретурн** задается общее количество устройств вывода аудио (воспроизведение).

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Команды MCI](mci-commands.md)
</dt> </dl>

 

