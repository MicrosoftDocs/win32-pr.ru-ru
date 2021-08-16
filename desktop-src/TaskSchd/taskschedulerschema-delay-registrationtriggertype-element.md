---
title: Элемент Delay (Регистратионтригжертипе)
description: Указывает промежуток времени между регистрацией задачи и началом задачи.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
keywords:
- планировщик задач элемента Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd7ba3e9fd0fb71da628ee15bc0f1bdf6281e74ef20f259faf7a5a63504a6f12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131853"
---
# <a name="delay-registrationtriggertype-element"></a>Элемент Delay (Регистратионтригжертипе)

Указывает промежуток времени между регистрацией задачи и началом задачи. Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут). Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Элемент **delay** определяется сложным типом [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                     | Унаследован от                                                                               | Описание                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md) | Указывает триггер, который запускает задачу при регистрации задачи.<br/> |



## <a name="remarks"></a>Remarks

Для разработки сценариев задержка триггера регистрации указывается с помощью свойства [**регистратионтригжер. Delay**](registrationtrigger-delay.md) .

Для разработки на C++ задержка триггера регистрации указывается с помощью свойства [**ирегистратионтригжер::D елай**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет задержку триггера регистрации, которая допускает задержку в 5 минут между регистрацией задачи и запуском задачи.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





