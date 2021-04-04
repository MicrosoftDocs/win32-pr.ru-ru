---
title: Константы WINBIO_REJECT_DETAIL (Винбио \_ types. h)
description: Укажите причину, по которой не удалось установить биометрические записи отпечатков пальцев или процедуры идентификации.
ms.assetid: b1ae4e65-9e53-42dd-99ba-1910b72688dd
topic_type:
- apiref
api_name:
- WINBIO_FP_TOO_HIGH
- WINBIO_FP_TOO_LOW
- WINBIO_FP_TOO_LEFT
- WINBIO_FP_TOO_RIGHT
- WINBIO_FP_TOO_FAST
- WINBIO_FP_TOO_SLOW
- WINBIO_FP_POOR_QUALITY
- WINBIO_FP_TOO_SKEWED
- WINBIO_FP_TOO_SHORT
- WINBIO_FP_MERGE_FAILURE
- WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK
- WINBIO_REJECT_DETAIL_POSITION_MASK
- WINBIO_REJECT_DETAIL_REASON_MASK
- WINBIO_IRIS_POOR_QUALITY
- WINBIO_IRIS_TOO_BRIGHT
- WINBIO_IRIS_TOO_DARK
- WINBIO_IRIS_SPOOF_DETECTED
- WINBIO_IRIS_TOO_SKEWED
- WINBIO_IRIS_TOO_CLOSED
- WINBIO_IRIS_GLARE
- WINBIO_IRIS_DIRTY_LENS
- WINBIO_IRIS_POOR_FOCUS
- WINBIO_IRIS_WRONG_ORIENTATION
- WINBIO_IRIS_TOO_HIGH
- WINBIO_IRIS_TOO_LOW
- WINBIO_IRIS_TOO_LEFT
- WINBIO_IRIS_TOO_RIGHT
- WINBIO_IRIS_TOO_NEAR
- WINBIO_IRIS_TOO_FAR
- WINBIO_FACE_POOR_QUALITY
- WINBIO_FACE_TOO_BRIGHT
- WINBIO_FACE_TOO_DARK
- WINBIO_FACE_SPOOF_DETECTED
- WINBIO_FACE_AMBIGUOUS_TARGET
- WINBIO_FACE_EYES_OCCLUDED
- WINBIO_FACE_WRONG_ORIENTATION
- WINBIO_FACE_TOO_HIGH
- WINBIO_FACE_TOO_LOW
- WINBIO_FACE_TOO_LEFT
- WINBIO_FACE_TOO_RIGHT
- WINBIO_FACE_TOO_NEAR
- WINBIO_FACE_TOO_FAR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d23dcf568e5ed25fb5081283a421b1c0dbb07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804048"
---
# <a name="winbio_reject_detail-constants"></a>\_ \_ Константы сведений об ОТКЛОНЕНии винбио

Следующие константы можно использовать для указания причины сбоя при захвате биометрической записи на отпечатке пальцев или процедуре идентификации.



