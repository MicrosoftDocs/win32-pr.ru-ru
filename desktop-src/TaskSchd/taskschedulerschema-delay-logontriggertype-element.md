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
ms.openlocfilehash: a820bad3d68cfb0a697f795a9fd7326c9e52abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492795"
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



## <a name="remarks"></a>Комментарии

Для разработки сценариев задержка триггера входа указывается с помощью свойства [**логонтригжер. Delay**](logontrigger-delay.md) .

Для разработки на C++ идентификатор пользователя для триггера LOGON указывается с помощью свойства [**илогонтригжер::D елай**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





