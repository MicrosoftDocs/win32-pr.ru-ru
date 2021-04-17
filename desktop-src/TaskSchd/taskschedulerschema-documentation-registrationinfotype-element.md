---
title: Элемент Documentation (Регистратионинфотипе)
description: Указывает любую дополнительную документацию для задачи.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Элемент Documentation планировщик задач
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682136"
---
# <a name="documentation-registrationinfotype-element"></a>Элемент Documentation (Регистратионинфотипе)

Указывает любую дополнительную документацию для задачи.

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

Элемент **Documentation** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                           | Унаследован от                                                                         | Описание                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) | Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.<br/> |



## <a name="remarks"></a>Комментарии

Для приложений со скриптами дополнительная документация по задачам указывается с помощью свойства [**RegistrationInfo.Docументатион**](registrationinfo-documentation.md) .

Для приложений C++ Дополнительная документация по задачам указывается с помощью свойства [**ирегистратионинфо::D kumentace**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





