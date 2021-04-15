---
title: Period, элемент
description: Указывает, как часто задача должна запускаться во время автоматического обслуживания.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Элемент period планировщик задач
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493122"
---
# <a name="period-element"></a>Period, элемент

Указывает, как часто задача должна запускаться во время автоматического обслуживания.

Формат этой строки — *пнинмндтнхнмнс*, где *Москва* — количество лет, NM — это число *месяцев,* равное числу дней, *T* — разделителю даты и времени, *NH* — число *часов, число* минут, а значение *NS* равно числу секунд (например, "PT5M" указывает 5 минут, а "P1M4DT2H5M" — один месяц, четыре дня, два часа и пять минут). Минимальное значение — одна минута. Дополнительные сведения о типе длительности см. в разделе [схема XML, часть 2: тип данных Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент **period** определяется сложным типом [**маинтенанцесеттингстипе**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                                          | Унаследован от                                                                               | Описание                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Маинтенанцесеттингс (Маинтенанцесеттингстипе)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**маинтенанцесеттингстипе**](taskschedulerschema-maintenancesettingstype-complextype.md) | Задает параметры задачи, которые планировщик задач будет использовать для запуска задачи во время автоматического обслуживания.<br/> |



## <a name="remarks"></a>Комментарии

При программировании на C++ этот параметр простоя указывается с помощью свойства [**имаинтенанцесеттингс::P ериод**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) .

## <a name="examples"></a>Примеры

Следующий код XML определяет задачу обслуживания с требованием периодичности, равным 5 дням.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
</MaintenanceSettings>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





