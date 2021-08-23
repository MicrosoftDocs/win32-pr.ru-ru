---
title: Константы WINBIO_IRIS (Винбио \_ types. h)
description: Укажите типы для распознавания IRI.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd528bc9a902379591fb6d9587fa66bda9df50ad74cb5e5723f8646a53609a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909963"
---
# <a name="winbio_iris-constants"></a>\_Константы IRI винбио

Следующие константы — это значения **\_ \_ ПОДтипа БИОметрической метрики винбио** , которые можно использовать для указания типов для распознавания IRI за пределами ANSI ИнЦитс 379-2004: "формат IRI Image Interchange", который не определяет значения видимости слева и справа:



| Константа/значение                                                                                                                                                                                                                                                                   | Описание                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <dt> **\_ Неизвестный \_ тип \_ диафрагмы винбио**</dt> <dt>0</dt> </dl>                       | Тип диафрагмы неизвестен. <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <dt> **\_ \_ \_ Винбиоая**</dt> <dt>0xF5а</dt> IRI </dl>                               | Тип IRI является левым глазом. <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <dt> **\_ \_ \_ Винбиоая**</dt> <dt>0xF6а</dt> IRI </dl>                            | Тип IRI является верным глазом. <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <dt>**Винбио \_ IRI \_ НЕуказанная \_ POS \_ 01**</dt> <dt>0xF7</dt> </dl>    | Подтип, связанный с первым шаблоном пользователя, если только один глаз является кадром камеры и не может быть определен, является ли он пользовательским.<br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <dt> **Винбиоая IRI, не \_ \_ указанная \_ POS \_ 02**</dt> <dt>0xf8</dt> </dl> | Подтип, связанный с вторым шаблоном пользователя, когда только один глаз является кадром камеры, и не может быть определен, является ли он продолжением пользователя или вправо.<br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <dt> **Винбиоая \_ диафрагма \_ \_**</dt> <dt>0xF9</dt> </dl>                             | Тип IRI — это оба глаза. <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <dt> **Винбио \_ \_ \_ диафрагмы**</dt> <dt>0xFA</dt> </dl>                          | Тип диафрагмы — это либо глаз. <br/>                                                                                                                              |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



 

 





