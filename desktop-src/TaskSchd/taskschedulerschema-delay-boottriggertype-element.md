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
ms.openlocfilehash: 91789b22b992af163e9676ef156a2a72f4316ac49b9b47b30ae5599446918bed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334604"
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



## <a name="remarks"></a>Remarks

Для разработки скриптов задержка триггера события задается свойством [**буттригжер. Delay**](boottrigger-delay.md) .

Для разработки на C++ задержка триггера события задается свойством [**ибуттригжер::D елай**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) .

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

 

 





