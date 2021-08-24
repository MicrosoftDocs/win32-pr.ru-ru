---
description: Структура NETWORKSTATUS описывает текущее состояние НПП.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Структура NETWORKSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3031cd8bd8f1af4e5ea5f03aec93b9a2f28b3ec098a8110563bb89869c97ae3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799524"
---
# <a name="networkstatus-structure"></a>Структура NETWORKSTATUS

Структура **NETWORKSTATUS** описывает текущее состояние НПП.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a>Члены

<dl> <dt>

**Состояние**
</dt> <dd>

Указывает текущее состояние НПП.



| Значение                                                                                                                                                                                                          | Значение                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <dt>**NETWORKSTATUS, \_ состояние \_ void**</dt> </dl>                | НПП не подключен, или он подключен, а запись не запущена.<br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <dt>**\_захват состояния \_ NETWORKSTATUS**</dt> </dl> | НПП захватывает данные.<br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <dt>**\_ \_ приостановлено состояние NETWORKSTATUS**</dt> </dl>          | НПП приостановлен во время записи данных.<br/>                                     |



 

</dd> <dt>

**Флаги**
</dt> <dd>

Флаги, описывающие текущее состояние НПП.



| Значение                                                                                                                                                                                                                             | Значение                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <dt>**\_ \_ Ожидание триггера NETWORKSTATUS flags \_**</dt> </dl> | Ожидается триггер для НПП.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

При использовании этой структуры необходимо выделить память для структуры, прежде чем ее можно будет использовать, и освободить память, когда структура больше не нужна.

В списке см. также в нижней части этого раздела перечислены все методы, использующие эту структуру.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Иделайдк:: QueryStatus](idelaydc-querystatus.md)
</dt> <dt>

[ИЕСП:: QueryStatus](iesp-querystatus.md)
</dt> <dt>

[ИРТК:: QueryStatus](irtc-querystatus.md)
</dt> <dt>

[Истатс:: QueryStatus](istats-querystatus.md)
</dt> </dl>

 

 