| Константа                                                                                                                                                                                                                                        | Описание                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FP_TOO_HIGH"></span><span id="winbio_fp_too_high"></span><dl> <dt>**\_ \_ слишком большое винбио \_ FP**</dt> </dl>                                                                  | На пальце слишком много начато сканирование пальца.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_LOW"></span><span id="winbio_fp_too_low"></span><dl> <dt>**\_ \_ слишком низкое винбио \_ FP**</dt> </dl>                                                                     | На пальце не было слишком мало сканирования пальца.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_LEFT"></span><span id="winbio_fp_too_left"></span><dl> <dt>**ВИНБИО \_ FP \_ не \_ осталось**</dt> </dl>                                                                  | Палец находился слишком далеко во время сканирования.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_RIGHT"></span><span id="winbio_fp_too_right"></span><dl> <dt>**\_слишком винбио \_ FP \_**</dt> </dl>                                                               | Палец находился слишком далеко во время сканирования.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_FAST"></span><span id="winbio_fp_too_fast"></span><dl> <dt>**\_ \_ слишком быстрое винбио \_ FP**</dt> </dl>                                                                  | Палец слишком быстро находился на датчике.<br/>                                                                                                                                                                                                                                       |
| <span id="WINBIO_FP_TOO_SLOW"></span><span id="winbio_fp_too_slow"></span><dl> <dt>**\_ \_ слишком низкое винбио \_ FP**</dt> </dl>                                                                  | Палец слишком медленно находился на датчике.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_FP_POOR_QUALITY"></span><span id="winbio_fp_poor_quality"></span><dl> <dt>**\_ \_ низкое качество винбио \_ FP**</dt> </dl>                                                      | Слишком низкое качество сканирования.<br/>                                                                                                                                                                                                                                                         |
| <span id="WINBIO_FP_TOO_SKEWED"></span><span id="winbio_fp_too_skewed"></span><dl> <dt>**ВИНБИО \_ FP \_ слишком \_ наклонен**</dt> </dl>                                                            | Палец не прошел прямую по датчику.<br/>                                                                                                                                                                                                                                    |
| <span id="WINBIO_FP_TOO_SHORT"></span><span id="winbio_fp_too_short"></span><dl> <dt>**\_ \_ слишком короткий винбио \_ FP**</dt> </dl>                                                               | Недостаточный уровень сканирования пальца.<br/>                                                                                                                                                                                                                                                  |
| <span id="WINBIO_FP_MERGE_FAILURE"></span><span id="winbio_fp_merge_failure"></span><dl> <dt>**\_ \_ сбой слияния винбио \_ FP**</dt> </dl>                                                   | Не удалось объединить записи отпечатка пальца.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK____"></span><span id="winbio_reject_detail_anti_spoof_mask____"></span><dl> <dt>**Винбио \_ отклонить \_ сведения о \_ \_ \_ маске антифишинга**</dt> </dl> | Эта маска охватывает верхние 8 битов значения отклонения, где размещаются сведения о поведении подтверждения жизни. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_POSITION_MASK______"></span><span id="winbio_reject_detail_position_mask______"></span><dl> <dt>**Винбио \_ отклонить \_ \_ \_ маску сведений о положении**</dt> </dl>    | Эта маска охватывает диапазон битов, посвященных ошибкам позиционирования. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                                                         |
| <span id="WINBIO_REJECT_DETAIL_REASON_MASK"></span><span id="winbio_reject_detail_reason_mask"></span><dl> <dt>**ВИНБИО \_ отклонить \_ сведения о \_ причине \_ маски**</dt> </dl>                       | Эта маска охватывает младшие 16 бит, где находится перечисленная причина отклонения. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                           |
| <span id="WINBIO_IRIS_POOR_QUALITY"></span><span id="winbio_iris_poor_quality"></span><dl> <dt>**\_ \_ низкое качество ДИАФРАГМы винбио \_**</dt> </dl>                                                | Эти условия привели к тому, что камера захватывает неплохое изображение. Попросите пользователя очистить датчик и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_IRIS_TOO_BRIGHT"></span><span id="winbio_iris_too_bright"></span><dl> <dt>**ВИНБИОая \_ IRI \_ слишком \_ яркий**</dt> </dl>                                                      | Изображение содержит слишком большой внешний свет, чтобы получить хорошее соответствие. Попросите пользователя убедиться, что они не направлены на другой яркий источник освещения. Это значение поддерживается начиная с Windows 10.<br/>                                                                                        |
| <span id="WINBIO_IRIS_TOO_DARK"></span><span id="winbio_iris_too_dark"></span><dl> <dt>**\_ \_ слишком \_ темная винбиоая IRI**</dt> </dl>                                                            | Изображение слишком темно, чтобы получить хорошее соответствие. Попросите пользователя убедиться, что их IRI не скрывается такими элементами, как оказывающихся, темно очков или цветные контакты. Это значение поддерживается начиная с Windows 10.<br/>                                                                     |
| <span id="WINBIO_IRIS_SPOOF_DETECTED"></span><span id="winbio_iris_spoof_detected"></span><dl> <dt>**\_ \_ обнаружена подмена IRI винбио \_**</dt> </dl>                                          | Компонент распознавания считает, что IRI не работает, но поступает из воспроизводимого видеоканала, фотографии или трехмерной скулптуре. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_IRIS_TOO_SKEWED"></span><span id="winbio_iris_too_skewed"></span><dl> <dt>**ВИНБИОая \_ IRI \_ слишком \_ наклонена**</dt> </dl>                                                      | Пользователь не смотрит непосредственно на камере. Попросите пользователя просмотреть камеру и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                       |
| <span id="WINBIO_IRIS_TOO_CLOSED"></span><span id="winbio_iris_too_closed"></span><dl> <dt>**ВИНБИОая \_ IRI \_ слишком \_ закрыта**</dt> </dl>                                                      | Эйелидс пользователя скрывают IRI. Попросите пользователя снова открыть свои глаза и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                          |
| <span id="WINBIO_IRIS_GLARE"></span><span id="winbio_iris_glare"></span><dl> <dt>**ВИНБИО \_ IRI \_**</dt> </dl>                                                                      | Изображение включает объективное покрытие. Попросите пользователя удалить свои очков и проверить еще раз. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                               |
| <span id="WINBIO_IRIS_DIRTY_LENS"></span><span id="winbio_iris_dirty_lens"></span><dl> <dt>**ВИНБИОая \_ \_ неизмененная \_ линза**</dt> </dl>                                                      | Объектив камеры был изменен. Попросите пользователя очистить линзу и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                                         |
| <span id="WINBIO_IRIS_POOR_FOCUS"></span><span id="winbio_iris_poor_focus"></span><dl> <dt>**ВИНБИОная \_ IRI, \_ неплохая \_ фокусировка**</dt> </dl>                                                      | Эта IRI не имеет фокуса. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                                                                                             |
| <span id="WINBIO_IRIS_WRONG_ORIENTATION"></span><span id="winbio_iris_wrong_orientation"></span><dl> <dt>**\_ \_ неправильная ориентация винбио IRI \_**</dt> </dl>                                 | Ориентация камеры не совпадает с обязательной ориентацией, которую указывает [**Структура \_ \_ \_ сведений о расширенном датчике винбио**](winbio-extended-sensor-info.md) . Попросите пользователя изменить ориентацию и проверку камеры. Это значение поддерживается начиная с Windows 10.<br/> |
| <span id="WINBIO_IRIS_TOO_HIGH"></span><span id="winbio_iris_too_high"></span><dl> <dt>**\_ \_ слишком \_ Высокая винбиоая IRI**</dt> </dl>                                                            | IRI. Попросите пользователя немного проанализировать и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LOW"></span><span id="winbio_iris_too_low"></span><dl> <dt>**\_ \_ слишком низкое винбио \_ IRI**</dt> </dl>                                                               | IRI отключается. Попросите пользователя немного выполнить поиск и сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LEFT"></span><span id="winbio_iris_too_left"></span><dl> <dt>**ВИНБИОая \_ диафрагма \_ слишком \_ левая**</dt> </dl>                                                            | IRI слишком далеко не левее. Попросите пользователя еще раз просмотреть право и проверить его. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_RIGHT"></span><span id="winbio_iris_too_right"></span><dl> <dt>**слишком ВИНБИОая \_ IRI \_ \_**</dt> </dl>                                                         | IRI находится слишком далеко справа. Попросите пользователя еще немного взглянуть на левую и просканируйте. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_NEAR"></span><span id="winbio_iris_too_near"></span><dl> <dt>**ВИНБИОая \_ IRI \_ слишком \_ близка**</dt> </dl>                                                            | IRI слишком близко к камере. Попросите пользователя переместиться чуть дальше и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_IRIS_TOO_FAR"></span><span id="winbio_iris_too_far"></span><dl> <dt>**\_ \_ слишком \_ далеко винбиоая IRI**</dt> </dl>                                                               | IRI слишком далеко от камеры. Попросите пользователя переместиться чуть ближе и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                         |
| <span id="WINBIO_FACE_POOR_QUALITY"></span><span id="winbio_face_poor_quality"></span><dl> <dt>**\_ \_ низкое \_ качество винбионого лица**</dt> </dl>                                                | Эти условия привели к тому, что камера захватывает неплохое изображение. Попросите пользователя очистить датчик и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_FACE_TOO_BRIGHT"></span><span id="winbio_face_too_bright"></span><dl> <dt>**\_ \_ слишком \_ яркое винбионое лицо**</dt> </dl>                                                      | Изображение содержит слишком большой внешний свет, чтобы получить хорошее соответствие. Попросите пользователя убедиться, что они не направлены на другой яркий источник освещения. Это значение поддерживается начиная с Windows 10.<br/>                                                                                        |
| <span id="WINBIO_FACE_TOO_DARK"></span><span id="winbio_face_too_dark"></span><dl> <dt>**\_ \_ слишком \_ темная винбиоая рожица**</dt> </dl>                                                            | Изображение слишком темно, чтобы получить хорошее соответствие. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                                                                             |
| <span id="WINBIO_FACE_SPOOF_DETECTED"></span><span id="winbio_face_spoof_detected"></span><dl> <dt>**\_ \_ обнаружено имитация лица винбио \_**</dt> </dl>                                          | Компонент распознавания считает, что лицо не находится в режиме реального времени, но поступает из воспроизводимого видеоканала, фотографии или трехмерной скулптуре. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_FACE_AMBIGUOUS_TARGET"></span><span id="winbio_face_ambiguous_target"></span><dl> <dt>**\_ \_ неоднозначный \_ целевой объект винбио Face**</dt> </dl>                                    | Два или более лица перекрываются в рамке камеры. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                                                                     |
| <span id="WINBIO_FACE_EYES_OCCLUDED"></span><span id="winbio_face_eyes_occluded"></span><dl> <dt>**ВИНБИО \_ \_ глаза \_ перекрыто**</dt> </dl>                                             | Глаза пользователя — перекрыто. Попросите пользователя убедиться, что их глаза не закрываются такими элементами, как оказывающихся, темно очков или цветные контакты. Это значение поддерживается начиная с Windows 10.<br/>                                                                                 |
| <span id="WINBIO_FACE_WRONG_ORIENTATION"></span><span id="winbio_face_wrong_orientation"></span><dl> <dt>**\_ \_ неправильная \_ ориентация винбио**</dt> </dl>                                 | Ориентация камеры не совпадает с обязательной ориентацией, которую указывает [**Структура \_ \_ \_ сведений о расширенном датчике винбио**](winbio-extended-sensor-info.md) . Попросите пользователя изменить ориентацию и проверку камеры. Это значение поддерживается начиная с Windows 10.<br/> |
| <span id="WINBIO_FACE_TOO_HIGH"></span><span id="winbio_face_too_high"></span><dl> <dt>**\_ \_ слишком большое лицо \_ винбио**</dt> </dl>                                                            | Лицевой стороны. Попросите пользователя немного проанализировать и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LOW"></span><span id="winbio_face_too_low"></span><dl> <dt>**ВИНБИО \_ лицо \_ слишком \_ мало**</dt> </dl>                                                               | Грань отключается. Попросите пользователя немного выполнить поиск и сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LEFT"></span><span id="winbio_face_too_left"></span><dl> <dt>**ВИНБИО \_ лицо \_ слишком \_ оставило**</dt> </dl>                                                            | Лицо слишком далеко от левого края. Попросите пользователя переместиться вправо и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_RIGHT"></span><span id="winbio_face_too_right"></span><dl> <dt>**ВИНБИО \_ лицо \_ слишком \_ право**</dt> </dl>                                                         | Лицо слишком далеко от правого края. Попросите пользователя переместиться влево и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_NEAR"></span><span id="winbio_face_too_near"></span><dl> <dt>**ВИНБИОная \_ поверхность \_ слишком \_ близка**</dt> </dl>                                                            | Эта грань слишком близка к камере. Попросите пользователя переместиться чуть дальше и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_FACE_TOO_FAR"></span><span id="winbio_face_too_far"></span><dl> <dt>**ВИНБИО \_ лицо \_ слишком \_ далеко**</dt> </dl>                                                               | Лицо слишком далеко от камеры. Попросите пользователя переместиться чуть ближе и повторить сканирование. Это значение поддерживается начиная с Windows 10.<br/>                                                                                                                                         |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                                                                               |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                                                                                  |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> </dl>

 

 





