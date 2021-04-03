---
title: Структура MPENDOFLIFE_DATA (Мпклиент. h)
description: '\ 0034; Окончание срока жизни \ 0034; данные уведомления.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA структуры устаревшие функции среды Windows
- Функции PMPENDOFLIFE_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136679"
---
# <a name="mpendoflife_data-structure"></a>\_Структура данных мпендофлифе

Данные уведомления "окончание срока жизни".

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**фтсигнатурикспири**
</dt> <dd>

Тип: **fileTime**

</dd> <dd>

Время истечения срока действия подписи.

</dd> <dt>

**фтплатформекспири**
</dt> <dd>

Тип: **fileTime**

</dd> <dd>

Время истечения срока действия платформы.

</dd> <dt>

**фадминконтроллед**
</dt> <dd>

Тип: **bool** .

</dd> <dd>

Значение true, если администратор управляет политикой отображения уведомления. Если этот параметр задан, в пользовательском интерфейсе не отображается уведомление конца строки.

</dd> <dt>

**фендофлифеимпендингорпаст**
</dt> <dd>

Тип: **bool** .

</dd> <dd>

Значение true, если "окончание срока жизни" находится в состоянии ожидания или в прошлом. Если задано значение false, Пользовательский интерфейс и клиенты могут очищать все состояния, связанные с конца строки.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





