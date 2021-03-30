---
title: Константы WINBIO_PRESENCE_CHANGE (Винбио \_ types. h)
description: Описывает типы изменений, которые могут возникать, когда биометрическая платформа Windows наблюдает за присутствием отдельных пользователей.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071224"
---
# <a name="winbio_presence_change-constants"></a>\_ \_ Константы изменения присутствия винбио

Описывает типы изменений, которые могут возникать, когда биометрическая платформа Windows наблюдает за присутствием отдельных пользователей.



| Константа/значение                                                                                                                                                                                                                                                                                      | Описание                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <dt>**Винбио \_ \_Неизвестный \_ тип \_ изменения присутствия**</dt> <dt>0</dt> </dl>           | Тип события неизвестен. Это значение используется для неинициализированной структуры.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <dt>**Винбио \_ \_ \_ Обновление типа изменения \_ присутствия \_ все**</dt> <dt>1</dt> </dl> | Предоставляет сведения обо всех лицах, текущих в кадре камеры.<br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <dt>**Винбио \_ \_ \_ \_ Прибытие типа изменения присутствия**</dt> <dt>2</dt> </dl>              | Новый элемент, поступил в кадр камеры.<br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <dt>**Винбио \_ \_Тип изменения присутствия, \_ \_ распознаваемый**</dt> <dt>3</dt> </dl>     | Лицо было сопоставлено с зарегистрированным пользователем.<br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <dt>**Винбио \_ \_Тип изменения \_ присутствия \_ выбывают**</dt> <dt>4</dt> </dl>              | Ранее обнаруженная грань была вне рамки камеры в течение определенного периода времени.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <dt>**Винбио \_ \_Тип изменения \_ присутствия \_ Track**</dt> <dt>5</dt> </dl>                 | Предоставляет сведения об обновлении ограничивающего прямоугольника и отклонения подробных значений для подмножества лиц, которые в данный момент находятся в кадре камеры.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt> </dl> |



 

 





