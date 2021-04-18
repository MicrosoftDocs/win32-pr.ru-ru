---
title: Сложный тип Идлесеттингстипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Идлесеттингс (Сеттингстипе).
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- планировщик задач сложного типа Идлесеттингстипе
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681846"
---
# <a name="idlesettingstype-complex-type"></a>Сложный тип Идлесеттингстипе

Определяет дочерние элементы и сведения о последовательности для элемента [**идлесеттингс (сеттингстипе)**](taskschedulerschema-idlesettings-settingstype-element.md) .

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="WaitTimeout"
            default="PT1H"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                  | Тип    | Описание                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Длительность**](taskschedulerschema-duration-idlesettingstype-element.md)                |         | Указывает время, отведенное на запуск задачи в условиях простоя.<br/>                                                                                                                     |
| [**рестартонидле**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | Логическое | Задача перезапускается сразу же после запуска условия простоя.<br/>                                                                                                                                             |
| [**стопонидлинд**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | Логическое | Указывает, что задача завершается, если условие простоя заканчивается до превышения длительности простоя.<br/>                                                                                                 |
| [**ваиттимеаут**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | Указывает период времени, в течение которого ожидается запуск условия простоя. Если для этого элемента не указано значение, то служба планировщик задач будет ждать неопределенное время, пока не произойдет условие простоя.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





