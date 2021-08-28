---
description: Определяет значения, указывающие свойства пакета.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Константы Паккетпропертигуидс (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b88a59d63bc8b45ea04e133f0d002fa86e35e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481080"
---
# <a name="packetpropertyguids-constants"></a>Константы Паккетпропертигуидс

Определяет значения, указывающие свойства пакета. В планшетном ПКАПИ используются идентификаторы GUID для идентификации свойств пакетов, которые в COM являются константными строками.

в C++ вы можете получить доступ к этим константам в файле заголовка мсинкаут. h, который находится в папке <systemdrive> : \\ Program files \\ Microsoft sdks \\ Windows \\ v 6.0 \\ Include, если пакет SDK установлен в расположение по умолчанию. В C++ эти константы являются Вчарс, а не BSTRs. Преобразуйте их в BSTRs перед использованием. Дополнительные сведения о типе данных BSTR см. в разделе [Использование библиотеки COM](using-the-com-library.md).

В следующей таблице перечислены доступные поля свойств пакетов с глобальным уникальным идентификатором (GUID). Используйте эти идентификаторы GUID, чтобы указать, какие свойства пакет содержит при создании контекста планшета. Чтобы определить диапазон и разрешение свойства, вызовите метод [**жетпропертиметрикс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) . Константы в таблице ниже, начиная с "STR \_ ", представляют собой строковые представления соответствующих двоичных констант, показанных в той же ячейке таблицы.




| Константа | Описание | 
|----------|-------------|
| <span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl><dt><strong>STR_GUID_X или GUID_PACKETPROPERTY_GUID_X</strong></dt></dl> | Координата x в пространстве координат планшета. Каждый пакет содержит это свойство по умолчанию. Источник (0, 0) планшета — левый верхний угол.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y или GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | Координата y в пространстве координат планшета. Каждый пакет содержит это свойство по умолчанию. Источник (0, 0) планшета — левый верхний угол.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y или GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | Координата y в пространстве координат планшета. Каждый пакет содержит это свойство по умолчанию. Источник (0, 0) планшета — левый верхний угол.<br /> | 
| <span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl><dt><strong>STR_GUID_Z или GUID_PACKETPROPERTY_GUID_Z</strong></dt></dl> | Z-координата или расстояние от кончика пера с поверхности планшета. Тип перечисления <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>таблетпропертиметрикунит</strong></a> определяет единицу измерения для этого свойства.<br /> | 
| <span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl><dt><strong>STR_GUID_PAKETSTATUS или GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt></dl> | Содержит одно или несколько следующих значений флагов:<br /><ul><li>Курсор касается поверхности рисования (значение = 1).</li><li>Курсор инвертирован. Например, конец пера указывает на поверхность (значение = 2).</li><li>Не используется (значение = 4).</li><li>Нажата кнопка пера (Value = 8).</li></ul> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK или GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | Время создания пакета.<br /> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK или GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | Время создания пакета.<br /> | 
| <span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl><dt><strong>STR_GUID_SERIALNUMBER или GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt></dl> | Свойство пакета для идентификации пакета.<br /> Это то же значение, которое используется для получения пакета из очереди пакетов.<br /> | 
| <span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl><dt><strong>STR_GUID_NORMALPRESSURE или GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt></dl> | Давление кончика пера перпендикулярно поверхности планшета.<br /> Чем больше нажим на кончик пера, тем больше чернил рисуется.<br /> | 
| <span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl><dt><strong>STR_GUID_TANGENTPRESSURE или GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt></dl> | Давление кончика пера вдоль плоскости планшета.<br /> | 
| <span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl><dt><strong>STR_GUID_BUTTONPRESSURE или GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt></dl> | Давление нажатия на кнопку с учетом нажима.<br /> | 
| <span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_XTILTORIENTATION или GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt></dl> | Угол между y, z-плоскостью и плоскостью пера и оси y.<br /> Применяется к курсору пера.<br /> Значение равно 0, если перо расположено перпендикулярно области рисования и положительное, когда перо находится справа от перпендикулярного.<br /> | 
| <span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_YTILTORIENTATION или GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt></dl> | Угол между плоскостью x, z и плоскостью пера и оси x.<br /> Применяется к курсору пера.<br /> Значение равно 0, когда перо расположено перпендикулярно поверхности рисования и положительно, когда перо перемещается от пользователя вверх или вниз.<br /> | 
| <span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl><dt><strong>STR_GUID_AZIMUTHORIENTATION или GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt></dl> | Поворот курсора относительно оси z по часовой стрелке через полный круговой диапазон.<br /> | 
| <span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl><dt><strong>STR_GUID_ALTITUDEORIENTATION или GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt></dl> | Угол между осью пера и поверхностью планшета.<br /> Значение равно 0, если перо находится рядом с поверхностью и 90, когда перо расположено перпендикулярно поверхности.<br /> При инвертировании пера значения становятся отрицательными.<br /> | 
| <span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl><dt><strong>STR_GUID_TWISTORIENTATION или GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt></dl> | Поворот курсора по часовой стрелке относительно своей собственной оси.<br /> | 
| <span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl><dt><strong>STR_GUID_PITCHROTATION или GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt></dl> | Свойство Packet, которое указывает, находится ли tip над горизонтальной линией или под ней, перпендикулярной поверхности письма.<br /><blockquote>[!Note]<br />Для этого требуется трехмерный дигитайзер.</blockquote><br /> Значение является положительным, если Совет находится над линией, и отрицательно, если он находится ниже строки. Например, если вы держите перо перед вами и пишете на мнимой стене, то этот шаг будет положительным, если Совет находится над линией, переданной на стену.<br /> | 
| <span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl><dt><strong>STR_GUID_ROLLROTATION или GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt></dl> | Поворот пера по часовой стрелке вокруг его собственной оси. <br /><blockquote>[!Note]<br />Для этого требуется трехмерный дигитайзер.</blockquote><br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION или GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | Угол пера слева или справа от центра его горизонтальной оси, когда перо горизонтально.<br /><blockquote>[!Note]<br />Для этого требуется трехмерный дигитайзер.</blockquote><br /> Если вы удерживаете перо перед вами и пишете на мнимой стене, ноль значения нутации указывает, что перо перпендикулярно стене. Значение является отрицательным, если TIP расположен слева от перпендикулярного и положительного, если TIP расположен справа от перпендикулярного.<br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION или GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | Угол пера слева или справа от центра его горизонтальной оси, когда перо горизонтально.<br /><blockquote>[!Note]<br />Для этого требуется трехмерный дигитайзер.</blockquote><br /> Если вы удерживаете перо перед вами и пишете на мнимой стене, ноль значения нутации указывает, что перо перпендикулярно стене. Значение является отрицательным, если TIP расположен слева от перпендикулярного и положительного, если TIP расположен справа от перпендикулярного.<br /> | 
| <span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl><dt><strong>STR_GUID_WIDTH или GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt></dl> | Ширина области контакта в сенсорном дигитайзере.<br /> | 
| <span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl><dt><strong>STR_GUID_HEIGHT или GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt></dl> | Высота контактной зоны на сенсорном дигитайзере.<br /> | 
| <span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE или GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt></dl> | Уровень достоверности пальца в сенсорном дигитайзере.<br /> | 
| <span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl><dt><strong>STR_GUID_DEVICE_CONTACT_ID или GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt></dl> | Идентификатор контакта устройства для пакета.<br /> | 




## <a name="remarks"></a>Комментарии

> [!Note]  
> Все значения пакетов, поступающие от оборудования планшета, являются целыми числами размером 32 бит.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Метод Испаккетпропертисуппортед**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[**Метод Жетпропертиметрикс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[**Интерфейс Иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




