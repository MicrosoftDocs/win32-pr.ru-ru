---
title: Сложный тип Ексектипе
description: Определяет дочерние элементы и сведения о последовательности элемента exec (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- планировщик задач сложного типа Ексектипе
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489543"
---
# <a name="exectype-complex-type"></a>Сложный тип Ексектипе

Определяет дочерние элементы и сведения о последовательности элемента [**exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) .

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                           | Тип                                                        | Описание                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Аргументы**](taskschedulerschema-arguments-exectype-element.md)               | **string**                                                  | Задает аргументы, связанные с операцией командной строки. <br/>                              |
| [**Get-Help**](taskschedulerschema-command-exectype-element.md)                   | [**пастипе**](taskschedulerschema-pathtype-simpletype.md) | Указывает исполняемый файл или документ для запуска.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | [**пастипе**](taskschedulerschema-pathtype-simpletype.md) | Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.<br/> |



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

 

 





