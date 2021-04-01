---
description: Структура НЕТВОРКИНФО описывает сетевую карту.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Структура НЕТВОРКИНФО (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818529"
---
# <a name="networkinfo-structure"></a>Структура НЕТВОРКИНФО

Структура НЕТВОРКИНФО описывает сетевую карту.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**перманентаддр**
</dt> <dd>

Постоянный MAC-адрес.

</dd> <dt>

**куррентаддр**
</dt> <dd>

Текущий MAC-адрес.

</dd> <dt>

**OtherAddress**
</dt> <dd>

Другой адрес, поддерживающий эту возможность (например, IP, IPX).

</dd> <dt>

**LinkSpeed**
</dt> <dd>

Скорость связи в Мбит/с.

</dd> <dt>

**MacType**
</dt> <dd>

Тип носителя.

</dd> <dt>

**MaxFrameSize**
</dt> <dd>

Максимально допустимый размер кадра.

</dd> <dt>

**Флаги**
</dt> <dd>

Этот параметр может иметь один из следующих информационных флагов:



| Значение                                                                                                                                                                                                                                       | Значение                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <dt>**\_Флаги нетворкинфо \_ пмоде \_ не \_ поддерживаются**</dt> </dl>    | Сетевой адаптер не поддерживает неизбирательный режим, то есть он будет записывать только трафик, который является широковещательным или включает только локальный компьютер.<br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <dt>**НЕТВОРКИНФО \_ Флаги \_ RAS**</dt> </dl>                                                      | Это виртуальная сетевая карта, которая является подключением к серверу удаленного доступа (RAS) через модем или другую сетевую карту.<br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <dt>**\_ \_ удаленная карта ФЛАГов нетворкинфо \_**</dt> </dl>                             | Сетевая карта не находится на локальном компьютере, но записывается на удаленном компьютере в соответствии с заданной учетной записью на локальном компьютере.<br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <dt>**НЕТВОРКИНФО \_ Флаги \_ удаленного \_ NAL**</dt> </dl>                                | Устаревшие не используйте.<br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <dt>**НЕТВОРКИНФО \_ помечает \_ Удаленный \_ NAL \_ Connected**</dt> </dl> | Устаревшие не используйте.<br/>                                                                                                                                          |



 

</dd> <dt>

**тиместампскалефактор**
</dt> <dd>

Например, значение 1 указывает на 1/1 мс, 10 — на 1/10 мс, 100 — на 1/100 мс и т. д.

</dd> <dt>

**NodeName**
</dt> <dd>

Имя удаленной рабочей станции.

</dd> <dt>

**пмодесуппортед**
</dt> <dd>

Индикатор поддержки сетевого интерфейса P-Mode.

</dd> <dt>

**Комментарий**
</dt> <dd>

Поле комментария адаптера.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




