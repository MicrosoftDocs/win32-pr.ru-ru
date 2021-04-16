---
title: Структура MPTHREAT_DATA (Мпклиент. h)
description: Данные уведомления передаются из-за обнаружения или изменения угроз.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA структуры устаревшие функции среды Windows
- Функции PMPTHREAT_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710549"
---
# <a name="mpthreat_data-structure"></a>\_Структура данных мпсреат

Данные уведомления передаются из-за обнаружения или изменения угроз.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**среатид**
</dt> <dd>

Тип: **мпсреат \_ ID**

</dd> <dd>

Идентификатор угрозы. Верхний бит задан для выявления угроз, связанных с антивирусной программой.

</dd> <dt>

**двсессионид**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Сеанс, связанный с угрозой. Установите значение-1, если сведения о конкретном сеансе недоступны.

</dd> <dt>

**среатактион**
</dt> <dd>

Тип: **[ **\_ действие мпсреат**](mpthreat-action.md)**

</dd> <dd>

Действие угрозы попыталось **выполнить \_ \_ \_ очистку** от / **\_ \_ \_ сбоев** мпнотифи Threat мпнотифи.

</dd> <dt>

**Dwstatus устанавливается**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Дополнительное состояние или действия, связанные с выполняемым действием. Это сочетание битовых флагов из [**\_ флага мпстатус**](mpstatus-flag.md).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_флаг мпстатус**](mpstatus-flag.md)
</dt> <dt>

[**\_действие мпсреат**](mpthreat-action.md)
</dt> </dl>

 

 





