---
description: Указывает текущее состояние работающего эксперта.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: Структура ЕКСПЕРТСТАТУС (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540234"
---
# <a name="expertstatus-structure"></a>Структура ЕКСПЕРТСТАТУС

Структура **експертстатус** указывает текущее состояние работающего эксперта.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a>Члены

<dl> <dt>

**Состояние**
</dt> <dd>

Текущее значение состояния эксперта, определенное перечислением [**експертстатусенумератион**](expertstatusenumeration.md) .

</dd> <dt>

**Подсостояние**
</dt> <dd>

Значение подсостояния.

</dd> <dt>

**PercentDone**
</dt> <dd>

Процент выполнения экспертного анализа сетевых данных.

</dd> <dt>

**Frame**
</dt> <dd>

Номер кадра.

</dd> <dt>

**сзстатустекст**
</dt> <dd>

Текст, описывающий состояние эксперта.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




