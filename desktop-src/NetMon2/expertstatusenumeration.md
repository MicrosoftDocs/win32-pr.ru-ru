---
description: Перечисление ЕКСПЕРТСТАТУСЕНУМЕРАТИОН содержит значения состояния. Он используется элементом Status структуры ЕКСПЕРТСТАТУС и параметром status в Експертиндикатестатус.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Перечисление ЕКСПЕРТСТАТУСЕНУМЕРАТИОН (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ee0729deab566717457f03af27a7e31de8cdf8f1b78f9a5f97b3c3ff406641fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795797"
---
# <a name="expertstatusenumeration-enumeration"></a>Перечисление ЕКСПЕРТСТАТУСЕНУМЕРАТИОН

Перечисление **експертстатусенумератион** содержит значения состояния. Он используется элементом **Status** структуры [експертстатус](expertstatus.md) и параметром *Status* в [експертиндикатестатус](expertindicatestatus.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**ЕКСПЕРТСТАТУС \_ неактивен**
</dt> <dd>

Эксперт никогда не начал работу.

</dd> <dt>

<span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**ЕКСПЕРТСТАТУС \_ Запуск**
</dt> <dd>

Эксперт начинает работу.

</dd> <dt>

<span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**ЕКСПЕРТСТАТУС \_ работает**
</dt> <dd>

Эксперт работает нормально.

</dd> <dt>

<span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**\_проблема експертстатус**
</dt> <dd>

Проблема, указанная в *подсостоянии* , прекратила работу эксперта.

</dd> <dt>

<span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**ЕКСПЕРТСТАТУС \_ прервана**
</dt> <dd>

Сетевой монитор был остановлен эксперт.

</dd> <dt>

<span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**ЕКСПЕРТСТАТУС \_ Готово**
</dt> <dd>

Эксперт успешно завершил работу.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




