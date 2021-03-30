---
title: Структура MPCLEAN_DATA (Мпклиент. h)
description: Данные уведомления передаются в функцию чистого обратного вызова.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA структуры устаревшие функции среды Windows
- Функции PMPCLEAN_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801919"
---
# <a name="mpclean_data-structure"></a>\_Структура данных мпклеан

Данные уведомления передаются в функцию чистого обратного вызова.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**среатид**
</dt> <dd>

Тип: **мпсреат \_ ID**

</dd> <dd>

Идентификатор угрозы для **мпнотифи \_ очистки \_ угрозы \_ запустить** / **мпнотифи \_ Clean \_ Threat \_ успешно** / **мпнотифи события \_ \_ \_ сбоя очистки** . Верхний бит задан для выявления угроз, связанных с антивирусной программой.

</dd> <dt>

**среатактион**
</dt> <dd>

Тип: **[ **\_ действие мпсреат**](mpthreat-action.md)**

</dd> <dd>

Действие угрозы для **мпнотифи " \_ Очистка \_ \_ после** сбоя" мпнотифи "очистить угрозу" / **\_ \_ \_** / .**мпнотифи удалить события с \_ \_ \_ ошибками** . См. раздел [**\_ действие мпсреат**](mpthreat-action.md).

</dd> <dt>

**Dwstatus устанавливается**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Дополнительное состояние или действия, связанные с выполняемым действием. Это сочетание битовых флагов из [**\_ флага мпстатус**](mpstatus-flag.md).

</dd> <dt>

**ресаурцеинфо**
</dt> <dd>

Тип: **пмпресаурце \_ info** .

</dd> <dd>

Сведения о ресурсах **для \_ мпнотифи \_ очистки \_** мпнотифи об очистке угрозы "Очистка после сбоя" / **\_ \_ \_** / **мпнотифи " \_ очистить \_ угрозу \_** ". См [**. \_ сведения о мпресаурце**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_сведения о мпресаурце**](mpresource-info.md)
</dt> <dt>

[**\_флаг мпстатус**](mpstatus-flag.md)
</dt> <dt>

[**\_действие мпсреат**](mpthreat-action.md)
</dt> </dl>

 

 





