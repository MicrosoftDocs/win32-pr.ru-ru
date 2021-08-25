---
title: EventTrigger. Delay, свойство
description: Для создания скриптов Возвращает или задает значение, указывающее промежуток времени между возникновением события и моментом запуска задачи.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- планировщик задач свойства Delay
- Свойство Delay планировщик задач, объект EventTrigger
- Объект EventTrigger планировщик задач, свойство Delay
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402ddb8e55f6eb22a4e2c106b64cbec3ed1afa6d0b58f38a2a8923f5bd8dfa4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959594"
---
# <a name="eventtriggerdelay-property"></a>EventTrigger. Delay, свойство

Для создания скриптов Возвращает или задает значение, указывающее промежуток времени между возникновением события и моментом запуска задачи. Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).

## <a name="syntax"></a>Синтаксис


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a>Значение свойства

Значение, указывающее промежуток времени между возникновением события и моментом запуска задачи.

## <a name="remarks"></a>Remarks

При чтении или записи собственного XML-кода для задачи задержка события указывается с помощью элемента [**delay**](taskschedulerschema-delay-eventtriggertype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

 





