---
title: Элемент Delay (Логонтригжертипе)
description: Промежуток времени между входом пользователя в систему и запуском задачи.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
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
ms.openlocfilehash: 1bd18652630ad14f9b888db6a810d8da1eb42a18fb9d2caa6726414aa9054702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357144"
---
# <a name="delay-logontriggertype-element"></a>Элемент Delay (Логонтригжертипе)

Промежуток времени между входом пользователя в систему и запуском задачи. Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут). Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Элемент **delay** определяется сложным типом [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                       | Унаследован от                                                                 | Описание                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md) | Указывает триггер, который запускает задачу при входе пользователя в систему.<br/> |



## <a name="remarks"></a>Remarks

Для разработки сценариев задержка триггера входа указывается с помощью свойства [**логонтригжер. Delay**](logontrigger-delay.md) .

Для разработки на C++ идентификатор пользователя для триггера LOGON указывается с помощью свойства [**илогонтригжер::D елай**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) .

## <a name="requirements"></a>Требования



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

 

 





