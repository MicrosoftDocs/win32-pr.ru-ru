---
title: Константы WINBIO_BIOMETRIC_TYPE (Винбио \_ types. h)
description: Стандартные биометрические типы, определяемые национальным институтом стандартов и технологий (НИСТИР) 6529-A, иначе известной как общая биометрическая среда форматов Exchange (КБЕФФ) патрон формат A.
ms.assetid: DCBDB5F9-FF81-44C1-B439-2B8C02483212
topic_type:
- apiref
api_name:
- WINBIO_STANDARD_TYPE_MASK
- WINBIO_NO_TYPE_AVAILABLE
- WINBIO_TYPE_MULTIPLE
- WINBIO_TYPE_FACIAL_FEATURES
- WINBIO_TYPE_VOICE
- WINBIO_TYPE_FINGERPRINT
- WINBIO_TYPE_IRIS
- WINBIO_TYPE_RETINA
- WINBIO_TYPE_HAND_GEOMETRY
- WINBIO_TYPE_SIGNATURE_DYNAMICS
- WINBIO_TYPE_KEYSTROKE_DYNAMICS
- WINBIO_TYPE_LIP_MOVEMENT
- WINBIO_TYPE_THERMAL_FACE_IMAGE
- WINBIO_TYPE_THERMAL_HAND_IMAGE
- WINBIO_TYPE_GAIT
- WINBIO_TYPE_SCENT
- WINBIO_TYPE_DNA
- WINBIO_TYPE_EAR_SHAPE
- WINBIO_TYPE_FINGER_GEOMETRY
- WINBIO_TYPE_PALM_PRINT
- WINBIO_TYPE_VEIN_PATTERN
- WINBIO_TYPE_FOOT_PRINT
- WINBIO_TYPE_OTHER
- WINBIO_TYPE_PASSWORD
- WINBIO_TYPE_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d2ab5c41a3c2af26312c97a67d1179b50fd759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681890"
---
# <a name="winbio_biometric_type-constants"></a>\_Константы БИОметрического \_ типа винбио

Следующие константы представляют стандартные биометрические типы, определяемые национальным институтом стандартов и технологических данных (НИСТИР) 6529-A, иначе известной как общая биометрическая среда форматов Exchange (КБЕФФ) патрон формат A. В настоящее время поддерживается только **\_ \_ отпечаток типа винбио** .



| Константа                                                                                                                                                                                                            | Описание                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <dt>**\_Маска стандартного \_ типа \_ винбио**</dt> </dl>                 | Битовая маска, указывающая поддерживаемый набор биометрических факторов.<br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <dt>**ВИНБИО \_ . \_ тип \_ недоступен**</dt> </dl>                    | Нет доступных биометрических типов.<br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <dt>**Тип ВИНБИО ( \_ \_ несколько)**</dt> </dl>                                 | Указано несколько типов.<br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <dt>**\_функции винбио типа \_ лица \_**</dt> </dl>           | Для определения личности пользователя используются функции лиц.<br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <dt>**ВИНБИО \_ тип \_ голоса**</dt> </dl>                                          | Частота и шаблоны томов в голоса пользователя используются для определения удостоверения отдельного лица.<br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <dt>**\_отпечаток типа винбио \_**</dt> </dl>                        | Шаблоны отпечатков пальцев используются для определения личности пользователя.<br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <dt>**ВИНБИО \_ тип \_ диафрагмы**</dt> </dl>                                             | Шаблоны IRI используются для определения удостоверения отдельного лица. Это значение поддерживается начиная с Windows 10.<br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <dt>**\_тип винбио \_ Retina**</dt> </dl>                                       | Шаблоны ключе в Retina используются для определения удостоверения отдельного лица.<br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <dt>**\_геометрия типа винбио " \_ рука" \_**</dt> </dl>                 | Форма руки отдельного лица используется для определения удостоверения отдельного лица.<br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <dt>**\_ \_ Dynamics сигнатуры типа винбио \_**</dt> </dl>  | Шаблоны принудительной настройки, используемые отдельными лицами при подписывании имени, используются для определения удостоверения отдельного лица.<br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <dt>**\_тип винбио \_ клавиша \_ Dynamics**</dt> </dl>  | Шаблоны скорости и ошибок при вводе пользователем по отдельности используются для определения удостоверения отдельного лица.<br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <dt>**\_ \_ Перемещение LIP типа \_ винбио**</dt> </dl>                    | Изменения в пакетах LIP для отдельного лица, возникающие при диктовке, используются для определения удостоверения отдельного пользователя.<br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <dt>**\_изображение " \_ тепловая \_ поверхность" типа винбио \_**</dt> </dl> | Шаблоны температуры на лицевой стороне лица используются для определения удостоверения отдельного лица.<br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <dt>**\_ \_ изображение тепловой системы типа \_ винбио \_**</dt> </dl> | Шаблоны температуры в руки отдельного лица используются для определения удостоверения отдельного лица.<br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <dt>**\_тип винбио \_ гаит**</dt> </dl>                                             | Шаблоны движения, происходящие при использовании отдельных проходов для определения удостоверения отдельного лица.<br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <dt>**\_тип винбио \_ колючкой**</dt> </dl>                                          | Колючкой отдельного пользователя используется для определения удостоверения отдельного лица.<br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <dt>**\_тип винбио \_ ДНК**</dt> </dl>                                                | Последовательности ACID деоксирибонуклеик (ДНК) используются для определения удостоверения отдельного объекта.<br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <dt>**\_форма типа \_ винбио \_**</dt> </dl>                             | Форма, совзятка за год, используется для определения удостоверения отдельного лица.<br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <dt>**\_ \_ \_ геометрическая геометрия типа винбио**</dt> </dl>           | Фигуры пальцами отдельного лица используются для определения удостоверения отдельного лица.<br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <dt>**ВИНБИО \_ тип \_ \_ печати Palm**</dt> </dl>                          | Форма карманного компьютера используется для определения удостоверения отдельного лица.<br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <dt>**\_ \_ шаблон ключе типа \_ винбио**</dt> </dl>                    | Закономерности в веинс, расположенной под обложкой руки отдельного лица, используются для определения удостоверения отдельного лица.<br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <dt>**\_ \_ Печать нижнего колонтитула типа винбио \_**</dt> </dl>                          | Форма нижнего колонтитула используется для определения удостоверения лица.<br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <dt>**\_другой тип \_ винбио**</dt> </dl>                                          | Поддерживаемые биометрические данные не определяются текущими константами.<br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <dt>**\_пароль типа \_ винбио**</dt> </dl>                                 | Данные пароля используются для определения удостоверения отдельного пользователя.<br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <dt>**ВИНБИО \_ введите \_ ANY**</dt> </dl>                                                | Данные любого типа используются для определения удостоверения отдельного пользователя.<br/>                                                          |



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

 

 





