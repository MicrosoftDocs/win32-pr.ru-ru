---
description: Указывает на высокую, среднюю или низкую производительность устройства, на котором работает устаревшая ОС.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Перечисление Упдатеимпактлевел
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662539"
---
# <a name="updateimpactlevel-enumeration"></a>Перечисление Упдатеимпактлевел

Указывает на высокую, среднюю или низкую производительность устройства, на котором работает устаревшая ОС. Это перечисление обычно используется структурами [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) , которые, в свою очередь, вложены в возвращенный [**осупдатеассессмент**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) из [**жетосупдатеассессмент**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**Упдатеимпактлевел \_ Нет**
</dt> <dd>

На ваше устройство не влияет ожидаемое воздействие. Это может быть вызвано тем, что устройство является актуальным или не является актуальным, так как оно учитывает Центр обновления Windows для периодов отсрочки бизнеса или устарело, но еще не достигло порогового значения **дайсаутофдате** , чтобы достичь более высокого уровня влияния.

</dd> <dt>

<span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**Упдатеимпактлевел \_ низкий**
</dt> <dd>

На устройстве не установлена последняя версия ОС, но имеется Последнее обновление.

</dd> <dt>

<span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**Упдатеимпактлевел \_ Средний уровень**
</dt> <dd>

Устройство работает под управлением последней ОС, но имеет умеренное Последнее обновление.

</dd> <dt>

<span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**Упдатеимпактлевел \_ высокий**
</dt> <dd>

Устройство устарело в течение длительного времени. На этом устройстве могут быть уязвимости системы безопасности, и в них могут отсутствовать важные исправления, которые делают Windows более эффективной. Если устройство работает под управлением версии Windows, которая больше не поддерживается, всегда возвращается **упдатеимпактлевел \_ High** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

При вызове [**жетосупдатеассессмент**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) возвращается структура [**осупдатеассессмент**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) . В структуре есть **ассессментфоркуррент** и **ассессментфоруптодате**. Оба из них являются структурами [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) . Оба члена имеют перечисление **упдатеимпактлевел** , которое указывает на высокий, средний, низкий или не оказывает влияния на устройство с устаревшей ОС. Эти уровни определяются значением **дайсаутофдате**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                   |
| IDL<br/>                      | <dl> <dt>Ваасапи. idl</dt> </dl> |



 

 




