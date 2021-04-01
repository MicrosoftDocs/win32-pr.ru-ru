---
title: Элемент Delay (Буттригжертипе)
description: Указывает промежуток времени между загрузкой системы и началом задачи.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
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
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989392"
---
# <a name="delay-boottriggertype-element"></a>Элемент Delay (Буттригжертипе)

Указывает промежуток времени между загрузкой системы и началом задачи. Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут). Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Элемент **delay** определяется сложным типом [**буттригжертипе**](taskschedulerschema-boottriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                     | Унаследован от                                                               | Описание                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md) | [**буттригжертипе**](taskschedulerschema-boottriggertype-complextype.md) | Указывает триггер, который запускает задачу при загрузке системы.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки скриптов задержка триггера события задается свойством [**буттригжер. Delay**](boottrigger-delay.md) .

Для разработки на C++ задержка триггера события задается свойством [**ибуттригжер::D елай**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) .

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

 

 





