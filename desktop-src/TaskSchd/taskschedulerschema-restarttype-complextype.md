---
title: Сложный тип Рестарттипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Рестартонфаилуре.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- планировщик задач сложного типа Рестарттипе
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 996debc2c8e3d7d00ca7b42facde582f918d72736426ed326691461d800f8562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516483"
---
# <a name="restarttype-complex-type"></a>Сложный тип Рестарттипе

Определяет дочерние элементы и сведения о последовательности для элемента [рестартонфаилуре](taskschedulerschema-restartonfailure-settingstype-element.md) .

``` syntax
<xs:complexType name="restartType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                              | Тип | Описание                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [**Count**](taskschedulerschema-count-restarttype-element.md)       |      | Число попыток перезапуска задачи.<br/> |
| [**Интервал**](taskschedulerschema-interval-restarttype-element.md) |      | Длительность попытки запуска задачи.<br/>      |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





