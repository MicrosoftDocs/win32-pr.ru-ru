---
title: Структура MPEXPIRATION_DATA (Мпклиент. h)
description: Уведомление о состоянии истечения срока действия продукта.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA структуры устаревшие функции среды Windows
- функции PMPEXPIRATION_DATA Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f270b7d433e6de7cd1eb3e7a3cfc88c9cb85c6087c20371ac804ec61d949d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976034"
---
# <a name="mpexpiration_data-structure"></a>\_Структура данных мпекспиратион

Уведомление о состоянии истечения срока действия продукта.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**Причина**
</dt> <dd>

Тип: **\_ \_ Причина истечения срока действия MP**

</dd> <dd>

Причина истечения срока действия. Это одно из следующих возможных значений.



| Значение                                                                                                                                                                                                                                | Значение                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <dt>**Пакет управления \_ Истек срок действия \_ неизвестного**</dt> <dt>0</dt> </dl> | Неизвестно.<br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <dt>**Пакет управления \_ Срок действия \_ пробной оценки**</dt> <dt>1</dt> истек </dl>          | Аттестаци.<br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <dt>**Пакет управления \_ Истек срок действия \_ западноафриканскому**</dt> <dt>2</dt> </dl>             | Западноафриканскому.<br/>        |



 

</dd> <dt>

**Состояние**
</dt> <dd>

Тип: **\_ \_ \_ отчет о состоянии истечения срока действия пакета управления**

</dd> <dd>

Состояние истечения срока действия. Это одно из следующих возможных значений.



| Значение                                                                                                                                                                                                                                                                      | Значение                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <dt>**Пакет управления \_ Отчет о состоянии истечения срока действия \_ \_ \_ неизвестен**</dt> <dt>0</dt> </dl> | Состояние неизвестно.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <dt>**Пакет управления \_ \_ \_ \_ Допустимый отчет о состоянии истечения срока действия**</dt> <dt>1</dt> </dl>       | Без истечения срока действия.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <dt>**Пакет управления \_ \_ \_ \_ Предупреждение о состоянии истечения срока действия**</dt> <dt>2</dt> </dl> | Приближается срок действия.<br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <dt>**Пакет управления \_ \_ \_ \_ Срок действия отчета об ИСтечении срока действия истек**</dt> <dt>3</dt> </dl> | Истек.<br/>       |



 

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





