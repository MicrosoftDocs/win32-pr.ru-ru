---
description: '\_Перечисление событий участника описывает события участников.'
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: Перечисление PARTICIPANT_EVENT (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5eb7a98a445ecb89b25fe2d18ef77be31aa54b5fac2920814fba2c4a3f6b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959774"
---
# <a name="participant_event-enumeration"></a>\_Перечисление событий участников

\[это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Перечисление **\_ событий участника** описывает события участников. Метод [**\_ события итпартиЦипантевент:: Get**](itparticipantevent-get-event.md) возвращает член этого перечисления для указания типа произошедшего события участника конференции. Это перечисление используется приложениями, которые обращаются к [ИПКОНФ MSP](ipconf-msp.md).

## <a name="syntax"></a>Синтаксис


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_новый \_ участник PE**
</dt> <dd>

На конференцию был добавлен новый участник.

</dd> <dt>

<span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**\_изменение сведений \_ PE**
</dt> <dd>

Изменились сведения об участнике.

</dd> <dt>

<span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**\_Выход участника \_ PE**
</dt> <dd>

Участник покинул конференцию.

</dd> <dt>

<span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**\_новый \_ ПОДпоток PE**
</dt> <dd>

К участнику добавлен новый подпоток.

</dd> <dt>

<span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**\_ПОДПОТОК PE \_ удален**
</dt> <dd>

Новый подпоток был удален из участника.

</dd> <dt>

<span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**\_сопоставленный ПОДПОТОК PE \_**
</dt> <dd>

Участник сопоставлен с подпотоком.

</dd> <dt>

<span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**подпоток PE не \_ \_ сопоставлен**
</dt> <dd>

Участник был отменен из подпотока.

</dd> <dt>

<span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**\_ \_ время ожидания участника PE**
</dt> <dd>

Участник был удален из конференции из-за истечения времени ожидания.

</dd> <dt>

<span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**\_участник PE \_ восстановлен**
</dt> <dd>

Удаленный участник снова становится видимым. Как правило, это участник, для которого истекло время ожидания, но теперь получаются сигналы.

</dd> <dt>

<span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**\_участник PE \_ активен**
</dt> <dd>

Участник стал активным на Конференции.

</dd> <dt>

<span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**\_участник PE \_ неактивен**
</dt> <dd>

Участник стал неактивным на Конференции.

</dd> <dt>

<span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**\_локальный \_ разговор PE**
</dt> <dd>

Локальный участник начал говорить.

</dd> <dt>

<span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**\_Локальное \_ Автоматическое выполнение PE**
</dt> <dd>

Локальный участник стал незамеченным на Конференции.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                              |
| Заголовок<br/>       | <dl> <dt>Ипмсп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Событие ИтпартиЦипантевент:: Get \_**](itparticipantevent-get-event.md)
</dt> <dt>

[Ипконф MSP](ipconf-msp.md)
</dt> <dt>

[Интерфейсы MSP Ипконф](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




